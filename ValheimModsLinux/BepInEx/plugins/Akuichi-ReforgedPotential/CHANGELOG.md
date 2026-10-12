# 2.0.7
* Updated README.md
* Made hidden mechanic toggle-able `Allow Extra Upgrade Limit On Current Tier` Setting: 	when enabled, the current boss tier allows an extra upgrade level on the current tier's base upgrade limit.
* New `Enable Level Cap` Setting: when enabled, a level cap is enforced for all equipment upgrades (This takes precedence over boss upgrade limits.)
* New `Level Cap` Setting: The maximum level that an equipment can be upgraded to if Enable Level Cap is set to true.

# 2.0.6
* Added EpicLoot compatibility, items now retain their enchantments when upgraded
* Recipes now are properly synced from server

# 2.0.5
* New `Enable Debug Logging` Setting: Config toggle to show debug logging.
* New `Consume Idols Only On Failure` Setting: when enabled, failed upgrades consume idols but restore the item to its original quality instead of degrading it (while break outcomes still destroy the item).
* New `Refund Idols On Break` Setting: when enabled, returns configured total used idol percentage if an equipment breaks during upgrading.
* New `Refund Idols On Break Starting Level` Setting: Calculation of the refunded idols starts at this level. (Ex. at value 5: Levels 1-4 are not included for the idol refund calculations).
* New `Refund Idols Percentage On Break` Setting: The percentage amount of idols of each tier used that is refunded if an equipment breaks during upgrading.
* Now uses the player's profile to track boss kills instead of checking for inconsistent playerkeys.
* Upgrade chance and break chance are now independent from each other.

# 2.0.4
* Global notifications now use the In-game item name instead of it's prefab name

# 2.0.3
* Fixed chances not being applied when Idol Progression is turned off

# 2.0.2
* Fixed not being able to upgrade normally on crafting stations
* Fixed upgrade and break chances not registering

# 2.0.1
* Temporary revert to 1.1.1 build until upgrade chance bug is fixed

# 2.0.0
* Added Jotunn as dependency
* Refactored recipe creation using Jotunn's api
* Config now syncs with server if installed on a server
* Added Boss Progression for further upgrades (On by default)
* Added Idol requirement progression (On by default)
* Added Global notifications for upgrading results (Off by default)
* Added toggle to crafting idol recipes

# 1.1.1
* Fixed typo

# 1.1.0
#### Added four new configuration options under the Upgrade Settings section to control how ingredient costs scale with item level:
* CostStart (default:1) — Base idol cost of upgrading any equipment.
* CostIncreasePerInterval (default: 1) — How many extra idols are added each scaling step.
* CostIncreaseInterval (default: 2) — Number of item levels required between each cost increase.
* CostScalingLevelStart (default: 6) — Level at which upgrade cost scaling begins.

# 1.0.1
* Fixed upgrade cost being free when cost increase per level is set to 0

# 1.0.0
* Initial release
                                                                                                                                                        