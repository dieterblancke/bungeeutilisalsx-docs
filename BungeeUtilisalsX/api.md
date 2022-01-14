# Developer API

# Bossbar API
* For all IBossBar methods, please [check it out here](https://git.dieterblancke.xyz/dbsoftwares/BungeeUtilisalsX/blob/master/api/src/main/java/com/dbsoftwares/bungeeutilisals/api/bossbar/IBossBar.java)!
* BossBar Actions, Colors & Styles can [also be found in the same package](https://git.dieterblancke.xyz/dbsoftwares/BungeeUtilisalsX/tree/master/api/src/main/java/com/dbsoftwares/bungeeutilisals/api/bossbar).
* The different methods to [create a bossbar can be found here](https://git.dieterblancke.xyz/dbsoftwares/BungeeUtilisalsX/blob/master/api/src/main/java/com/dbsoftwares/bungeeutilisals/api/BUAPI.java#L236-258)!

## Creating a BossBar
```java
final IBuXApi api = BuX.getApi();

// Creating BossBar: api.createBossBar(BarColor color, BarStyle style, float progress, BaseComponent[] message)
IBossBar bossBar = api.createBossBar( BarColor.YELLOW, BarStyle.SOLID, 0.0F, Utils.format( "&aExample Message ..." ) );

// Adding all online users | this basically broadcasts the BossBar on the local proxy
api.getUsers().forEach( bossBar::addUser );
```

It is recommended to unregister Bossbar objects when they are not being used, as for every bossbar made, there is an event registered. <br>
This event listens for users leaving the network, so they can be removed from the bossbar (in order to prevent memory leaks).

```java
bossbar.unregister();
```

# Configuration API
BungeeUtilisalsX has a configuration API, similar to the one of Bukkit, implemented for both YAML & JSON files. <br>
This ConfigurationAPI is a separate project, which also [has it's own repository](https://git.dieterblancke.xyz/dbsoftwares/ConfigurationAPI/blob/master/README.md), here you can find more info about how to use it.

> [!WARNING|style:flat]
> An exception will be thrown if the file does not exist! In order to avoid this, make sure that the file exists (empty or not) before loading it.

## Loading a JSON file
```java
// Creating new configuration instance
IConfiguration jsonExample = IConfiguration.loadJsonConfiguration(new File(getDataFolder(), "jsonExample.json"));

// Loading configuration defaults from plugin resources
try {
    jsonExample.copyDefaults(IConfiguration.loadJsonConfiguration(getResourceAsStream("jsonExample.json")));
} catch (IOException e) {
    System.out.println("Could not load configuration defaults: ");
    e.printStackTrace();
}

// Get a String from the config
String test = jsonExample.getString("test");

// Set a value in the config
jsonExample.set("test.test2", 16);

// Save the config
try {
    jsonExample.save();
} catch (IOException e) {
    System.out.println("Could not save configuration: ");
    e.printStackTrace();
}

// Reload config (for when something manually got changed in the configuration)
// Reloading is NOT REQUIRED AFTER SAVING
try {
    jsonExample.reload();
} catch (IOException e) {
    System.out.println("Could not reload configuration: ");
    e.printStackTrace();
}
```

## Loading a YAML file
```java
// Creating new configuration instance
IConfiguration yamlExample = IConfiguration.loadYamlConfiguration(new File(getDataFolder(), "yamlExample.yml"));

// Loading configuration defaults from plugin resources
try {
    yamlExample.copyDefaults(IConfiguration.loadYamlConfiguration(getResourceAsStream("yamlExample.yml")));
} catch (IOException e) {
    System.out.println("Could not load configuration defaults: ");
    e.printStackTrace();
}

// Get a String from the config
String test = yamlExample.getString("test");

// Set a value in the config
yamlExample.set("test.test2", 16);

// Save the config
try {
    yamlExample.save();
} catch (IOException e) {
    System.out.println("Could not save configuration: ");
    e.printStackTrace();
}

// Reload config (for when something manually got changed in the configuration)
// Reloading is NOT REQUIRED AFTER SAVING
try {
    yamlExample.reload();
} catch (IOException e) {
    System.out.println("Could not reload configuration: ");
    e.printStackTrace();
}
```

# Custom Language Integration
By default, BungeeUtilisalsX uses it's own system to handle user languages, however, some servers have their own Language System / API that they use. For this, they could use this API.

## Registering Language Fetcher
This is by far the easiest implementation, this just gets called when a user's language is being requested.
```java
ILanguageManager langManager = BuX.getApi().getLanguageManager();

langManager.setLanguageIntegration(uuid -> {
    Language language = null;

    try (Connection connection = database.getConnection()) {
        PreparedStatement pstmt = connection.prepareStatement("SELECT lang FROM users WHERE uuid = ?;");
        pstmt.setString(1, uuid.toString());

        try (ResultSet rs = pstmt.executeQuery()) {
            if (rs.next()) {
                language =  langManager.getLangOrDefault(rs.getString("lang"));
            }
        }
    } catch (SQLException e) {
        e.printStackTrace();
    }

    return language == null ? langManager.getDefaultLanguage() : language;
});
```

## Creating a custom language manager
You could also create a custom language manager, which you could base on the default language manager ([PluginLanguageManager](https://github.com/dieterblancke/BungeeUtilisalsX/blob/master/common/src/main/java/com/dbsoftwares/bungeeutilisals/language/PluginLanguageManager.java) and [AbstractLanguageManager](https://github.com/dieterblancke/BungeeUtilisalsX/blob/master/bungee/src/main/java/com/dbsoftwares/bungeeutilisals/language/AbstractLanguageManager.java)).

You could also just make a custom LanguageManager which extends PluginLanguageManager and override the methods you want to see changed.
**Note:** This is the more "hacky" way of implementing your custom language manager by using Reflection to do so. Please do not use this if you don't understand what you are doing.
```java
// Creating new ILanguageManager instance
final ILanguageManager languageManager = new YourCustomLanguageManager();

// Getting languageManager field.
Field languageManagerField = ReflectionUtils.getField(BuX.getApi().getClass(), "languageManager");
try {
    // Attempting to update languageManager field to new, custom, ILanguageManager instance.
    languageManagerField.set(BuX.getApi().getClass(), languageManager);
} catch (IllegalAccessException e) {
    e.printStackTrace();
}
```

# PlaceHolders
A list of placeholders can be [found here](placeholders.md).
PlaceHolderAPI path is [be.dieterblancke.bungeeutilisalsx.common.api.placeholder.PlaceHolderAPI](https://github.com/dieterblancke/BungeeUtilisalsX/blob/master/common/src/main/java/be/dieterblancke/bungeeutilisalsx/common/api/placeholder/PlaceHolderAPI.java) 

## Formatting a message
To replace a placeholder, there are two methods, one for general placeholders:
```java
final String message = PlaceHolderAPI.formatMessage("Online Players in our lobby: {getcount: Lobby1}");
```
and one for both general and user related placeholders:
```java
final String message = PlaceHolderAPI.formatMessage("Hello {user}, there are {getcount: Lobby1} players in our lobby!");
```

## Create your own placeholder
### Normal PlaceHolder
A normal placeholder simply gets replaced by what you return in your handler.
The parameters this method takes is the placeholder to be replaced, a boolean whether the placeholder involves a user, and the placeholder handler.

```java
PlaceHolderAPI.addPlaceHolder("{user-server}", true, new PlaceHolderEventHandler() {
    @Override
    public String getReplacement(PlaceHolderEvent event) {
        return event.getUser().getServerName();
    }
});
```

### Input PlaceHolder
An input placeholder requests an argument which you can use to return your result.
The parameters this method takes is a boolean whether or not the placeholder involves an user, the placeholder prefix, and the placeholder handler.

In this example, the placeholder would be {upper: your text that has to be in upper case}
```java
PlaceHolderAPI.addPlaceHolder(false, "upper", new InputPlaceHolderEventHandler() {
    @Override
    public String getReplacement(InputPlaceHolderEvent event) {
        return event.getArgument().toUpperCase();
    }
});
```