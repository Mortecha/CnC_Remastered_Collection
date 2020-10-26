# CFE Patch Redux for CnC_Remastered_Collection
------------------
This mod updates the original CFE Patch mod by cfehunter to the official 9/24/2020 hotfix patch (supposedly the final official patch) and adds new features.

The current version is 1.4.

The Tiberian Dawn mod is available on Steam Workshop here: [link](https://steamcommunity.com/sharedfiles/filedetails/?id=2239875646)

The Red Alert mod is available on Steam Workshop here: [link](https://steamcommunity.com/sharedfiles/filedetails/?id=2268301299)

If you don't have Steam (or Steam is misbehaving), you can download the mod directly from Github here: [link](https://github.com/ChthonVII/CnC_Remastered_Collection/releases).

The original CFE Patch features all appear to be working, but not all of them have been thoroughly tested them or examined for uncaught merge conflicts.


# Features
------------------
All features can be controlled via the INI file located at "My Documents\\CnCRemastered\\Mods\\Tiberian\_Dawn\\CFEPatchRedux\\CFEPATCHREDUX.INI" or "My Documents\\CnCRemastered\\Mods\\Red\_Alert\\CFEPatchRedux\\CFEPATCHREDUX_RA.INI". See the [settings table on the wiki](https://github.com/ChthonVII/CnC_Remastered_Collection/wiki/Features-and-INI-Settings-Charts) for details.

- A* Pathing -- Units use the superior A* pathfinding algorithm instead of CnC's default "crash and turn" algorithm.
- Infantry Tiberium Aversion (TD only) --  Infantry (except chem soldiers) will avoid walking through tiberium if a reasonable detour is available. Requires A* Pathing to be enabled.
- Suspend Building Repairs -- Building repairs are suspended, rather than canceled entirely, for insufficient funds.
- Rally Points -- Rally points can be set for unit-producing buildings. Click to set a rally point at a location. Use \[Alt\]+Click to set a rally point on a unit or building.
- Harvester Queue Jumping -- Harvesters will cut in line rather than waiting when they are closer to the refinery than the other harvester. (Can be enabled/disabled independently of Harvester Load Balancing or Harvester Optimization and works in tandem with either, or with the vanilla harvester behavior.)
- Harvester Load Balancing -- Restores the "load balancing" refinery selection behavior added in the official Sept. 16 patch, and removed in the official Sept. 24 hotfix patch. (If both Harvester Load Balancing and Harvester Optimization are enabled, Harvester Load Balancing will be automatically disabled. Harvester Optimization is strongly recommended as the superior choice.)
- Harvester Optimization -- Harvesters will select the nearest refinery, while pretending that the distance to each refinery is increased for each other harvester already bound for that refinery. Results in good load balancing, but without harvesters driving to very distant refineries. See the Settings Chart for further details. (If both Harvester Load Balancing and Harvester Optimization are enabled, Harvester Load Balancing will be automatically disabled. Harvester Optimization is strongly recommended as the superior choice.)
- Harvester Self-Repair (TD only) -- Harvesters will slowly regain hp up to 50%.
- Disable Commando Airstrikes (TD only) -- Prevents the computer from using airstrikes until the player has a base.
- Commando/Tanya Guard -- Commandos/Tanya will attack things while in guard mode.
- Safe Sabotage -- Buildings destroyed with C4 never spawn surviving infantry.
- Instant Capture (RA only) -- Engineers always capture buildings, regardless of the building's health.
- Attack-Move -- Use \[Shift\]+Click to issue an attack-move order. Units will move to the destination while stopping to fight foes encountered along their path. Aircraft will return to base after running out of ammo or reaching the destination. Boats (except the normal submarine) will attack briefly, then resume movement. Surface boats will not alter course to chase their targets. (Attack-move code was entirely rewritten in v1.4.)
- Smarter Aircraft -- Aircraft given an attack or attack-move order will ignore the order if they have no ammo.
- Configurable Build Distance -- Controls the maximum allowable gap between buildings, allowing a TD-style no-space, or an RA-style 1-space, or larger gaps if you like.
- Tiberium/Ore Growth Scale -- Applies a multiplier to tiberium/ore growth rate.
- TS/RA2-style Wall Building -- Automatically builds wall pieces in the intervening spaces when a wall piece is constructed in line with a nearby piece of the same type. Hold \[Ctrl\] when placing a wall piece to disable this behavior. (Note: This feature is not compatible with LAN multiplayer. A total rework of this feature is planned to fix it.)
- Configurable Silo/Refinery Capacity (RA only) -- Increases (or decreases) the amount of ore silos and refineries can hold.


# TODO List
------------------
See [wiki](https://github.com/ChthonVII/CnC_Remastered_Collection/wiki/TODO-List).

# Credits
------------------
cfehunter -- original CFE Patch

As per original CFE Patch notes:
- FluffyQuack -- Assistance with building tile gaps & multi wall improvements
- A\_\_Gun -- Assistance with building tile gaps.
- Spyyre -- Helping to track down the building placement issue.
- pchote -- Tile drawing in remastered view
- Butch -- Assistance with attack move polish

Root-Core -- original RA port of CFE patch

ChthonVII -- Merge official patches since cfehunter and Root-Core abandoned project, harvester refinery selection optimization, infantry tiberium aversion, complete rewrite of attack-move code, assorted bugfixes.

# A Reminder About the GPL
------------------
A reminder like this *shouldn't* be necessary. But it appears it is necessary since one of the most popular mods on Steam Workshop has appropriated a lot of GPL code (both from EA and from other modders), and yet its author has ignored at least a dozen public requests for its source code. So let me be clear: You are free to copy my source code and use it in your mod, so long as you do so in accordance with the GPL. That means, if you use my code in your mod, then you are legally required to license your mod under the GPL and to make your mod's source code publicly available (and a few other things too -- go read [the GPL](https://github.com/ChthonVII/CnC_Remastered_Collection/blob/master/License.txt)). Using my code in a manner inconsistent with the provisions of the GPL is copyright infringement. If it comes to my attention that you are using my code in your mod, but not making your mod's source code publicly available, I will give you a brief opportunity to rectify the situation, and then I will file a DMCA complaint against your mod if you fail to do so. Don't make me do that. Don't be a jerk. Publish your source code.

# A Reminder that Mods Are Not Official EA Products
------------------
 This is a mod. It's not an official EA product. In fact, [EA wants](https://www.ea.com/games/command-and-conquer/command-and-conquer-remastered/modding-faq) mod authors to remind you that “EA has not endorsed and does not support this product.” So there.
