# Parties
The BungeeUtilisalsX party system is a (multi-)proxy party system.

This party system has been stress tested running with 4000 parties with 1000 members each without any issues.

**Note for multi proxy parties**: <br/>
The parties get stored in redis and if a new proxy starts up, existing parties will be loaded into local memory.

## Configuration
By default, the party system is disabled, to enable this, just put "enabled" to true in the party/config.yml file.

### Member limits
Each party can have their own member limit assigned. By default, this limit is 10 players per party.

There can also be member limits set up per permission, for example:
```yaml
member-limits:
  - permission: bungeeutilisalsx.party.limits.vip
    limit: 15
  - permission: bungeeutilisalsx.party.limits.mvp
    limit: 25
```
In this example, players with the vip permission will have 15 as a limit, players with the mvp permission will have 25 as the limit.

**Important Note**: <br/>
A party limit gets assigned to a party based on the initial party owner.
With other words, if the party gets created by someone with a party limit of 10, and he gives the party to someone with a party limit of 25,
the party will remain with a party limit of 10 (and vice-versa).

### Disabled warp servers
This is just a list of servers **from which** a player cannot be warped.
For example, if you have an offline mode server with login servers, you don't want people to be able to warp them out from there and bypassing the login.

### Inactivity period scan
When players leave the server, they are not automatically kicked from the party. This is handled by the inactivity scheduler task.

The task works as follows:
- If all members of a party are offline, the scheduler will mark the party as "inactive".
If the next time the task runs, all party members are still offline, the scheduler will automatically remove the party.
- If a specific member of a party is offline, the scheduler will mark that member as "inactive".
If the next time the task runs, this member is still offline, the scheduler will automatically remove this member from the party.

The duration between runs of the scheduler can be changed on both party and member level.
By default, it scans for inactive parties every minute while it doesn't scan for individual inactive members.

### Party roles
By default, there are 2 party roles present:
- MEMBER
- MODERATOR

Alongside these two roles, there is also the "OWNER" role, this role is not editable and has all party permissions.
The other, custom, roles can be given one of the following permissions:
- INVITE
- KICK
- WARP

Each role is also given a priority, when kicking someone from the party, you can only kick people with a priority **lower** than yours.
The party owner cannot be kicked by anyone but himself, if the party owner kicks himself it is essentially the same as changing the party owner.

### Allowing invites when you are already in a party
By default, you can still be invited when you are already in a party.
This means that, even if you are in a party, you can still be invited to another party.
If you accept an invite while already in a party, you will leave your current party and join the other party.

This behaviour can be disabled by setting `allow-invites-to-members-already-in-party` to false in the config.