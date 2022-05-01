# Pavlov Push Advanced Pack by Golden


## Installation
1. Open the Pavlov.uproject.
2. Rename the UGCxxxx with the same name as your project's UGC folder.
3. Then right click on the UGC > Migrate
4. Inside your project, open your gamelogic and chose PAP_GlobalInfo, PAP_PlayerInfo and PAP_PlayerProxy as references.
5. Drag and drop the PAP_PlayerProxy in your level!
6. Go inside the PUSH_Setup folder.
7. Put two PAP_PushLoadoutProxy in your level. (There are 4 examples, 2 moderns and 2 WWII). You can now change the default loadout I set by opening the blueprint and going in the Class Defaults. DO NOT RENAME THE COMMANDER, ENGINEER and AT titles! If you have to, you'll have to change the node "Switch on Name" located in the "OnLoadoutTaken" function.
8. You can add custom Push objectives. The PAP_Push_CustomObjective is basic, just add the meshes. Inside the Artillery folder, you will find a PAP_PushObjective_Artillery blueprint. A working cannon can be used for the objective.
9. Inside the Artillery folder, you will find spawners for all guns.

## Sticky Grenades
1. Inside the StickGrenades folder you will find the spawner for the Gammonbomb and the magnetic grenade.
2. If Push is not the gamemode used, you can add those grenades inside the player inventory by using the PAP_PlayerProxy.

## MobileSpawns
1. To add a plane, go inside the Plane folder, add a BP_PlaneTrack on your level. Recommended height: 20000. Then move the Splineline as you want your plane to move around.
2. Add a BP_Plane blueprint in your level. Click on it, and reference your BP_PlaneTrack. It will be automatically moved on the track.
3. You can select when you want the doors to open by changing the variables "Doors Open Point" and "doors Close Point". If you don't have doors or you don't want to close them, just tick "No Doors Closing"
4. The Plane Speeed has to be adjusted (default 90"). Increase this value to slow the plane. Test by clicking the Play button in Ue4.
5. Finally, overlap one of your spawn with the BP_PlaneTeleporter to spawn players directly in the plane. 
6. By default, the BP_Plane and the BP_PlaneTeleporter are set to Team 1 (Attackers in Push). Tick "Is Team0" inside those two blueprints if those are used by the team 0!

## MSP Pavlov
1. The MSP allows you to use a Pavlov vanilla vehicle and turn it into a mobile spawn point.
2. Overlap a pavlov vehicle with the BP_VehicleMSP. When the vehicle will spawn, it will be attached to the MSP blueprint for the rest of its life.
3. The MSPTeleporter is used to teleport the player to the MSP. It is only activated when the vehicle is not moving. If the path is blocked, it will not be activated.