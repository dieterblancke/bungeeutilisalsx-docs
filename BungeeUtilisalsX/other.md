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