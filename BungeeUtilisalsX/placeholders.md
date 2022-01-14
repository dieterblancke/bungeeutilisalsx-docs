# PlaceHolders

**NOTES:**
- The placeholders displayed here are not all placeholders! There are many, message-specific placeholders available. For this, check out the [language files](https://github.com/dieterblancke/BungeeUtilisalsX/blob/master/common/src/main/resources/languages/).
- If you want additional placeholders that are not available yet, feel free to ask me to add them on [my Discord](https://discord.dieterblancke.xyz)!

## General PlaceHolders
| PlaceHolder            | Explanation                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `{timeleft: targetTime}` | Shows the time left untill a certain time. targetTime must be of format dd-MM-yyyy hh:mm:ss, for example 01-01-2020 00:00:00, which would be first of january 2020, midnight.                                                            |
| `{getcount: server}`     | Shows the amount of players online on a server. server can be both a ServerGroup or a ServerName.                                                                                                                                        |
| `{proxy_online}`         | Gets replaced by the total amount of players online (redis is supported)                                                                                                                                                                 |
| `{proxy_max}`            | Gets replaced by the max players you have setup in your BungeeCord config                                                                                                                                                                |
| `{date}`                 | Gets replaced by the current date, the format is located in the language file under placeholders.format.date. For more info on date formatting, see https://docs.oracle.com/javase/7/docs/api/java/text/SimpleDateFormat.html            |
| `{time}`                 | Gets replaced by the current time, the format is located in the language file under placeholders.format.time. For more info on date formatting, see https://docs.oracle.com/javase/7/docs/api/java/text/SimpleDateFormat.html            |
| `{datetime}`             | Gets replaced by the current date & time, the format is located in the language file under placeholders.format.datetime. For more info on date formatting, see https://docs.oracle.com/javase/7/docs/api/java/text/SimpleDateFormat.html |

## User PlaceHolders
| PlaceHolder      | Explanation                                                               |
|------------------|---------------------------------------------------------------------------|
| `{user}`           | Gets replaced by the name of this user                                    |
| `{me}`             | Gets replaced by the name of this user (alternative to `{user}`)            |
| `{user_prefix}`    | Gets replaced by the prefix of this user (from the staffranks file)       |
| `{ping}`           | Gets replaced by the ping of this user                                    |
| `{server}`         | Gets replaced by the server this user is currently in                     |
| `{server_online}`  | Gets replaced by the player count of the server this user is currently in |
| `{language_short}` | Gets replaced by the language of this user, formatted like "en"           |
| `{language_long}`  | Gets replaced by the language of this user, formatted like "en_US"        |

## Permission PlaceHolders
These placeholders currently only support LuckPerms **BungeeCord / Velocity**.
If any other permission plugins should be integrated, please contact my on [my Discord](https://discord.dieterblancke.xyz)!

| PlaceHolder | Explanation                                                  |
| --- |--------------------------------------------------------------|
| `{permission_user_prefix}` | Gets replaced by the prefix for this user                    |
| `{permission_user_suffix}` | Gets replaced by the suffix for this user                    |
| `{permission_user_primary_group}` | Gets replaced by the primary group this user is currently in |

## XML PlaceHolders
| PlaceHolder                                                                          | Explanation                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<center>ENTER TEXT</center>` <br/>`<center padchar="-">ENTER TEXT</center>` | This placeholder attempts to center a given amount of text in the Minecraft chat box.<br/> If the padchar attribute is set, it will use that attribute as filler instead of a space. |

## Punishment PlaceHolders
| PlaceHolder            | Explanation                                                                          |
|------------------------|--------------------------------------------------------------------------------------|
| `{reason}`         | Gets replaced with the punishment reason                                             |
| `{date}`           | Gets replaced with the punishment execution date                                     |
| `{by}`             | Gets replaced with the punisher name                                                 |
| `{server}`         | Gets replaced with the server where it was executed on                               |
| `{uuid}`           | Gets replaced with the punished person his uuid                                      |
| `{ip}`             | Gets replaced with the punished person his IP                                        |
| `{user}`           | Gets replaced with the punished person his name                                      |
| `{id}`             | Gets replaced with the punishment ID                                                 |
| `{type}`           | Gets replaced with the punishment type (f.e. BAN, MUTE, ...)                         |
| `{expire}`         | Gets replaced with the expiry date (if temporary punishment)                         |
| `{timeLeft}`       | Gets replaced with the time that is left until the punishment expires (or "Never")   |
| `{removedBy}`      | Gets replaced by the user that removed this punishment (or "Unknown" if not removed) |
| `{punishment_uid}` | Gets replaced by the punishment UID (this is different from the ID)                  |

## MOTD PlaceHolders
| PlaceHolder | Explanation                                                                           |
|------------|---------------------------------------------------------------------------------------|
| `{user}`     | Gets replaced with the username, "Unknown" if username is not known.                  |
| `{version}`  | Gets replaced with the client version, "Unknown" if version is not found / not known. |
| `{domain}`   | Gets replaced with the used domain, "Unknown" if not found.                           |