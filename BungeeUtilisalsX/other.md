# ServerGroups
[Click here to see the default servergroups.yml file](https://github.com/dieterblancke/BungeeUtilisalsX/blob/master/common/src/main/resources/servergroups.yml)

This configuration file allows you to create custom server groups. <br />
For example, if you have 2 lobbies, you can group them together in this file as following:

```yml
groups:
  - name: 'Lobbies'
    servers:
      - 'Lobby*'
```
Throughout all BungeeUtilisalsX configuration files, you will be able to use the servergroup 'Lobbies' (for example to send an announcement only to lobbies).

## Dynamic ServerGroups
In case you use some kind of "cloud" system, or any other system that adds servers dynamically (like CloudNet), you should set the "dynamic" option to true, for example:

```yml
groups:
  - name: 'Lobbies'
    dynamic: true
    servers:
      - 'Lobby*'
```

If you don't do this, BungeeUtilisalsX may not know about newer servers that were added on the fly.