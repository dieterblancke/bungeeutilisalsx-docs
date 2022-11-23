# FAQ / Common Issues

# Using unicode causes weird characters to occur

In this case, you are most likely running your server on a Windows Machine.

However, there is a simple way to fix this:
1. Shutdown your BungeeCord server
1. Open your start script
1. Add -Dfile.encoding=UTF-8 in front of -jar
1. Start your BungeeCord server, all should be working fine now.

For MultiCraft, you should locate the .jar.conf file of your BungeeCord, and edit the command field with the same steps as mentioned above.
# I am getting a SSL warning

If the warning is similar to the one below, then open the main configuration file. Under storage, set useSSL to false.

```
Establishing SSL connection without server's identity verification is not recommended.
According to MySQL 5.5.45+, 5.6.26+ and 5.7.6+ requirements SSL connection must be established by default if explicit option isn't set.
For compliance with existing applications not using SSL the verifyServerCertificate property is set to 'false'.
You need either to explicitly disable SSL by setting useSSL=false, or set useSSL=true and provide truststore for server certificate verification.
```

# I'm getting an error on startup
If you're getting an error on startup, just contact didjee2 on Spigot, MC-Market or Discord for help.

If the error contains the following:
`Caused by: java.lang.NoSuchMethodError: com.zaxxer.hikari.HikariConfig.setInitializationFailTimeout(J)V`

Then make sure to check for other plugins that use MySQL (specifically HikariCP) as their Hikari might be outdated.

# When I use one bold color code, the entire message becomes bold
This is a "bug" ever since BungeeUtilisalsX v2.3.5, although this is intended behaviour.

To avoid / fix this, please use the MiniMessage syntax for bold messages, or use the 'reset' color code when you want the bold text to stop.

For example:
```
This is &lsome bold text &rand this is some normal text.
```
or:
```
This is <bold>some bold text</bold> and this is some normal text.
```

# A new Minecraft version came out, but I cannot use it in my MOTD yet?
BungeeUtilisalsX does not automatically map newer versions, for that I need to make a migration so the plugin can support the new version.

In the meantime, since BungeeUtilisalsX v2.4.0, you can navigate to the /plugins/BungeeUtilisalsX/_internal folder and open the versions.json file.
In there, you can find the version mappings, if you want to add a new version, you can just add the version mapping by looking up the [protocol version](https://minecraft.fandom.com/wiki/Protocol_version).

For example for 1.19.1, you can add this to the versions.json file (its already present):
```
    {
      "versionName": "1.19.1",
      "protocolVersion": 760
    }
```

It is important to note that there should be **NO DUPLICATE** protocol versions.
One protocol version can only be mapped to one version name (while it's possible for Minecraft to have multiple version numbers per mapping, for example 1.19.1 and 1.19.2 both have 760 as protocol versions).

If it is not urgent, you don't have to do any of this and you can just wait for the next update, make sure to ask me about it on [my support Discord](https://discord.dieterblancke.xyz) if you want to speed things up!