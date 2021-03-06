# Single Train Unit

Adds a single train unit comprising of a small cargo/fluid wagon and a locomotives at both ends. Total size is of a standard wagon. There are separate cargo and fluid wagon versions.

![Single Train Unit Examples](https://thumbs.gfycat.com/DependableMixedBarasinga-size_restricted.gif)


Overview
============

- Intended for use as single unit trains, but they be joined together or joined with other locomotives or wagons (see Limitations).
- The unit's first and last 2 tiles are for feeding fuel to the locos. For Cargo wagons the middle 2 tiles are for accessing the small cargo wagon. For Fluid wagons the middle third is for connecting one pump. See the images.
- The units run between the performance of a single loco & wagon (1-1) and a dual headed train with a wagon (1-1-1). It consumes fuel at twice the usual loco rate to account for its compact dual direction nature. These are all changeable via mod settings.
- The cargo/fluid wagon space is 1/2 of the standard capacity given its small size. These are changeable via mod settings.
- The units are unlocked with the standard Railway research or modded variant research.
- Place the dual headed cargo/fluid wagon in the usual manner and it will be replaced out for the 2 mini locos and a mini cargo wagon.
- The unit will be mined by the player as a whole and will be damaged/destroyed as a whole.
- While the graphics look as one, there are actually 2 separate locomotives and a wagon there. So you must fuel both locomotive ends separately and select the right part of the Single Train Unit for giving train orders, entering to drive it, viewing the cargo, etc.
- UPS efficient as there is no continuously running active code in the mod, so no ongoing CPU load added to the game.
- An optional mod setting exists to disable the standard larger locomotives and wagons. Unique purpose wagons like the artillery wagon and modded Vehicle Wagon are not impacted. If this is applied mid game it won't remove any existing standard rolling stock or set recipes, but will disable and hide the recipe to avoid future use. A whitelist option exists to exclude specific named entities from disabling.


Not Implemented Yet / TODO
================

- Graphics are a work in progress and there is a mod setting to turn them on. By default the vanilla game's cargo wagon and fluid tanker graphics are used. Graphics for when stopped at stations are being done first, with the rotations being done in stages after this.
- Method for players to colour the train unit.
- Add direction indicator to placement graphics to help with snapping to stations.
- Support for other mods to place the single train units, i.e. Train Construction Site.


Limitations / Known Issues
================

- You can't get out of a fast moving train some times. This seems to be a core Factorio limitation.
- Don't build a longer train with multiple single train units joined together out of order. Start at one end and place each one sequentially. As placing a middle single train unit between 2 other rail wagons may not place correctly.
- You can not detach a single train unit from other carriages as the parts all face outwards. There is protection in the mod to prevent a single train unit being broken up. However, you can detach regular carriages (cargo, loco, fluid) from a single train unit. If you need to detach a single train unit from another, the only option is to mine (pickup) one of them.
- Single train units when being placed will only snap to a stations position if they are facing the right way. There's no visual way to tell their direction at present, so just rotate them before placing if needed. Snapping on corners can be finickity.
- When single train units are blueprinted with fuel in them the highest fuel value type and count across them all is noted and this is used in the ghosted request. As blueprints lose the relationship between the single train unit parts its not possible to keep the fuel to train parts exactly the same.
- When one single train unit is blueprinted with a schedule, the schedule will be applied correctly. However, if a blueprint has multiple single train units in it, they will all get the same schedule.
- A single action that does multiple damages at a time (i.e. explosive rocket) will only do the single max damage and not the total cumulative damage. In the case of explosive rockets this means it will lose the lower impact damage, but get the correct higher blast damage. This is the fairest balance solution I can find so far to damage across the multiple parts of the train unit.
- When a player or bot mines a single train unit the mod will try and take all of the contents before removing the unit, however, in some cases things may still get dropped on the ground. This is similar to some mining actions in vanilla Factorio.
- In an existing blueprint using the "Select new Contents" option will give a messed up blueprint contents. Core Factorio bug: https://forums.factorio.com/88100
- Other mods that try to manipulate the train unit may have issues. Please report anything so I can review it if not listed below already.


Compatible New Recipe & Tier Mods
====================

- Battery Pack
- Factorio Extended
- Factorio Extended Plus
- AAI Industry
- Krastorio 2
- Zombies Extended
- Schall Armoured Train - armoured trains and nuclear trains

Compatible Usage Mods
=============

*Fill4Me*
The Fill4Me mod's auto insertion of fuel is applied to both locomotive ends of the single train unit. If you don't have enough fuel then as much as is available will be spread between the 2 locomotives.

*Signalized Couplers*
As the single train unit is made up of 3 train parts internally you need to account for this in the signals used. i.e. to decouple a single train unit at the end of a train use -3 as the decouple signal, not the standard -1 for a vanilla cargo wagon or locomotive.

Intentionally Ignored / 0 Impact Mods
==============

- Vehicle Wagon (2)
- Multiple Unit Train Control
- Noxys Multidirectional Trains
- Space Exploration - always keeps an item only version of the locomotive available for science use

Incompatible Mods
============

I have not blocked any other mods unless they hard break this mod. As while some won't work with the single train units added by this mod, they will still work with other types of trains and wagons. All train related mods with known issues or no effect are listed below with details.

*Bulk Rail Loader*
At present the Bulk Rail Loader can't work with the single train units as the Bulk Rail Loader only tries to take cargo items from one end of the wagon, which is a locomotive in the single train units case. This has been raised with the mod author to see if there's a solution. https://mods.factorio.com/mod/railloader/discussion/5f59068dab70d5cb80c7e723

*Electric Train*
At present no integration is present and so there isn't an electric version available.

*Train Construction Site*
Mod isn't compatible with single train units due to how it creates the boxed train prototypes at present. Not raised to mod author so far due to lack of interest.

*Renai Transportation*
Mod isn't compatible as it manipulates the train entities when they land after flying. This may be supportable in the future, but not planned at present.