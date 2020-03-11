# Commands

# Legenda
- ( argument ) = a required argument
- [ argument ] = an optional argument

# General Commands
## /bungeeutilisals
**Usage:** /bungeeutilisals<br>
**Aliases:** /bu, /butili, /butilisals <br>
**Permission:** bungeeutilisals.admin <br>

### /bungeeutilisals version
**Permission:** bungeeutilisals.admin.version <br>
Shows you the version you are currently running on.

### /bungeeutilisals reload
**Permission:** bungeeutilisals.admin.reload <br>
Reloads the plugin

### /bungeeutilisals dump
**Permission:** bungeeutilisals.admin.dump <br>

Creates a dump on https://paste.dbsoftwares.eu with information that can be useful for an issue.

### /bungeeutilisals convert (oldtype) [properties]
**Permission:** bungeeutilisals.admin.convert <br>
Allows you to convert plugin data when you switch storage type.

Example: /bungeeutilisals convert MYSQL host:127.0.0.1,port:3306,database:bu_old,username:bungeeutilisals,password:test <br>
This example will convert from MySQL (with the given properties) to the current storage implementation.

### /bungeeutilisals import (plugin) [properties]
**Permission:** bungeeutilisals.admin.import <br>
Allows you to import plugin data when you switch storage type. <br>
**Supported plugins:** BungeeUtilisals (old version), BungeeAdminTools

Example: /bungeeutilisals import BAT host:127.0.0.1,port:3306,database:bu_old,username:bungeeutilisals,password:test <br>
This example will import data from BungeeAdminTools (with the given properties) to the current storage implementation.

## /glist
This is a customizable alternative for the default /glist command, with redis support. **Note:** Make sure to remove the glist module.

**Usage:** /glist <br>
**Aliases:** /blist, /globallist <br>
**Default Permission:** bungeeutilisals.commands.glist <br>

## /announce (p/b/c/a/t) (message)
This is an 'upgraded' alternative for the default /alert command, as this allows you to broadcast a chat, title, bossbar and / or actionbar message throughout your server.

**Types explanation:**
- p: preconfigured, this is the path to the preconfigured message in the languages file (this also allows an alert to be multilingual), by default, */announce p welcome* should work
- c: chat
- t: title, to split a title into a title and subtitle you can use %sub%, so for example: &c&lBungeeUtilisalsX %sub%&eThank you for using our plugin!
- b: bossbar
- a: actionbar

**Usage:** /announce (p/b/c/a/t) (message) <br>
**Aliases:** /blist, /globallist <br>
**Default Permission:** bungeeutilisals.commands.glist <br>

## /find (user)
This is a customizable alternative for the default /find command, with redis support. **Note:** Make sure to remove the find module.

**Usage:** /find (user) <br>
**Aliases:** /search <br>
**Default Permission:** bungeeutilisals.commands.find <br>

## /server (server)
This is a customizable alternative for the default /server command. **Note:** Make sure to remove the server module.

**Usage:** /server (server) <br>
**Aliases:** /switch <br>
**Default Permission:** bungeeutilisals.commands.server <br>

## /clearchat (local / global)
This command allows you to clear the chat of the entire network, or of the server you are in.

**Usage:** /clearchat (local / global) <br>
**Aliases:** /cc <br>
**Default Permission:** bungeeutilisals.commands.clearchat <br>

## /chatlock (local / global)
This command allows you to lock the chat of the entire network, or of the server you are in.

**Usage:** /chatlock (local / global) <br>
**Aliases:** /cl, /lock, /lockchat <br>
**Default Permission:** bungeeutilisals.commands.chatlock <br>
**Default Bypass Permission:** bungeeutilisals.chatlock.bypass <br>

## /glag
This command shows you basic statistics of your server, such as tps, max, free and total memory and last startup timestamp.

**Usage:** /glag <br>
**Aliases:** /bgc, /blag <br>
**Default Permission:** bungeeutilisals.commands.glag <br>

## /staffchat
This command allows staff to communicate with eachother in a separate staff chat.

**Usage:** /staffchat <br>
**Aliases:** /sc, /schat <br>
**Default Permission:** bungeeutilisals.commands.staffchat <br>

## /language (language)
This command allows people to change their language to one of the languages supported by the plugin.

**Usage:** /language (language) <br>
**Aliases:** /lang <br>
**Default Permission:** bungeeutilisals.commands.language <br>

## /staff
This command shows the online staff per role. These roles can be installed in the commands/generalcommands.yml file.

**Usage:** /staff <br>
**Aliases:** /onlinestaff <br>
**Default Permission:** bungeeutilisals.commands.staff <br>

## /msg (user) (message)
This command allows you to send a PM to anyone who is online in the network (redis supported) (target must ofcourse not have ignored you).

**Usage:** /msg (user) (message) <br>
**Aliases:** /m, /whisper <br>
**Default Permission:** bungeeutilisals.commands.msg <br>

## /reply (message)
This command allows you to reply to the last person who sent you a PM.

**Usage:** /reply (message) <br>
**Aliases:** /r <br>
**Default Permission:** bungeeutilisals.commands.reply <br>

## /ignore (add / remove / list) [user]
This command allows you to add / remove someone to / from your ignored members list. Or it lists the people you are ignoring.

**Usage:** /ignore (add / remove / list) [user] <br>
**Aliases:** /bignore <br>
**Default Permission:** bungeeutilisals.commands.ignore <br>

## /socialspy
This command allows you to see private messages (/msg & /reply commands).

**Usage:** /socialspy <br>
**Aliases:** /ss, /sspy <br>
**Default Permission:** bungeeutilisals.commands.socialspy <br>

## /commandspy
This command allows you to see commands people execute (ignored commands can be setup).

**Usage:** /commandspy <br>
**Aliases:** /cs, /cspy <br>
**Default Permission:** bungeeutilisals.commands.commandspy <br>

## /ping [user]
Shows your ping, or the ping of another user towards the **BungeeCord**.

**Usage:** /ping [user] <br>
**Aliases:** /gping, /bping <br>
**Default Permission:** bungeeutilisals.commands.ping <br>
**Default Other Permission:** bungeeutilisals.commands.ping.other <br>

## /domains
**Aliases:** /domainlist
**Default Permission:** bungeeutilisals.commands.domains

### /domains list
Lists the domains that have been used to connect to your server with the amount of unique connections.

**Usage:** /domains list <br>
**Aliases:** /domains ls, /domains all <br>
**Default Permission:** bungeeutilisals.commands.domains.list <br>

### /domains list
Searches a domain in the list of domains that have been used to connect to your server. <br>
Only domains that contain the text you entered will be listed.

**Usage:** /domains search <br>
**Aliases:** /domains find, /domains select <br>
**Default Permission:** bungeeutilisals.commands.domains.search <br>

## /bhelpop (message) or /bhelpop reply (user) (message)
Helpop will message the online staff that have a permission to receive the message. <br>
Helpop reply will allow you to reply to this user (only if you have the reply permission).

**Usage:** /helpop (message) or /helpop reply (user) (message) <br>
**Aliases:** /ghelpop <br>
**Default Permission:** bungeeutilisals.commands.helpop <br>
**Default Receive Permission:** bungeeutilisals.commands.helpop.receive_broadcast <br>
**Default Reply Permission:** bungeeutilisals.commands.helpop.reply <br>

# Addon Commands
## /addon enable (name)
Enables an addon that has a JAR file present, but isn't enabled yet.

**Permission:** bungeeutilisals.admin.addons.enable

## /addon disable (name)
Disables an addon, but doesn't remove the files it has.

**Permission:** bungeeutilisals.admin.addons.disable

## /addon info (name)
Shows information about an addon.

**Permission:** bungeeutilisals.admin.addons.info

## /addon list
Shows all exising addons, and whether or not they are installed & enabled.

**Permission:** bungeeutilisals.admin.addons.list

## /addon install (addon)
Installs an addon from our web api, and enables it.

**Permission:** bungeeutilisals.admin.addons.install

## /addon uninstall (addon)
Uninstalls an addon (by removing the jar file) and disables it.

**Permission:** bungeeutilisals.admin.addons.uninstall

## /addon reload (addon)
Reloads an addon.

**Permission:** bungeeutilisals.admin.addons.reload

# Punishment Commands
Possible punishment formats:
- Year formats:
  + 1y
  + 1year
  + 2years
- Month formats:
  + 1mo
  + 1month
  + 2months
- Week formats:
  + 1w
  + 1week
  + 2weeks
- Day formats:
  + 1d
  + 1day
  + 2days
- Hour formats:
  + 1h
  + 1hour
  + 2hours
- Minute formats:
  + 1m
  + 1min
  + 2mins
- Second formats:
  + 1s
  + 1sec
  + 2secs

## /ban
This command permanently bans someone from the BungeeCord network.

**Usage:** /ban (user) (reason) <br>
**Per Server Usage:** /ban (user) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /pban, /gban <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /ban didjee2 test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /ban didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.ban <br>
**Default Broadcast permission:** bungeeutilisals.punishments.ban.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /ipban
This command permanently bans someone's ip from the BungeeCord network.

**Usage:** /ipban (user / IP) (reason) <br>
**Per Server Usage:** /ipban (user / IP) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /banip, /gbanip, /gipban <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /ipban didjee2 test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /ipban didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.ipban <br>
**Default Broadcast permission:** bungeeutilisals.punishments.ipban.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /tempban
This command temporarily bans someone from the BungeeCord network.

**Usage:** /tempban (user) (timeformat) (reason) <br>
**Per Server Usage:** /tempban (user) (timeformat) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /tban, /gtban <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /tempban didjee2 1d test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /tempban didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.tempban <br>
**Default Broadcast permission:** bungeeutilisals.punishments.tempban.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /iptempban
This command temporarily bans someone's ip from the BungeeCord network.

**Usage:** /iptempban (user / IP) (timeformat) (reason) <br>
**Per Server Usage:** /iptempban (user) (timeformat) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /iptempban, /tipban, /gtipban, /tbanip <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /iptempban didjee2 1d test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /iptempban didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.tempbanip <br>
**Default Broadcast permission:** bungeeutilisals.punishments.tempbanip.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /mute
This command permanently mutes someone from the BungeeCord network.

**Usage:** /mute (user) (reason) <br>
**Per Server Usage:** /mute (user) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /pmute, /gmute <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /mute didjee2 test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /mute didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.mute <br>
**Default Broadcast permission:** bungeeutilisals.punishments.mute.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /ipmute
This command permanently mutes someone's ip from the BungeeCord network.

**Usage:** /ipmute (user / IP) (reason) <br>
**Per Server Usage:** /ipmute (user / IP) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /muteip, /gmuteip, /gipmute <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /ipmute didjee2 test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /ipmute didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.ipmute <br>
**Default Broadcast permission:** bungeeutilisals.punishments.ipmute.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /tempmute
This command temporarily mutes someone from the BungeeCord network.

**Usage:** /tempmute (user) (timeformat) (reason) <br>
**Per Server Usage:** /tempmute (user) (timeformat) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /tmute, /gtmute <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /tempmute didjee2 1d test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /tempmute didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.tempmute <br>
**Default Broadcast permission:** bungeeutilisals.punishments.tempmute.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /iptempmute
This command temporarily mutes someone's ip from the BungeeCord network.

**Usage:** /iptempmute (user / IP) (timeformat) (reason) <br>
**Per Server Usage:** /iptempmute (user / IP) (timeformat) (server) (reason) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /iptempmute, /tipmute, /gtipmute, /tmuteip <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /iptempmute didjee2 1d test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /iptempmute didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.tempmuteip <br>
**Default Broadcast permission:** bungeeutilisals.punishments.tempmuteip.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /kick
This command kicks someone from the BungeeCord network.

**Usage:** /kick (user) (reason) <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /kick didjee2 test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /kick didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.kick <br>
**Default Broadcast permission:** bungeeutilisals.punishments.kick.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /warn
This command warns someone on the BungeeCord network.

**Usage:** /warn (user) (reason) <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /warn didjee2 test -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /warn didjee2 test -s

**Default Permission:** bungeeutilisals.punishments.warn <br>
**Default Broadcast permission:** bungeeutilisals.punishments.warn.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /unban
This command unbans someone from the BungeeCord network.

**Usage:** /unban (user) <br>
**Per Server Usage:** /unban (user) (server) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /punban, /gunban, /unsetban, /removeban <br>
**Parameters:**
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /unban didjee2 -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /unban didjee2 -s

**Default Permission:** bungeeutilisals.punishments.unban <br>
**Default Broadcast permission:** bungeeutilisals.punishments.unban.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /unbanip
This command unbans someone's ip from the BungeeCord network.

**Usage:** /unbanip (user / IP) <br>
**Per Server Usage:** /unbanip (user / IP) (server) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /punbanip, /gunbanip, /unsetbanip, /removebanip <br>
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /unbanip didjee2 -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /unbanip didjee2 -s

**Default Permission:** bungeeutilisals.punishments.unbanip <br>
**Default Broadcast permission:** bungeeutilisals.punishments.unbanip.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /unmute
This command unmutes someone from the BungeeCord network.

**Usage:** /unmute (user) 
**Per Server Usage:** /unmute (user) (server) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /punmute, /gunmute, /unsetmute, /removemute <br>
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /unmute didjee2 -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /unmute didjee2 -s

**Default Permission:** bungeeutilisals.punishments.unmute <br>
**Default Broadcast permission:** bungeeutilisals.punishments.unmute.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /unmuteip
This command unmutes someone's ip from the BungeeCord network.

**Usage:** /unmuteip (user / IP) <br>
**Per Server Usage:** /unmuteip (user / IP) (server) <small>| This will only work when per-server-punishments are enabled in the punishments config |</small><br>
**Aliases:** /punmuteip, /gunmuteip, /unsetmuteip, /removemuteip <br>
- -nbp, stands for nobroadcastpermission, this parameter will make it so the broadcast permission gets ignored (aka public punishment), example: /unmuteip didjee2 -nbp
- -s, stands for silent, this paramater will make it so no broadcast is sent, for example: /unmuteip didjee2 -s

**Default Permission:** bungeeutilisals.punishments.unmuteip <br>
**Default Broadcast permission:** bungeeutilisals.punishments.unmuteip.broadcast <br>

When someone has the default broadcast permission, they will get a message when someone gets punished.

## /punishmentinfo
This command shows info about the punishments a certain user currently has.

**Usage:** /punishmentinfo (user) [type / all] [page] <br>
**Aliases:** /pinfo <br>
**Default Permission:** bungeeutilisals.punishments.punishmentinfo <br>

## /punishmenthistory
This command shows info about the punishment history of a certain user.

**Usage:** /punishmenthistory (user) [type / all] [page] <br>
**Aliases:** /phistory <br>
**Default Permission:** bungeeutilisals.punishments.punishmenthistory <br>

## /punishmentdata
This command shows info about a certain punishment id.

**Usage:** /punishmentdata (type) (id) <br>
**Aliases:** /pdata <br>
**Default Permission:** bungeeutilisals.punishments.punishmentdata <br>

## /staffhistory
This command shows info about the punishments that have been **executed** by a certain user.

**Usage:** /staffhistory (user) [type / all] [page] <br>
**Aliases:** /shistory <br>
**Default Permission:** bungeeutilisals.punishments.staffhistory <br>

# Friend Commands
## /friend add (user)
Adds someone to your friend list.

**Usage:** /friend add (user) <br>
**Aliases:** /friends send, /friends request <br>
**Default Permission:** bungeeutilisals.friends.add <br>

## /friend remove (user)
Removes someone from your friend list.

**Usage:** /friend remove (user) <br>
**Aliases:** /friends delete, /friends del <br>
**Default Permission:** bungeeutilisals.friends.remove <br>

## /friend accept (user)
Accepts someone into your friend list.

**Usage:** /friend accept (user) <br>
**Aliases:** /friends approve <br>
**Default Permission:** bungeeutilisals.friends.accept <br>

## /friend deny (user)
Denies someone from your friend list.

**Usage:** /friend deny (user) <br>
**Default Permission:** bungeeutilisals.friends.deny <br>

## /friend removerequest (user)
Removes a request that you sent to someone.

**Usage:** /friend removerequest (user) <br>
**Aliases:** /friends rr <br>
**Default Permission:** bungeeutilisals.friends.removerequest <br>

## /friend list [page]
Lists the friends that you have.

**Usage:** /friend list [page] <br>
**Aliases:** /friends fl <br>
**Default Permission:** bungeeutilisals.friends.list <br>

## /friend requests (in / out) [page]
Lists the incoming and outgoing friend requests that you have.

**Usage:** /friend requests (in / out) [page] <br>
**Aliases:** /friends req <br>
**Default Permission:** bungeeutilisals.friends.requests <br>

## /friend msg (user) (message)
Sends a private message to someone in your friends list.

**Usage:** /friend msg (user) (message) <br>
**Aliases:** /friends m, /friends tell, /friends w, /friends whisper, /friends message <br>
**Default Permission:** bungeeutilisals.friends.msg <br>

## /friend reply (message)
Replies to a private message by / to a friend.

**Usage:** /friend reply (message) <br>
**Aliases:** /friends r <br>
**Default Permission:** bungeeutilisals.friends.reply <br>

## /friend settings (setting) (enable / disable)
Changes user preference for certain settings.

**Usage:** /friend settings (setting) (enable / disable) <br>
**Default Permission:** bungeeutilisals.friends.settings <br>

# Report Commands
## /report create (user) (reason)
Creates a report against a certain user.

**Usage:** /report create (user) (reason) <br>
**Aliases:** /report c, /report new <br>
**Default Permission:** bungeeutilisals.commands.report.create <br>

## /report list [all/active/accepted/denied] [page]
Lists the reports that are valid to the criteria (all, active, accepted or denied).

**Usage:** /report list [all/active/accepted/denied] [page] <br>
**Aliases:** /report list, /report l <br>
**Default Permission:** bungeeutilisals.commands.report.list <br>

## /report accept (id)
Accepts a report with a certain ID (the ID can be retrieved from /report list)

**Usage:** /report accept (id) <br>
**Default Permission:** bungeeutilisals.commands.report.accept <br>

## /report deny (id)
Denies a report with a certain ID (the ID can be retrieved from /report list)

**Usage:** /report deny (id) <br>
**Default Permission:** bungeeutilisals.commands.report.deny <br>

## /report history [page]
Shows your report history and the data of the report (and whether or not it was handled & accepted yet)

**Usage:** /report history [page] <br>
**Aliases:** /report hist <br>
**Default Permission:** bungeeutilisals.commands.report.history <br>