![](https://i.imgur.com/IZvmEY8.png)

# Inventory Rollback: Continued

[![Build Status](https://img.shields.io/jenkins/build?jobUrl=https%3A%2F%2Fci.sidpatchy.com%2Fjob%2FInventoryRollback-Continued%2F&style=flat-square)](https://ci.sidpatchy.com/job/InventoryRollback-Continued/)
[![License](https://img.shields.io/github/license/Sidpatchy/Inventory-Rollback?style=flat-square)](https://github.com/Sidpatchy/Inventory-Rollback/blob/master/LICENSE)
[![Commits Since Latest Release](https://img.shields.io/github/commits-since/Sidpatchy/InventoryRollback-Continued/latest?style=flat-square)](https://github.com/Sidpatchy/InventoryRollback-Continued/commits/master)
[![Latest Commit](https://img.shields.io/github/last-commit/Sidpatchy/InventoryRollback-Continued?style=flat-square)](https://github.com/Sidpatchy/InventoryRollback-Continued/commits/master)

### Minecraft Bukkit Plugin - Tested with versions 1.8.8 - 1.18

**Versions 1.5.3 and above require NBTAPI v2.9.0 or greater: https://www.spigotmc.org/resources/nbt-api.7939/**

This plugin logs players' inventory, health, hunger, experience, and ender chest during various events. Perfect if someone loses their gear because of an admin mishap or if a bad plugin accidentally wipes a players data for example! These logged events include:

* Player death
* Player joining the 
* Player disconnecting from the 
* Player changing worlds

Staff with the required permission can open a GUI and select the required backup for the player. They can then click and drag the items the player requires off the GUI so they can pick them up. Clicking on the other icons enables you to restore the other attributes if required directly to the player.  
  
By default, it will log 50 deaths and 10 joins, disconnects, world changes, and force saves each per player before the old data is purged to save space. These values can be changed in the config.  
  
**If upgrading a current server from before 1.13 you will need to delete all your backup data due to the changes with materials in later versions.**

## Downloads
* [Spigot](https://www.spigotmc.org/resources/inventory-rollback-continued.93436/)
* [CurseForge](https://dev.bukkit.org/projects/inventory-rollback-continued)
* [GitHub](https://github.com/Sidpatchy/InventoryRollback-Continued/releases)
* [Jenkins (Development Builds)](https://ci.sidpatchy.com/)

## Commands
| Command Usage              | Description                                       | Permission                      |
|----------------------------|---------------------------------------------------|---------------------------------|
| `/ir restore <player>`     | Opens a GUI to select the backup you require.     | `inventoryrollback.restore`     |
| `/ir forcebackup <player>` | Forces a backup for an online player's inventory. | `inventoryrollback.forcebackup` |
| `/ir reload`               | Reloads the plugin's configuration file.          | `InventoryRollback.reload`      |
| `/ir enable`               | Enables the plugin if previously disabled.        | `InventoryRollback.enable`      |
| `/ir disable`              | Disables the plugin.                              | `InventoryRollback.disable`     |

## Permissions
| Permission Node                     | Description                                         | Default Access |
|-------------------------------------|-----------------------------------------------------|----------------|
| `inventoryrollback.cmd`             | Allows access to the base command *(/ir)*           | OP             |
| `inventoryrollback.restore`         | Grants access to */ir restore*                      | OP             |
| `inventoryrollback.forcebackup`     | Grants access to */ir forcebackup*                  | OP             |
| `inventoryrollback.enable`          | Grants access to */ir enable*                       | OP             |
| `inventoryrollback.disable`         | Grants access to */ir disable*                      | OP             |
| `inventoryrollback.deathsave`       | Saves inventory on a player death.                  | All            |
| `inventoryrollback.joinsave`        | Saves inventory on joining the server.              | All            |
| `inventoryrollback.leavesave`       | Saves inventory on leaving the server.              | All            |
| `inventoryrollback.worldchangesave` | Saves inventory when changing to a different world. | All            |

# Why does this fork exist?
Danjono, the plugin's original dev, seems to have disappeared off the face of the earth. I intend to maintain this fork in their absence. I will be manually merging pull requests (which I believe are of benefit to the plugin) from the original repo.

Additionally the author of the other Inventory Rollback fork has licensed all their changes as all rights reserved. I disagree with that philosophy, the mere ability to publish our forks should demonstrate that copyleft licenses are a good thing.
