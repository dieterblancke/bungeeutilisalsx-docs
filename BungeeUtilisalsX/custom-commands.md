# Custom Commands
Not only does BungeeUtilisalsX have a lot of commands, it also allows you to create your own commands!

These commands can go from very simple messages you want to send to more advanced commands with hover and click events.

Below you can find an example of a very basic "vote" command with no permissions:
```yaml
commands:
  - name: 'vote'
    messages:
      text: '&eYou can find our vote links at &bwww.example.com/vote&e!'
```
Once you reload BungeeUtilisals using `/bu reload`, you will be able to use `/vote`.
Running this command, you will get the message `&eYou can find our vote links at &bwww.example.com/vote&e!`, as configured!

With the custom commands system, you can:
- create commands with name and aliases
- send messages on command execute
  * these messages can be made hoverable
  * these messages can be made clickable
  * these messages support placeholders
- execute other commands (by console) on command execute

Check out the default custom commands [here](https://github.com/dieterblancke/BungeeUtilisalsX/blob/master/common/src/main/resources/commands/customcommands.yml)!
You can test these commands yourself by joining **test.dieterblancke.xyz**!

# Alias commands
Custom commands can also be made as an alias for other commands, for example:
```yaml
commands:
  - name: 'vote'
    aliases:
      - 'testvote'
      - 'votetest'
    alias-for: 'examplevotecommand'
```