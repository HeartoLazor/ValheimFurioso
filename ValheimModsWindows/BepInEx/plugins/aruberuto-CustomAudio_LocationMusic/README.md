# CustomAudio, now with locations music

This is a fork of the original [CustomAudio](https://www.nexusmods.com/valheim/mods/90) mod by aedenthorn.
It allows the substitution of location music, which was previously not implemented (as location music was added in a later game update).

## Important change from the original CustomAudio
The mod first loads audio tracks found in the `BepInEx/plugins/CustomAudio` folder (as in the original mod).  
Afterwards it looks for the folder `CustomAudio` in any of the `BepInEx/plugins/<modauthor>-<modname>/` folders, and loads it.   
It will overwrite similarly named audio tracks and folders, if they have the same names. 

In this way, CustomAudio is fully compatible with r2modman's package structure, and no action from the user (such as copying the `CustomAudio` folder to the `plugins/` folder) is required.

## How to change location music

Unlike normal music, location music does not have track lists (1 location, 1 track). 
To substitute the original track, location, simply add a with the same name as the original one into the `CustomAudio/Music` folder 

As of 0.218.19, these are the names of the location music tracks:

Ashland - Fortress  
Ashlands - Ruins 1  
Ashlands - Ruins 2  
Ashlands - Ruins 3  
Black Forest - Greydwarf Camp  
Black Forest - Haldor  
Black Forest - Smouldering Tomb  
LocationReveal  
Meadows - Hildir  
Meadows - Village & Farm  
Mistlands - Dvergr Excavation Site  
Mistlands - Dvergr Tower  
Mountain Cave Sanctum  
Mountains - Abandoned cottages  
Mountains - Howling cavern  
Plains - Fuling Camp  
Plains - Sealed Tower  
Plains - Stone Henges  

LocationReveal is the burial chamber discover track in the black forest. All other names are self explanatory.

For everything else, refer to the original CustomAudio readme.  
For an example, check out my [Elderscrollian themed soundtrack](https://thunderstore.io/c/valheim/p/aruberuto/Elderscrollian_themed_soundtrack/) package.
