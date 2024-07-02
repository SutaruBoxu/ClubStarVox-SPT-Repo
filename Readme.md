# The Club StarVox SPT Guides
This is a collection of tips and configurations for SPT from the Club StarVox community Discord server.  
Refer to the server with any questions or suggestions regarding this repository.  
Most, if not all, of the items here are referenced or covered in the SPT Show on YouTube for demonstration.

### Club StarVox Links

[StarVox on YouTube](https://www.youtube.com/channel/UC_NQ0kJpwwjjd708z5YsYeQ)

[StarVox's SPT Quick Start Guide](https://shore-emery-aa6.notion.site/SPT-AKI-Starter-Guide-d3c17ba5bcd94aae88ec382f0c3c1d30)

[StarVox's SPT Mod List](https://starvox.notion.site/StarVox-s-SPT-3-8-3-Mod-List-58c11fea78994e26a094dac43ac85e69)

[The Club StarVox Discord Server](https://discord.gg/9GNEtnK2Yj)

[Original Google Site for this repository](https://sites.google.com/view/club-starvox-spt/home)

# Mod Configurations
### Load Order  

Many SPT mods won't require you to assign them a specific location in the game's Load Order, but several must be place well to work properly.  
Always read a mod's description on the Filebase or GitHub, as it will often clarify a Load Order requirement.  
Most will state that the mod needs to load "last" in the order to function properly, meaning it must hold certain changes against other mods.  
When inherently conflicting mods are patched to work together, they need to be loaded in the correct order to function.  

[StarVox's 3.8.3 Mod Load Order](https://lh6.googleusercontent.com/MrmsJVWNACwnjiDnddRViZsoo0PuNU9fbBh18iGYa8DS08BjPLjKRldGwUVw3EBrA6XdZIW1v3WJGyTUzzy9uivAOkfeGaNNWZap8u7FZrQP047el56gdljqfsStOGlFVg=w1280)  

<details>

<summary>Load Order List</summary>
  
1. Modular Attachments
2. MFAC Shop
3. Artem
4. Painter
5. Bright Lasers
6. Borkel's Bullet Wounds
7. Backdoor Bandit
8. EpicRangeTime's All-In-One
9. Fontaine's FOV Fix & Variable Optics
10. More Checkmarks
11. Black Core
12. Mag Tape
13. Tactical Gear Component
14. ODT Item Info
15. Two-Slot Extended Mags
16. Raid Review
17. AllTheClothes
18. DeDistortionizer
19. Looting Bots
20. Borkel's NVGs
21. Borkel's Realistic Thermal's
22. SPT Realism Mod
23. SWAG+Donuts
24. UI Fixes
25. Virtual's Custom Quest Loader
26. Trader Modding & Enhanced Weapon Building
27. The Server Value Modifier
28. SAIN

</details>  

##  

### The SPT Realism Mod  
[The SPT Realism Mod](https://hub.sp-tarkov.com/files/file/606-spt-realism-mod/) is an extensive game play overhaul to make Tarkov mechanics more realistic and immersive.  
This mod makes drastic changes to central game mechanics that players should be aware of upon installation.  
The Traders, Flea Market, Weapon Handling, Injury Treatment systems and more will all take on new rules and mechanics.  
Even things like arm stamina when holding weapons in a certain stance will require attention from the player, so research is critical.  

As of mid-June, the Hazards Update for Realism Mod is out and adds toxic zones to the game along with numerous other features.  
I will need to update this entry to reflect those additions and changes.  
I am also currently working on an updated comprehensive review for the mod.  

In the meantime, I use the majority of changes made by Realism Mod and enjoy what they do for the game.  
The stances, ground type and slope speed modifiers, and adjusted weapon handling all enhance the immersive SPT experience.  
Despite the plethora of sliders and values available in the mod's BepInEx entry, I have only adjusted a few of them.  
In particular, I have sped up the process of checking the chamber, checking magazine contents, and the quick reload animations.  
I've also enabled the new High Ready spring animation and disabled the Idle Arm Stamina Drain to prevent frequently spending the arms.  
Lastly, I often revisit the Low Ready and High Ready stance position settings, using the sliders to move the arms and how the hold weapons.  
It's rather difficult to do, the sliders have large steps and cause the arms to move entirely too far on every axis, necessitating verbose input.  

### SWAG+Donuts
[The SWAG+Donuts mod](https://hub.sp-tarkov.com/files/file/878-swag-donuts-dynamic-spawn-waves-and-custom-spawn-points/) is an overhaul for the bot spawn system, introducing numerous scenarios for waves in raids.  
The `Starting PMCs Quiet Raids` preset is what I use most often. This only spawns PMC bots at the beginning of each wave.  
Additionally, I have edited the `ScenarioConfig.json` file to control max spawn caps for bots on all maps, but SWAG is left as is.  
These configurations are designed to accommodate my PC hardware and to promote immersion in-raid with a lore-friendly bot count.  

An example of the changes I've made to `ScenarioConfig.json` is here, for the `Starting PMCs Quiet Raids` scenario:  

```
"Name": "starting-pmcs-only-quietraids",
  	"PMCBotLimitPresets": {
      "FactoryBotLimit": 5,
      "InterchangeBotLimit": 5,
      "LaboratoryBotLimit": 5,
      "LighthouseBotLimit": 5,
      "ReserveBotLimit": 5,
      "ShorelineBotLimit": 5,
      "WoodsBotLimit": 5,
      "CustomsBotLimit": 5,
      "TarkovStreetsBotLimit": 5,
      "GroundZeroBotLimit": 5
    },
    "SCAVBotLimitPresets": {
      "FactoryBotLimit": 5,
      "InterchangeBotLimit": 5,
      "LaboratoryBotLimit": 5,
      "LighthouseBotLimit": 5,
      "ReserveBotLimit": 5,
      "ShorelineBotLimit": 5,
      "WoodsBotLimit": 5,
      "CustomsBotLimit": 5,
      "TarkovStreetsBotLimit": 5,
      "GroundZeroBotLimit": 5
```
This reduces the spawn limit for both PMC and Scav bots to a total of five each for this particular scenario, but I've adjusted them all similarly.  
Even without changing SWAG configurations, these numbers seem to provide both optimial performance and immersion in most raids.  
With Questing Bots and Looting Bots running, these wave numbers provide activity both near and far for the player in our testing.  

### SAIN 2.0
[The SAIN mod](https://hub.sp-tarkov.com/files/file/1062-sain-2-0-solarint-s-ai-modifications-full-ai-combat-system-replacement/) is an overhaul for the bot behavior system, hugely expanding their capabilities and potential for customization.  

This mod comes with several default presets randing from "very easy" to "very hard" and each can be fully configured.  
Due to its complexity and constant activity in-raid, SAIN is considered to be performance-intensive and can slow weakers PCs.  

It should be noted that certain changes need to be made in the SAIN GUI when used toegether with the "That's Lit" mod.  
Without the proper configuration, bots will suffer an immense nerf to their perception, rendered largely unable to find the player.  
The exact parameters to be changed are listed on the "That's Lit" mod page and involve entity vision detection.  
With these changes in effect and a correct load order, SAIN will be in full effect and should be working without issue.  

It should also be noted that I still observed what seemed like problems even with those changes in effect.  

Concerning performance, SAIN uses a lot of PC resources to run added custom commands for the bots.  
Reducing the activity of bots, through reducing parameters for sighting and engagements, reduces that strain on performance.  
With sliders for "Aggression", "Vision Multipliers" of various kinds, and even "Reaction Time" for certain circumstances like CQB,  
it's easy to make the bots simply carry otu fewer checks and actions in raids.  
This is one of the primary methods of controlling SPT performance.  

### Raid Overhaul
[The Raid Overhaul mod](https://hub.sp-tarkov.com/files/file/1673-raid-overhaul/) adds an array of random events and other changes designed to make raids more dynamic and interesting.  

The many new events added by this mod should be reviewed upon installation, such as the "Heart Attack" and "Blackout" events.  
They can affect player health, the armor of everyone in the raid, lights, doors, and even skills. Do not go in unprepared.  
Extra preparations will be necessary for raids after installation, especially when the SPT Realism Mod is also running.  

What's more, there are some features that conflict with other primiary mods, like Realism Mod, to an extent.  
Each conflict-prone item, I have disabled for compatibility reasons.  
I do, also, toggle most of the brutal or silly events, such as "Heart Attack".  
While potentially immersive, they can easily make recording footage for videos a much more challenging process.  
The same goes for the mod's "Local Time" feature for raids, I've sabled it to continue using the "Weather Changer" mod.  

It should be noted that the developer has released a standalone version of "Raid Overhaul" with reduced features for a lighter experience,  
or to make it easier on those who are likely to disable many of the mod's core features anyway.  

### MeowShader
[The MeowShader mod](https://hub.sp-tarkov.com/files/file/1432-meowshader-a-stylishly-beautiful-reshade-preset/) brings ReShade into Tarkov with a very intuitive in-game GUI.  
There's no complex installation method, simply drag the files out of their download and into your SPT installation folder.  
It seems messy adn the files will be loose in your SPT folder, but that's how it works.  
The Filebase also shows that it's outdated, but ReShade doesn't require any updates in this case - it functions very well.  

When MeowShader is running, it will load all preset shaders at startup, visible in a bar at the top of the screen.  
By default, the "Home" key opens the interface and the "End" key toggles the mod's effects on and off.  
The GUI consitst of a list of plugins and their controls, once enabled, at the bottom of the window.  

Many ReShade plugins are heavily graphics-intensive and will require more PC resources than vanilla EFT or SPT.  

