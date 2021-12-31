# GUI System

## This page is still a work in progress

For the GUI system to work, you need to have the plugin
"[Protocolize](https://www.spigotmc.org/resources/protocolize-protocollib-for-bungeecord-waterfall-velocity.63778/)"
installed.

## Custom GUI's
Since v2.3.0, BungeeUtilisalsX supports custom GUI's. These are located in the gui/custom folder.
These guis can be opened by using `/opengui custom (GUINAME)`, for example `/opengui custom test` for the default GUI.

Custom GUI's support the general actions and placeholders from other guis.

## Slots
The GUI system supports different slot types to be entered:

- **Border Slots**: If the value of slots is set to 'borders', it will add the item to the top, side and bottom rows of the GUI.
- **Ranged Slots**: Slots can also be set up as a range, for example a slot range of 1 - 10 can be done as following: '1..10'.
- **Single Slots:** Slots can also be just single slots, like '1'.
- **Combining slots**: You can also combine any of these slots, like 'borders,10..20,25' will add the item to the border slots, slots 10-20 and slot 25.
Even if some of these slots overlap, the item will be 'overridden' and only be set once.

## Actions
The GUI system currently supports the following actions:
- **nothing**: as the name says, this action will just do nothing and keep the inventory opened.
- **close**: this action will close the inventory once clicked.
- **input**: this action will close the inventory and request the player to enter some text. 
The configuration for this action is different though, for example:
```yaml
    action:
      type: input
      languagePath: 'party.gui.kick-chat-input'
      action: execute:party kick {output}
```
- **open**: this action will open another inventory with the given arguments.
For example, to open the friends inventory you can use `action: open:friend`, and to open a custom GUI you can use `action: open:custom GUINAME`.
- **execute**: this action will let the player execute a command, for example `action: execute:hub`
- **Page Actions**: if the GUI is a paged GUI (such as friends, party, reports and punishments), the **previous-page** and **next-page** actions open the previous page or next page.

### Right Click Actions
These support the same actions as the default left click actions, but instead of for example: `action: open:friend`, you can use `right-action: open:friend`.

## Enchantments
Items can have multiple enchantments by adding an "enchants" section to the item.
A list of available enchantments can for example be found [here](https://www.digminecraft.com/lists/enchantment_list_pc.php).

An example enchanted item could be:
```yaml
  - slots: '53'
    item:
      # In 1.13 and higher, this should be RED_BED and the "data" key should be removed.
      material: BED
      data: 14
      name: '&c&lClose'
      enchants:
        # A list of enchantments can be found here: https://www.digminecraft.com/lists/enchantment_list_pc.php
        - enchantment: aqua_affinity
          level: 1
        - enchantment: unbreaking
          level: 2
    action: close
```