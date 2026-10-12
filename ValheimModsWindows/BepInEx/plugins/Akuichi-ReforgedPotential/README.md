# Reforged Potential

With Valheim's new addition of Forge of Potential we can now upgrade our gear beyond limits, but it comes with the risk of losing your gear and I didn't want that.
This Mod solves that problem while trying to keep a balanced experience.

## Features

1. Fully Customizable Forge of Potential
2. Forge of Potential upgrade chance is now 100% by default, can be turned off.
3. Idols are now craftable with configurable recipes to meet your own needs.
4. Upgrade crafting base duration and per item level duration increase is now configurable.
5. Configurable upgrade cost and cost scaling.
6. Boss Progression
7. Upgrade material Progression

## Config

`akuichi.ReforgedPotential.cfg`

The mod features highly configurable settings

<details>
<summary><b>Server Only</b></summary>
</br>

| Config name               | Default Value | Description                                                                                                                                                                     |
|---------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable Server Sync        | true          | If true, config values are synchronized from the server to clients.                                                                                                          |

</details>

<details>
<summary><b>Upgrade Settings</b></summary>
</br>

| Config name   | Default Value        | Description |
|---------------|--------------------|-----------------|
| Upgrade Chance                                    | 1 (100%)  | The chance for an upgrade to succeed </br> <b>(Ex. 1 = Item will always upgrade without failure, 0 = Item will trigger failure)</b> |
| Break Chance                                      | 0 (0%)    | Whenever an upgrade fails, this is the chance that will determine if the equipment will break or degrade </br> <b>(Ex. 1 = Item will always break on upgrade failure, 0 = Item will just degrade 1 level on upgrade failure)</b> |
| Consume Idols Only On Failure                     | false     | If true, idols are just consumed and the item doesn't lose a level </br><b>(Triggering a break still removes the item)</br> |
| Cost Start                                        | 1         | This is the starting idol cost for upgrades before any additional calculations are made |
| Cost Increase Per Interval                        | 1         | Additional ingredient cost each time the cost scaling interval is reached starting at <b>Cost Scaling Level Start.</b> </br> <b>(Starting at level X, the upgrade cost increases by this amount every Y levels. For example, with an increase of 1 every 2 levels starting at level 6: levels 1–5 cost 1, levels 6–7 cost 2, levels 8–9 cost 3, and so on.)</b>|
| Cost Increase Interval                            | 1         | Number of levels between each cost increase. Set to 0 to disable cost scaling.</br><b>(Ex. a value of 2 means the idol cost for the next upgrade will increase every 2 levels)</b> |
| Cost Scaling Level Start                          | 1         | Level after at which cost scaling starts. |
| Upgrade Crafting Time Base Duration               | 2         | Base crafting duration for upgrading. This is the base time it takes to upgrade an equipment </br><b>(Game Default is 8)</b> |
| Upgrade Crafting Time Duration Increase Per Level | 1         | Additional crafting duration per item level. This is the additional time added per item level to the total crafting time. </br><b>(Game Default is 1)</b> |
| Refund Idols On Break                             | false     | If true, a percentage of the idols used are refunded when an equipment breaks |
| Refund Idols On Break Starting Level              | 5         | Calculation of the refunded idols starts at this level. </br><b>(Ex. at value 5: Levels 1-4 are not included for the idol refund calculations)</b>  |
| Refund Idols Percentage On Break                  | 0.3 (30%) | Percentage of idols refunded when an equipment breaks. It returns the set percentage of the idols used for each tier, 30% means 30% of each idol type used | 
| Enable Level Cap                                  | false     | If true, a level cap is enforced for all equipment upgrades </br><b>(This takes precedence over boss upgrade limits)</b> |
| Level Cap                                         | 10        | The maximum level that an equipment can be upgraded to if <b>Enable Level Cap</b> is set to true.</b> |

</details>

<details>
<summary><b>Global Notifications</b></summary>
</br>

| Config name                        | Default Value | Description                                                                                                                                                                   |
|------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable Global Upgrade Notifications | false         | Broadcasts a message to all online players when someone attempts an upgrade.                                                                                                 |
| Success Message                   | `{PlayerName} successfully upgraded {ItemName} to level {Level}.` | Message shown on a successful upgrade. Supports `{PlayerName}`, `{ItemName}`, and `{Level}` placeholders.         |
| Failed Message                     | `{PlayerName} tried to upgrade {ItemName} to level {Level}, but failed.` | Message shown when an upgrade fails. Supports `{PlayerName}`, `{ItemName}`, and `{Level}` placeholders.           |

</details>

<details>
<summary><b>Boss Progression</b></summary>
</br>

| Config name                   | Default Value | Description                                                                                                                                                                   |
|-------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable Boss Progression      | true          | If true, upgrades are limited by boss progression. Defeat bosses to unlock higher upgrade levels.                                                                            |
| Base Upgrade Limit            | 5             | Base upgrade limit for all items before additional calculations are made.                                                                                                   |
| Boss 1 Max Upgrade Level      | 4             | Additional maximum upgrade level unlocked for the wooden tier after defeating Eikthyr.                                                                                       |
| Boss 2 Max Upgrade Level      | 4             | Additional maximum upgrade level unlocked for the bronze tier and below after defeating the Elder.                                                                           |
| Boss 3 Max Upgrade Level      | 4             | Additional maximum upgrade level unlocked for the iron tier and below after defeating Bonemass.                                                                             |
| Boss 4 Max Upgrade Level      | 4             | Additional maximum upgrade level unlocked for the silver tier and below after defeating Moder.                                                                              |
| Boss 5 Max Upgrade Level      | 4             | Additional maximum upgrade level unlocked for the black metal tier and below after defeating Yagluth.                                                                         |
| Boss 6 Max Upgrade Level      | 4             | Additional maximum upgrade level unlocked for the black marble tier and below after defeating the Queen.                                                                     |
| Boss 7 Max Upgrade Level      | 4             | Additional maximum upgrade level unlocked for the flametal tier and below after defeating Fader.                                                                            |
| Boss 8 Max Upgrade Level      | 100           | Additional maximum upgrade level unlocked for the bloodgold tier and below after defeating Kall Fimbulbringer.                                                                |
| Allow Extra Upgrade Limit On Current Tier | true          | If true, the current boss tier allows an extra upgrade level on the current tier's base upgrade limit.<br><b>(Ex. after defeating Eikthyr, bronze-tier items can be upgraded one level past the base limit.)</b> |

</details>

<details>
<summary><b>Idol Progression</b></summary>
</br>

| Config name                   | Default Value | Description                                                                                                                                                                   |
|-------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable Idol Progression         | true          | If true, the idol required to upgrade equipment changes to match its current equivalent item tier and level.<br><b>(If boss progression is disabled, tiers change every 4 levels.)</b> |

</details>

<details>
<summary><b>Crafting Station</b></summary>
</br>

| Config name                   | Default Value          | Description                                                                                                                                       |
|-------------------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Global Station                 | `piece_artisanstation` | Global crafting station for all configurable upgrader recipes. Use the station `m_name` (for example, `piece_workbench`). |

</details>

<details>
<summary><b>Recipes</b></summary>
</br>

| Config name                   | Default Value                                   | Description                                                                                                                                                          |
|-------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable Recipes                  | true                                            | Enables or disables all idol crafting recipes.                                                                                                                     |
| Wooden Protection Idol        | `Wood:50,GreydwarfEye:10`                      | Ingredients for the Wooden Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                          |
| Wooden Battle Idol            | `Wood:50,GreydwarfEye:10`                      | Ingredients for the Wooden Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                              |
| Bronze Protection Idol        | `Bronze:10,SurtlingCore:1`                     | Ingredients for the Bronze Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                          |
| Bronze Battle Idol            | `Bronze:10,SurtlingCore:1`                     | Ingredients for the Bronze Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                              |
| Iron Protection Idol          | `Iron:10,ElderBark:5`                          | Ingredients for the Iron Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                            |
| Iron Battle Idol              | `Iron:10,ElderBark:5`                          | Ingredients for the Iron Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                                |
| Silver Protection Idol        | `Silver:10,FreezeGland:5,Obsidian:5`         | Ingredients for the Silver Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                          |
| Silver Battle Idol            | `Silver:10,FreezeGland:5,Obsidian:5`         | Ingredients for the Silver Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                              |
| Black Metal Protection Idol    | `BlackMetal:10,Needle:2,Tar:5`                | Ingredients for the Black Metal Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                      |
| Black Metal Battle Idol        | `BlackMetal:10,Needle:2,Tar:5`                | Ingredients for the Black Metal Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                          |
| Black Marble Protection Idol  | `BlackMarble:20,BugMeat:10,Carapace:10`       | Ingredients for the Black Marble Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                      |
| Black Marble Battle Idol      | `BlackMarble:20,BugMeat:10,Carapace:10`       | Ingredients for the Black Marble Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                        |
| Flametal Protection Idol      | `FlametalNew:10,CharredBone:15`                | Ingredients for the Flametal Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                          |
| Flametal Battle Idol          | `FlametalNew:10,CharredBone:15`                | Ingredients for the Flametal Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                            |
| Bloodgold Protection Idol      | `Gold:10,Coins:40,AncientCoin:10`             | Ingredients for the Bloodgold Protection Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                      |
| Bloodgold Battle Idol          | `Gold:10,Coins:40,AncientCoin:10`             | Ingredients for the Bloodgold Battle Idol. Use comma-separated entries in the format `PrefabName:Amount`.                                                          |

</details>

<details>
<summary><b>Logging</b></summary>
</br>

| Config name                   | Default Value | Description                                  |
|-------------------------------|---------------|----------------------------------------------|
| Enable Debug Logging            | false         | Shows debug logging.                         |

</details>


## Compatibility
- Compatible with EpicLoot by RandyKnapp

## Known Bug(s)
- Upgradeable items' icon may appear greyed out in the upgrade UI due to the item requirements being dynamic, but this is only a visual bug I'm still trying to resolve

<br>
<br>

#### You can contact me on [Discord](https://discord.gg/wq3C7t5W9b) here if you have problems or suggestions or need help in configuring values to your needs, etc.
Bug reports are always appreciated!