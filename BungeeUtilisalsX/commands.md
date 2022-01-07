# Commands

All commands in this list can be enabled / disabled or changed. Each (sub)command name, alias, permission, ... can be changed to your liking.
Each message can also be changed as you please!

The most obvious commands don't have screenshots included in order to limit the amount of images,
you can also test everything on my test server: test.dieterblancke.xyz!
* ( argument ) stands for a required argument
* [ argument ] stands for an optional argument
* < argument > stands for a required argument based on a configuration variable

## Table of Contents
- [/bungeeutilisals](#bungeeutilisals)
- [/bungeeutilisals help](#bungeeutilisals-help)
- [/bungeeutilisals version](#bungeeutilisals-version)
- [/bungeeutilisals reload](#bungeeutilisals-reload)
- [/server](#server)
- [/announce](#announce)
- [/find](#find)
- [/glag](#glag)
- [/clearchat](#clearchat)
- [/bhelpop](#bhelpop)
- [/ping](#ping)
- [/language](#language)
- [/glist](#glist)
- [/shout](#shout)
- [/socialspy](#socialspy)
- [/commandspy](#commandspy)
- [/msg](#msg)
- [/reply](#reply)
- [/ignore](#ignore)
- [/msgtoggle](#msgtoggle)
- [/report](#report)
- [/report help](#report-help)
- [/report create](#report-create)
- [/report list](#report-list)
- [/report accept](#report-accept)
- [/report deny](#report-deny)
- [/report history](#report-history)
- [/chatlock](#chatlock)
- [/staffchat](#staffchat)
- [/domains](#domains)
- [/domains help](#domains-help)
- [/domains list](#domains-list)
- [/domains search](#domains-search)
- [/staffannouncement](#staffannouncement)
- [/offlinemessage](#offlinemessage)
- [/opengui](#opengui)
- [/friends](#friends)
- [/friends help](#friends-help)
- [/friends add](#friends-add)
- [/friends accept](#friends-accept)
- [/friends deny](#friends-deny)
- [/friends removerequest](#friends-removerequest)
- [/friends remove](#friends-remove)
- [/friends list](#friends-list)
- [/friends requests](#friends-requests)
- [/friends msg](#friends-msg)
- [/friends reply](#friends-reply)
- [/friends settings](#friends-settings)
- [/friends broadcast](#friends-broadcast)
- [/party](#party)
- [/party help](#party-help)
- [/party create](#party-create)
- [/party invite](#party-invite)
- [/party accept](#party-accept)
- [/party leave](#party-leave)
- [/party chat](#party-chat)
- [/party setowner](#party-setowner)
- [/party kick](#party-kick)
- [/party warp](#party-warp)
- [/party list](#party-list)
- [/party setrole](#party-setrole)
- [/party disband](#party-disband)
- [/party info](#party-info)
- [/ban](#ban)
- [/ipban](#ipban)
- [/tempban](#tempban)
- [/iptempban](#iptempban)
- [/mute](#mute)
- [/ipmute](#ipmute)
- [/tempmute](#tempmute)
- [/iptempmute](#iptempmute)
- [/kick](#kick)
- [/warn](#warn)
- [/unban](#unban)
- [/unbanip](#unbanip)
- [/unmute](#unmute)
- [/unmuteip](#unmuteip)
- [/punishmentinfo](#punishmentinfo)
- [/punishmenthistory](#punishmenthistory)
- [/punishmentdata](#punishmentdata)
- [/checkip](#checkip)
- [/staffhistory](#staffhistory)
- [/trackpunish](#trackpunish)
- [/staffrollback](#staffrollback)

## /bungeeutilisals

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /bungeeutilisals | /bux, /bu, /bungeeutilisalsx | bungeeutilisals.commands.admin |

**Usage:** /bungeeutilisals

**Description:** The default / admin command to help manage the plugin.

### /bungeeutilisals help

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /bungeeutilisals help |  | null |

**Usage:** /helpsub help

**Description:** Displays help information for the helpsubcommand

### /bungeeutilisals version

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /bungeeutilisals version |  | bungeeutilisals.commands.admin.version |

**Usage:** /bungeeutilisals version

**Description:** Prints the current BungeeUtilisalsX version in your chat.

### /bungeeutilisals reload

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /bungeeutilisals reload |  | bungeeutilisals.commands.admin.reload |

**Usage:** /bungeeutilisals reload

**Description:** Reloads all configuration files and most systems of BungeeUtilisalsX.

## /server

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /server | /switch | bungeeutilisals.commands.server |

**Usage:** /server [user] (serverName)

**Description:** Allows you to switch yourself, or someone else, to another server.

## /announce

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /announce | /alert, /bigalert | bungeeutilisals.commands.announce |

**Usage:** /announce (p/b/c/a/t) (message)

**Description:** Announces a message globally (similarly to alert). This can be done over chat, title, actionbar and bossbar.
Title and subtitles can be split using %sub%.
If a default type is set up in the config, a type can still be overridden by using type:(types) as first parameter.
Types can be concatinated, for example 'bcat' will announce bossbar, chat, actionbar and title at the same time.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/tbDWLQs.png" alt="/announce images"/>
	<img src="https://i.imgur.com/owmvMA7.png" alt="/announce images"/>
	<img src="https://i.imgur.com/aN250KS.png" alt="/announce images"/>
</div>

## /find

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /find | /search | bungeeutilisals.commands.find |

**Usage:** /find (user)

**Description:** Finds the server the given user currently is in.

## /glag

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /glag | /bgc, /blag | bungeeutilisals.commands.glag |

**Usage:** /glag

**Description:** Gives you some basic information about the current proxy (online time and memory usage).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/XNnxrqq.png" alt="/glag images"/>
</div>

## /clearchat

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /clearchat | /cc | bungeeutilisals.commands.clearchat |

**Usage:** /clearchat (server / ALL)

**Description:** Clears the chat globally or in a specfic server.

## /bhelpop

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /bhelpop | /ghelpop | bungeeutilisals.commands.helpop |

**Usage:** /helpop [reply] (message)

**Description:** Sends a helpop message to the online staff. Staff can reply using /helpop reply (user) (message).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/YAxhwzb.png" alt="/bhelpop images"/>
</div>

## /ping

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /ping | /gping, /bping | bungeeutilisals.commands.ping |

**Usage:** /ping [user]

**Description:** Shows your (or someone else's) current ping towards the current proxy.

## /language

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /language | /lang | bungeeutilisals.commands.language |

**Usage:** /language (language)

**Description:** Changes your current language.

## /glist

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /glist | /blist, /globallist | bungeeutilisals.commands.glist |

**Usage:** /glist

**Description:** Lists the players online on each server in a very configurable way, with multi proxy support.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/A8HjCM3.png" alt="/glist images"/>
	<img src="https://i.imgur.com/mBoXqyY.png" alt="/glist images"/>
</div>

## /shout

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /shout | /sh | bungeeutilisals.commands.shout |

**Usage:** /shout (message)

**Description:** Sends a global shout. This is a simplified version of /announce that can be used as a donator perk. Staff can have a custom shout format.

## /socialspy

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /socialspy | /ss, /sspy | bungeeutilisals.commands.socialspy |

**Usage:** /socialspy

**Description:** Toggles social spy for the current session. This will allow you to see all private messages that are being sent.

## /commandspy

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /commandspy | /cs, /cspy | bungeeutilisals.commands.commandspy |

**Usage:** /commandspy

**Description:** Toggles command spy for the current session. This will allow you to see all commands that are being executed.

## /msg

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /msg | /m, /whisper | bungeeutilisals.commands.msg |

**Usage:** /msg (user) (message)

**Description:** Sends a private message to a user.

## /reply

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /reply | /r | bungeeutilisals.commands.reply |

**Usage:** /reply (message)

**Description:** Sends a reply to the user you lastly interacted privately with.

## /ignore

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /ignore | /bignore | bungeeutilisals.commands.ignore |

**Usage:** /ignore (add/remove/list) [user]

**Description:** Ignores private messages and friend requests from a user.

## /msgtoggle

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /msgtoggle | /msgt | bungeeutilisals.commands.msgtoggle |

**Usage:** /msgtoggle

**Description:** Allows you to toggle private messages for the current session (will re-enable on rejoin).

## /report

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /report | /greport, /breport | bungeeutilisals.commands.report |

**Usage:** /report

**Description:** This command sends a list of available report commands.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/Yj3Hh7z.png" alt="/report images"/>
</div>

### /report help

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /report help |  | null |

**Usage:** /helpsub help

**Description:** Displays help information for the helpsubcommand

### /report create

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /report create | /report new, /report c | bungeeutilisals.commands.report.create |

**Usage:** /report create (user) (reason)

**Description:** Creates a new report against a user with a given description.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/7ULcefN.png" alt="/report create images"/>
</div>

### /report list

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /report list | /report list, /report l | bungeeutilisals.commands.report.list |

**Usage:** /report list [all / denied / accepted / active] [page]

**Description:** Lists all active reports or all reports of a given type.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/QfiOSoN.png" alt="/report list images"/>
	<img src="https://i.imgur.com/G1McUUc.png" alt="/report list images"/>
</div>

### /report accept

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /report accept |  | bungeeutilisals.commands.report.accept |

**Usage:** /report accept (id)

**Description:** Accepts a report with a given id. This will notify the reporter.

### /report deny

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /report deny |  | bungeeutilisals.commands.report.deny |

**Usage:** /report deny (id)

**Description:** Denies a report with a given id.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/0FT1oo8.png" alt="/report deny images"/>
</div>

### /report history

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /report history | /report hist | bungeeutilisals.commands.report.history |

**Usage:** /reports history [page]

**Description:** Lists all reports you have created in the past.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/xhVmfxv.png" alt="/report history images"/>
</div>

## /chatlock

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /chatlock | /cl, /lock, /lockchat | bungeeutilisals.commands.chatlock |

**Usage:** /chatlock (server / ALL)

**Description:** Locks the chat globally or in a specfic server.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/hCoX27y.png" alt="/chatlock images"/>
</div>

## /staffchat

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /staffchat | /sc, /schat | bungeeutilisals.commands.staffchat |

**Usage:** /staffchat [message]

**Description:** Toggles your chat mode into staff chat mode, only people with a given permission can then see your messages.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/cFxsm2L.png" alt="/staffchat images"/>
</div>

## /domains

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /domains | /domainlist | bungeeutilisals.commands.domains |

**Usage:** /domains

**Description:** This command allows you to see on what domains users first joined. This might not work when behind another proxy.

### /domains help

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /domains help |  | null |

**Usage:** /helpsub help

**Description:** Displays help information for the helpsubcommand

### /domains list

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /domains list | /domains ls, /domains all | bungeeutilisals.commands.domains.list |

**Usage:** /domains list

**Description:** Lists all domains that have been used to join your network. This can also show how many people joined on the domain in total and how many are online right now.

### /domains search

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /domains search | /domains find, /domains select | bungeeutilisals.commands.domains.search |

**Usage:** /domains search (input)

**Description:** Searches domain details for one specific domain, this works similar to /domains list, but instead of all domains it only shows domains that match your input.

## /staffannouncement

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /staffannouncement | /sa, /staffannounce | bungeeutilisals.commands.staffannouncement.send |

**Usage:** /staffannouncement (message)

**Description:** Sends an announcement only to people that have a specific permission.

## /offlinemessage

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /offlinemessage | /omsg | bungeeutilisals.commands.offlinemessage |

**Usage:** /offlinemessage (user) (message)

**Description:** Sends an offline private message to a user.

## /opengui

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /opengui | /og | bungeeutilisals.commands.opengui |

**Usage:** /opengui (gui) [args] [-u=USER]

**Description:** Opens a given gui for yourself or another user, for another user, you need this permission: COMMANDPERMISSION.parameters.-u!
For example: /opengui custom test will open a custom GUI named from the gui/custom/test.yml file.


## /friends

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends | /friend, /bfriends | bungeeutilisals.friends |

**Usage:** /friends

**Description:** This command either sends a list of available friends commands, or it opens a GUI.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/QIZxT2v.png" alt="/friends images"/>
	<img src="https://i.imgur.com/Fq4skEB.png" alt="/friends images"/>
</div>

### /friends help

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends help |  | null |

**Usage:** /helpsub help

**Description:** Displays help information for the helpsubcommand

### /friends add

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends add | /friends send, /friends request | bungeeutilisals.friends.add |

**Usage:** /friend add (user)

**Description:** Adds a friend to your friends list. If this user has an outstanding friend request towards you, this request will be accepted.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/RvtnG0o.png" alt="/friends add images"/>
	<img src="https://i.imgur.com/UpClGJH.png" alt="/friends add images"/>
</div>

### /friends accept

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends accept | /friends approve | bungeeutilisals.friends.accept |

**Usage:** /friend accept (user)

**Description:** Accepts an outstanding incoming friend request.

### /friends deny

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends deny |  | bungeeutilisals.friends.deny |

**Usage:** /friend deny (user)

**Description:** Denies an incoming friend request.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/4mn5TLY.png" alt="/friends deny images"/>
	<img src="https://i.imgur.com/hz5CB2Q.png" alt="/friends deny images"/>
</div>

### /friends removerequest

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends removerequest | /friends rr | bungeeutilisals.friends.removerequest |

**Usage:** /friend removerequest (user)

**Description:** Removes an outstanding friend request from / towards a certain user.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/kvf7tLF.png" alt="/friends removerequest images"/>
	<img src="https://i.imgur.com/qHREX5n.png" alt="/friends removerequest images"/>
</div>

### /friends remove

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends remove | /friends delete, /friends del | bungeeutilisals.friends.remove |

**Usage:** /friend remove (user)

**Description:** Removes a friend from your friends list. If this user has an outstanding friend request towards you, this request will be denied.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/ZTlZlEN.png" alt="/friends remove images"/>
	<img src="https://i.imgur.com/wTtYthk.png" alt="/friends remove images"/>
</div>

### /friends list

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends list | /friends fl | bungeeutilisals.friends.list |

**Usage:** /friend list [page]

**Description:** Lists your current friends.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/MUKiy9p.png" alt="/friends list images"/>
</div>

### /friends requests

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends requests | /friends req | bungeeutilisals.friends.requests |

**Usage:** /friend requests (in / out) [page]

**Description:** Lists all friend requests for a certain type (incoming / outgoing)

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/aNGKILf.png" alt="/friends requests images"/>
	<img src="https://i.imgur.com/4j4pUke.png" alt="/friends requests images"/>
</div>

### /friends msg

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends msg | /friends m, /friends tell, /friends w, /friends whisper, /friends message | bungeeutilisals.friends.msg |

**Usage:** /friend msg (user)

**Description:** Allows you to privately message a friend.

### /friends reply

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends reply | /friends r | bungeeutilisals.friends.reply |

**Usage:** /friend reply (message)

**Description:** Allows you to reply to a friend that messaged you earlier.

### /friends settings

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends settings |  | bungeeutilisals.friends.settings |

**Usage:** /friend settings [setting] [value]

**Description:** Updates a setting value for one of the existing setting types.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/jjUlGbb.png" alt="/friends settings images"/>
</div>

### /friends broadcast

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /friends broadcast |  | bungeeutilisals.friends.broadcast |

**Usage:** /friend broadcast (message)

**Description:** Broadcasts a message to all your online friends.

## /party

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party | /party, /bparty | bungeeutilisalsx.party |

**Usage:** /party

**Description:** This command either sends a list of available party commands, or it opens a GUI.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/OAJphyK.png" alt="/party images"/>
	<img src="https://i.imgur.com/ujwwBvA.png" alt="/party images"/>
	<img src="https://i.imgur.com/ej1Stkk.png" alt="/party images"/>
	<img src="https://i.imgur.com/o5ooNOm.png" alt="/party images"/>
	<img src="https://i.imgur.com/bViNz8e.png" alt="/party images"/>
	<img src="https://i.imgur.com/EcnDQJ4.png" alt="/party images"/>
	<img src="https://i.imgur.com/hKyOH1G.png" alt="/party images"/>
</div>

### /party help

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party help |  | null |

**Usage:** /helpsub help

**Description:** Displays help information for the helpsubcommand

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/KBzmNcr.png" alt="/party help images"/>
</div>

### /party create

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party create | /party make, /party new | bungeeutilisalsx.party.create |

**Usage:** /party create

**Description:** Creates a new party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/mhCdwLF.png" alt="/party create images"/>
</div>

### /party invite

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party invite | /party invite, /party add | bungeeutilisalsx.party.invite |

**Usage:** /party invite (user)

**Description:** Invites someone to your current party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/tVm5nnW.png" alt="/party invite images"/>
	<img src="https://i.imgur.com/hjhE72y.png" alt="/party invite images"/>
</div>

### /party accept

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party accept | /party join | bungeeutilisalsx.party.accept |

**Usage:** /party accept (user)

**Description:** Accepts the party invite from a certain user.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/ZfnYcv7.png" alt="/party accept images"/>
	<img src="https://i.imgur.com/2SKBtDf.png" alt="/party accept images"/>
</div>

### /party leave

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party leave | /party quit | bungeeutilisalsx.party.leave |

**Usage:** /party leave

**Description:** Leaves your current party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/QG1B0sc.png" alt="/party leave images"/>
	<img src="https://i.imgur.com/ArKod08.png" alt="/party leave images"/>
</div>

### /party chat

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party chat | /party c | bungeeutilisalsx.party.chat |

**Usage:** /party chat [message]

**Description:** Toggles party chat mode or sends a chat message to the party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/o79mBKC.png" alt="/party chat images"/>
</div>

### /party setowner

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party setowner | /party owner | bungeeutilisalsx.party.setowner |

**Usage:** /party setowner (user)

**Description:** Changes the owner of the party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/SlR9W0O.png" alt="/party setowner images"/>
</div>

### /party kick

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party kick | /party remove | bungeeutilisalsx.party.kick |

**Usage:** /party kick (user)

**Description:** Kicks a member from the party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/a2HeVfX.png" alt="/party kick images"/>
	<img src="https://i.imgur.com/f9BgEgD.png" alt="/party kick images"/>
	<img src="https://i.imgur.com/IaY8Kex.png" alt="/party kick images"/>
</div>

### /party warp

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party warp | /party tphere | bungeeutilisalsx.party.warp |

**Usage:** /party warp [user]

**Description:** Warps all party members to your current server.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/5TI2n5B.png" alt="/party warp images"/>
	<img src="https://i.imgur.com/PvMSQzd.png" alt="/party warp images"/>
	<img src="https://i.imgur.com/v59Xamv.png" alt="/party warp images"/>
</div>

### /party list

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party list | /party l | bungeeutilisalsx.party.list |

**Usage:** /party list (members / invites / requests) [page]

**Description:** Shows a list of members, invites or requests of your current party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/flRb6Lf.png" alt="/party list images"/>
</div>

### /party setrole

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party setrole | /party sr | bungeeutilisalsx.party.setrole |

**Usage:** /party setrole (user) (role)

**Description:** Warps all party members to your current server.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/vPskkS5.png" alt="/party setrole images"/>
</div>

### /party disband

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party disband | /party dispose | bungeeutilisalsx.party.disband |

**Usage:** /party disband

**Description:** Disbands the party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/bnYd101.png" alt="/party disband images"/>
	<img src="https://i.imgur.com/W8MN0yn.png" alt="/party disband images"/>
</div>

### /party info

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /party info | /party stats | bungeeutilisalsx.party.info |

**Usage:** /party info

**Description:** Shows basic information about your current party.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/z8sJBSr.png" alt="/party info images"/>
</div>

## /ban

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /ban | /pban, /gban | bungeeutilisals.punishments.ban |

**Usage:** /ban (user) <server> (reason)

**Description:** Permanently bans a given user from the network (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/Xh9CDWd.png" alt="/ban images"/>
	<img src="https://i.imgur.com/qpdlTAd.png" alt="/ban images"/>
</div>

## /ipban

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /ipban | /banip, /gbanip, /gipban | bungeeutilisals.punishments.ipban |

**Usage:** /ipban (user / ip) <server> (reason)

**Description:** Permanently ipbans a given user from the network (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/QnBWURl.png" alt="/ipban images"/>
</div>

## /tempban

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /tempban | /tban, /gtban | bungeeutilisals.punishments.tempban |

**Usage:** /tempban (user) (time) <server> (reason)

**Description:** Temporarily bans a given user from the network (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/OKqe23Q.png" alt="/tempban images"/>
	<img src="https://i.imgur.com/AWui1nz.png" alt="/tempban images"/>
</div>

## /iptempban

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /iptempban | /iptempban, /tipban, /gtipban, /tbanip | bungeeutilisals.punishments.tempbanip |

**Usage:** /iptempban (user / ip) (time) <server> (reason)

**Description:** Temporarily ipbans a given user from the network (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/LFejfJE.png" alt="/iptempban images"/>
</div>

## /mute

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /mute | /pmute, /gmute | bungeeutilisals.punishments.mute |

**Usage:** /mute (user) <server> (reason)

**Description:** Permanently bans a given user globally (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/5iT5Mun.png" alt="/mute images"/>
	<img src="https://i.imgur.com/nRJEXFk.png" alt="/mute images"/>
</div>

## /ipmute

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /ipmute | /muteip, /gmuteip, /gipmute | bungeeutilisals.punishments.ipmute |

**Usage:** /ipmute (user / ip) <server> (reason)

**Description:** Permanently ip mutes a given user globally (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/YrMU7wO.png" alt="/ipmute images"/>
</div>

## /tempmute

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /tempmute | /tmute, /gtmute | bungeeutilisals.punishments.tempmute |

**Usage:** /tempmute (user) (time) <server> (reason)

**Description:** Temporarily mutes a given user globally (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/JKe2UrJ.png" alt="/tempmute images"/>
	<img src="https://i.imgur.com/MyOUwXn.png" alt="/tempmute images"/>
</div>

## /iptempmute

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /iptempmute | /iptempmute, /tipmute, /gtipmute, /tmuteip | bungeeutilisals.punishments.tempmuteip |

**Usage:** /iptempmute (user / ip) (time) <server> (reason)

**Description:** Temporarily ipmutes a given user globally (or given server if per-server punishments are enabled).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/Yd91BxV.png" alt="/iptempmute images"/>
</div>

## /kick

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /kick |  | bungeeutilisals.punishments.kick |

**Usage:** /kick (user) <server> (reason)

**Description:** Kicks a user for a given reason.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/NiTAjXg.png" alt="/kick images"/>
	<img src="https://i.imgur.com/ZQLk50n.png" alt="/kick images"/>
</div>

## /warn

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /warn |  | bungeeutilisals.punishments.warn |

**Usage:** /warn (user) <server> (reason)

**Description:** Warns a user for a given reason.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/4SXzSG4.png" alt="/warn images"/>
	<img src="https://i.imgur.com/d2faosi.png" alt="/warn images"/>
</div>

## /unban

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /unban | /punban, /gunban, /unsetban, /removeban | bungeeutilisals.punishments.unban |

**Usage:** /unban (user) <server>

**Description:** Removes a ban for a given user.

## /unbanip

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /unbanip | /punbanip, /gunbanip, /unsetbanip, /removebanip | bungeeutilisals.punishments.unbanip |

**Usage:** /unbanip (user / IP) <server>

**Description:** Removes an IP ban for a given user / IP.

## /unmute

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /unmute | /punmute, /gunmute, /unsetmute, /removemute | bungeeutilisals.punishments.unmute |

**Usage:** /unmute (user) <server>

**Description:** Removes a mute for a given user.

## /unmuteip

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /unmuteip | /punmuteip, /gunmuteip, /unsetmuteip, /removemuteip | bungeeutilisals.punishments.unmuteip |

**Usage:** /unmuteip (user / IP) <server>

**Description:** Removes an IP mute for a given user / IP.

## /punishmentinfo

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /punishmentinfo | /pinfo | bungeeutilisals.punishments.punishmentinfo |

**Usage:** /punishmentinfo (user) <server> [type / all]

**Description:** Shows you the current status for a specific punishment type or all punishment types for a specific user.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/BUqYtSI.png" alt="/punishmentinfo images"/>
</div>

## /punishmenthistory

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /punishmenthistory | /phistory | bungeeutilisals.punishments.punishmenthistory |

**Usage:** /punishmenthistory (user) [type / all] [page]

**Description:** Shows you the punishment history for a specific user.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/QxMdfY0.png" alt="/punishmenthistory images"/>
</div>

## /punishmentdata

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /punishmentdata | /pdata | bungeeutilisals.punishments.punishmentdata |

**Usage:** /punishmentdata (type) (id)

**Description:** Shows you data for a specific punishment type and id.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/TwjOTut.png" alt="/punishmentdata images"/>
</div>

## /checkip

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /checkip | /dupeip, /checkalts | bungeeutilisals.punishments.checkip |

**Usage:** /checkip (user / ip)

**Description:** Checks the accounts on a given IP and their current ban status.

## /staffhistory

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /staffhistory | /shistory | bungeeutilisals.punishments.staffhistory |

**Usage:** /staffhistory (user) [type / all] [page]

**Description:** Shows you a list of punishments executed by this specific user.

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/ch3xmq8.png" alt="/staffhistory images"/>
</div>

## /trackpunish

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /trackpunish | /pt, /punishtrack, /trackpunishment | bungeeutilisals.punishments.trackpunish |

**Usage:** /trackpunish (user) (reason)

**Description:** Executes a track punishment for a specific user. Track punishments can be very useful for laying out a set punishment path for certain rule breakings.

## /staffrollback

| Command | Default Aliases | Permission |
| --- | --- | --- |
| /staffrollback | /srollback | bungeeutilisals.punishments.staffrollback |

**Usage:** /staffrollback (user) (time) [-f]

**Description:** Performs a rollback of punishments executed since the given time. If the -f parameter is given, the rollback will be a hard rollback (permanently deleted).

**Images:**

<div class="imagelist">
	<img src="https://i.imgur.com/q5zheYO.png" alt="/staffrollback images"/>
</div>

