# GUI System

## This page is still a work in progress

For the GUI system to work, you need to have the plugin
"[Protocolize](https://www.spigotmc.org/resources/protocolize-protocollib-for-bungeecord-waterfall-velocity.63778/)"
installed.

## Slots
WIP

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