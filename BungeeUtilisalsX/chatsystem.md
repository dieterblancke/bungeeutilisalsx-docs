# Chat & Announcer System
BungeeUtilisalsX has several chat management and enhancement features to both make the chatting experience more pleasant and more richful.

# Announcer Systems
Each announcer system has the following settings in their respective configurations:
- `enabled`: whether the announcer should be enabled.
- `random`: whether announcement messages should be randomized or not.
- `group-per-server`: whether the announcer should group messages per server or not. 
If you have a lot of servers that you announce to, it could take a long time till the announcer cycled through all available announcements.
By putting this option to true, the announcer will cycle through announcements on a per-server basis.
- `delay`: the delay between announcement messages, the unit can be one of the following values: `NANOSECONDS, MICROSECONDS, MILLISECONDS, SECONDS, MINUTES, HOURS, DAYS, WEEKS`

Each of the server's that can be entered support [the servergroup system](/other#servergroups).

## Actionbar Announcer
The actionbar announcer sends "announcements" in the actionbar. These announcements can be used as animations too by leaving a low enough delay between messages.

Each actionbar announcement is represented by a list section in the config, for example:
```yaml
# You can enter a ServerGroup name or a ServerName in here.
- server: Global
  # If set to true, BungeeUtilisalsX will search the message in the language file of the user.
  use-language: false
  # How long should the actionbar be shown (in seconds)
  time: 1
  # Permission you need in order to receive the announcement, leave empty if no permission.
  permission: 'bungeeutilisals.announcements.receive'
  # The message to be sent in the actionbar or a YAML path
  message: '&eThis server is using BungeeUtilisals'
```
For additional announcements, you just have to copy - paste the list section and edit the message!

## Bossbar Announcer
BungeeUtilisalsX comes with a BossBar system built in, which also allows you to use bossbar announcements!

```yaml
# You can enter a ServerGroup name or a ServerName in here.
- server: Global
  # How long should the bossbar be shown?
  # Set to -1 to keep the bossbar until the next announcement
  stay: -1
  # Permission you need in order to receive the announcement, leave empty if no permission.
  permission: 'bungeeutilisals.announcements.receive'
  # Every new line = a new BossBar (up to 5 bossbars at ONE POINT possible!)
  messages:
    # BarColor PINK, BLUE, RED, GREEN, YELLOW, PURPLE, WHITE
    - color: 'YELLOW'
      # SOLID, SIX_SEGMENTS, TEN_SEGMENTS, TWELVE_SEGMENTS, TWENTY_SEGMENTS
      style: 'SOLID'
      # Number between 0.0 & 1.0
      progress: 1.0
      # Set to true if the text is a path to a language message
      language: false
      # The message to be sent in the bossbar or a YAML path
      text: '&eThis server is using BungeeUtilisals'
      # BarColor PINK, BLUE, RED, GREEN, YELLOW, PURPLE, WHITE
    - color: 'GREEN'
      # SOLID, SIX_SEGMENTS, TEN_SEGMENTS, TWELVE_SEGMENTS, TWENTY_SEGMENTS
      style: 'SOLID'
      # Number between 0.0 & 1.0
      progress: 1.0
      # Set to true if the text is a path to a language message
      language: false
      # The message to be sent in the bossbar or a YAML path
      text: '&aJoin the DBSoftwares Discord at &bhttps://discord.dieterblancke.xyz&a!'
```
For additional announcements, you just have to copy - paste the list section and edit the message!

## Chat Announcer
The chat announcer allows you to send a simple chat announcement.
[Text section messages](/languages#text-section-messages) can be used by enabling use-language and linking to the language file.

```yaml
# You can enter a ServerGroup name or a ServerName in here.
- server: Global
  # If set to true, the prefix set in the user's languages file will be used in the announcements.
  use-prefix: true
  # Permission you need in order to receive the announcement, leave empty if no permission.
  permission: 'bungeeutilisalsx.announcements.receive'
  # These are the lines of the message that will be sent, each new line is a new line in the chat.
  messages:
    - '&eThis server is using BungeeUtilisals:'
    - '&6BungeeUtilisals has been coded by &bdidjee2&6.'
```
For additional announcements, you just have to copy - paste the list section and edit the message!

## Tab Announcer
The tab announcer allows you to send / update a user's tab. It's not necessarily an announcer, but could be used as one.

```yaml
# You can enter a ServerGroup name or a ServerName in here.
- server: Global
  # Permission you need in order to receive the announcement, leave empty if no permission.
  permission: ''
  # Should the message be retrieved from the language files? If true, you must use a valid path!
  language: false
  # The lines for the header of the tab list.
  header:
    - 'Tab Header Message'
  # The lines for the footer of the tab list.
  footer:
    - 'Tab Footer Message'
```

## Title Announcer
BungeeUtilisalsX also allows you to send announcements through titles and subtitles.

```yaml
# You can enter a ServerGroup name or a ServerName in here.
# Do note that ServerGroup names will be prioritized above ServerNames.
- server: Global
  # How long should the title fade in?
  fadein: 10
  # How long should the title stay?
  stay: 30
  # How long should the title fade out?
  fadeout: 10
  # Permission you need in order to receive the announcement, leave empty if no permission.
  permission: 'bungeeutilisals.announcements.receive'
  # Should the message be retrieved from the language files? If true, you must use a valid path!
  language: false
  # Title text, if language is set to true, the path will be searched in the language file.
  title: '&c&lBungeeUtilisals'
  # SubTitle text, if language is set to true, the path will be searched in the language file.
  subtitle: '&dThank you for using our plugin!'
```

# UTF Symbol Enhancements
## Fancy Chat
By enabling fancy chat, BungeeUtilisalsX will replace one of the following characters with a (fancier looking) UTF symbol:
`abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ,?;.:+=-%*$!'"@|&<>0123456789#`

## UTF Symbols
This system allows you to create custom placeholders that can be replaced with UTF symbols.

For example `<3` or `:heart:` can be replaced with \u2764, which is the java code for: ❤.
The full configuration for it would be:
```yaml
symbols:
  enabled: true
  permission: 'bungeeutilisals.chat.symbols'
  symbols:
    '\u2764': '<3, :heart:'
```

Any amount of placeholder -> utf symbol replacements can be added this way, by default BungeeUtilisalsX already supplies some fun symbols you can play with!

# Chat Protection Systems
BungeeUtilisalsX comes with some built-in chat protection systems, while these are somewhat simple, you can often customize the used patterns and make it more advanced.

## Anti Advertise
BungeeUtilisalsX's anti advertise has two pre-definted patterns which are editable in the `chat/protection/antiadvertise.yml` configuration file.
Only edit these if you know what you are doing!

It's also possible to set up the domains that the anti advertise can ignore.
Like other protection systems, the anticaps system also has a bypass permission and commands that can be executed on detection.

## Anti Caps
The anticaps system can be configured with the following options:
- `caps characters`: a list of characters that should be considered as caps, by default this is `ABCDEFGHIJKLMNOPQRSTUVWXYZ`.
- `cancel`: if this is set to false, BungeeUtilisalsX will lowercase the message, otherwise cancel the message.
- `min-length`: the minimum length a message should be for it to be checked for caps (so abbreviations like 'LMAO' wouldn't be flagged).
- `percentage`: the maximum percentage of caps letters a message can contain.

Like other protection systems, the anticaps system also has a bypass permission and commands that can be executed on detection.

## Anti Spam
The antispam system is quite simple, all it does is adding a "cooldown" to chatting. By default you can only chat every 3 seconds.

Like other protection systems, the anticaps system also has a bypass permission and commands that can be executed on detection.

## Anti Swear
The antiswear system can be configured with the following options:
- `cancel`: if this is set to false, BungeeUtilisalsX will replace the swear word with the `replace` option, otherwise the message will be cancelled.
- `replace`: the characters that should be used to replace a swear word.
- `words`: a list of words that should be blocked by the anti swear
- `patterns`: a list of patterns that should be blocked by the anti swear (these can be made more advanced), each pattern can also whitelist a set of words that shouldn't be blocked.

Like other protection systems, the anticaps system also has a bypass permission and commands that can be executed on detection.