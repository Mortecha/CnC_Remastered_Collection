# CFE Patch Redux for CnC_Remastered_Collection
------------------
This mod updates the original CFE Patch mod by cfehunter to the official 9/24/2020 hotfix patch (supposedly the final official patch) and adds new features.

This is a Tiberian Dawn mod only at present. A Red Alert port is planned, but the RA code here only includes cfehunter's unfinished work from June 2020 (not usable, might not even compile).

The original CFE Patch features all appear to be working, but I have not thoroughly tested them or examined the code for uncaught merge conflicts.

The current version is 1.3.

# Features
------------------
You can control the following features via the CFEPATCHREDUX.INI file located in "My Documents\CnCRemastered\Mods\Tiberian_Dawn\CFEPatchRedux\":

- ASTAR\_PATHING (0/1) -- If enabled, units use the superior A\* pathfinding algorithm instead of CnC's default "crash and turn" algorithm.
- OOM\_REPAIR (0/1) -- If enabled, building repairs are suspended, rather than canceled entirely, for insufficient funds.
- RALLY\_POINTS (0/1) -- If enabled, rally points can be set for unit-producing buildings and repair bays. Hold Alt to set a rally point on a unit or building.
- HARVY\_QUEUE\_JUMP (0/1) -- If enabled, harvesters will cut in line when they are closer to the refinery than the other harvester.
     - QUEUE\_JUMP\_CUTOFF (integer, in cell units) -- If a harvester is closer to its target refinery than this distance, other harvesters won't cut in front of it.
- HARVY\_LOAD\_BALANCING (0/1) -- If enabled, restores the "load balancing" refinery selection behavior added in the official Sept. 16 patch, and removed in the official Sept. 24 hotfix patch.
     - If both HARVY\_LOAD\_BALANCING and HARVY\_OPTIMIZE are enabled,  HARVY\_LOAD\_BALANCING will be ignored.
- HARVY\_OPTIMIZE (0/1) -- If enabled, harvesters will select the nearest refinery, while pretending that the distance to each refinery is increased for each other harvester already bound for that refinery. Results in good load balancing, but without harvesters driving to very distant refineries.
     - HARVY\_OPTIMIZE\_UNLOAD\_WAIT\_WEIGHT (integer, in cell units) -- Specifies the size of the distance increase per other harvester. The theoretical optimum is one half the distance a harvester can travel during the time it takes another harvester to unload.
     - HARVY\_OPTIMIZE\_THRASHING\_CUTOFF  (integer, in cell units) -- If a harvester is closer to a refinery than this distance, a multiplier is applied to the distance increase per other harvester in order to prevent thrashing (driving back and forth repeatedly as refineries alternate which is slightly less congested).
     - HARVY\_OPTIMIZE\_THRASHING\_NUMERATOR (integer) and HARVY\_OPTIMIZE\_THRASHING\_DENOMINATOR (integer) together specify a fraction that is the anti-thrashing multiplier. Sane values are between 0 (always stick to current refinery) and 1 (no anti-thrashing effect).
     - HARVY\_OPTIMIZE\_COMMUNALISM\_NUMERATOR (integer) and HARVY\_OPTIMIZE\_COMMUNALISM\_DENOMINATOR (integer) together specify a fraction used as a "communalism multiplier." HARVY\_OPTIMIZE\_UNLOAD\_WAIT\_WEIGHT multiplied by the communalism multiplier yields a "communalism cutoff." If a harvester is closer to a refinery than another harvester bound for that refinery by a margin greater than the communalism cutoff, then it will ignore that other harvester for purposes of choosing a refinery. If set to 0, a harvester will always choose the best refinery for itself, even if that means making other harvesters wait longer. If set to a very large value, like 10000, harvesters will always be mindful of other harvesters. The default is 2.25, which means roughly "you can ignore other harvesters if you can unload and get out of the way before they arrive."
- HARVY\_SELF\_REPAIR (0/1) -- If enabled, harvesters will slowly regain hp up to 50%.
- DISABLE\_COMMANDO\_AIRSTRIKES (0/1) -- If enabled, prevents the computer from using airstrikes until the player has a base.
- ATTACK\_MOVE (0/1) -- If enabled, shift+click to issue an attack move order, and units will stop to fight along their path.
- COMMANDO\_GUARD (0/1) -- If enabled, commandos will attack things while in guard mode (or attack-move mode, if that's enabled).
- SAFE\_SABOTAGE (0/1) -- If enabled, a building destroyed with C4 never spawns surviving infantry.
- BUILDING\_GAP (integer 1 to 10, in cell units) -- Sets allowable space between buildings. Set to 1 for the default Tiberian Dawn behavior requiring adjacent buildings. Set to 2 for the default Red Alert behavior allowing a gap of 1 cell.
- TIB\_GROWTH\_SCALE (integer) -- Sets how many times to run the tiberium growth logic when it would ordinarily be run once. (Note: Multiplicative with the multiplayer setting.)
- WALL\_BUILD\_LENGTH (integer 1 to 10) -- If greater than 1 enables Tiberian Sun/Red Alert 2 style wall building with max length specified.
     - If WALLS\_HAVE\_FULL\_COST (0/1) is enabled, you are charged for each cell of wall; otherwise you are charged the base price regardless of length.
- Always enabled: Aircraft will ignore an attack order if they have no ammo.

# TODO List:
------------------
- RA Port
- Add .ini option for aircraft ammo check
- Replace the tiberium growth logic with something sane?
- Multiplayer units in campaign
- Capturable churches
- Single-engineer capture for RA
- Better skirmish AI
- Skim steam workshop for features worth borrowing

# Credits
------------------
cfehunter -- original CFE Patch

As per original CFE Patch notes:
- FluffyQuack -- Assistance with building tile gaps & multi wall improvements
- A\_\_Gun -- Assistance with building tile gaps.
- Spyyre -- Helping to track down the building placement issue.
- pchote -- Tile drawing in remastered view
- Butch -- Assistance with attack move polish

ChthonVII -- Merge official patches since cfehunter abandoned project, harvester refinery selection optimization
