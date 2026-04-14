# BloomTraversalSystem - A prototype of a responsive traversal system with PCG implementation

## Description 
The Bloom Traversal System Project is a prototype of an enhanced traversal system that has add on inventory funcitonality and early implementation of PCG logic for realtime spawning. 

### Required Plugins (enable in Edit → Plugins):
 
| Plugin | Version | Notes |
|---|---|---|
| Procedural Content Generation Framework (PCG) | 1.0 | Core PCG system |
| PCG External Data Interop | 0.2 | Beta — external data formats |
| PCG FastGeo Interop | 0.1 | Experimental — runtime primitive spawning |
| PCG Geometry Script Interop | 0.2 | Beta — geometry script integration |
 

## Installation and build instructions

### Prior to Installation: 

1. Intall Epic Games Launcher 
2. Download the Unreal Engine version 5.7.3

### Installation

1. Clone/download repository found here: 
https://github.com/Namrata-Gurung/BloomTraversalSystem.git 
2. Navigate to the project folder and open BloomTraversalSystem.uproject. If rebuild prompt appears, please click yes. 
3. Enable the required plugins via navigating to Edit tab, Plugins and selecting the PCG pluigns. Restart the editor as prompted. 
4. All the main project code is within the PCGEnhanced_TMS plugin folder with changes made in the Third Person Content folder only to ABP_Unarmed and BP_ThirdPersonCharacter. 

### Project Opening 

- The starter map provided in the starter assets should load and the play button can be pressed to view the plugin functionality in action. 
- The level can then be played through and tested. 
- The content drawer, whcih contains all of the files can be found at the bottomof the editor and docked in the layout to access all the code files. 

## Controls
 
| Action | Key |
|---|---|
| Move | WASD |
| Jump | Space |
| Sprint | Shift |
| Crouch | C |
| Slide | Shift + X |
| Toggle Inventory | F |
| Debug Inventory | 1 |

## Project Structure
- This is the folder tree structure where the following can be found. 

```
Content/
├── Characters/          # Character assets
├── Input/               # Input action mappings
├── LevelPrototyping/    # Main level
├── ThirdPerson/         # Base third person assets
 
Plugins/PCGEnhanced_TMS/
├── Animations/
│   ├── Crouch/          # Crouch animation assets
│   ├── Slide/           # Slide animation assets
│   ├── ABP_TraversalLayer        # Main animation blueprint
│   ├── ALI_TraversalLayers       # Animation layer interface
│   └── BS_Crouch                 # Crouch blend space
├── Components/          # AC_InventoryComponent, AC_TraversalComponent
├── Input/               # IA_Crouch, IA_Slide, IA_Sprint, IA_ToggleInventory, IMC_Extended
├── Interfaces/          # Blueprint interfaces
├── Items/
│   ├── Blueprints/
│   │   ├── Equipment/   # Equippable item blueprints (e.g. BP_BootItem_Left)
│   │   └── ItemResponses/ # Item response blueprints (e.g. BP_ItemResponse_BootLeft)
│   ├── DataAssets/      # Item data assets (e.g. DA_BootLeft)
│   └── Equipment/
│       ├── Materials/
│       ├── Meshes/
│       └── Textures/
│           ├── Boot/
│           └── Hoverboard/
├── Foliage/
│   ├── Materials/
│   ├── StaticMeshes/
│   └── Textures/
├── Icons/               # Item icons for UI
├── PCG/                 # PCG graph assets
└── UI/                  # Widget blueprints (WBP_InventoryBox, WBP_InventorySlot)
```

## Game Scene 
In the game scene, the player character spawns in the the cnetre of the thrird person map, provided in the Third Person Starter Assets. There is no on screen UI for the main scene, however, the player can toggle inventory and see the invenotry populated with the equipment items in the game world. 

## Known Issues / In Progress
 
- PCG foliage spawning system is partially implemented — graph exists but runtime triggering from boot equipment is still being integrated
- Inventory description panel and item inspection UI not yet implemented
- Socket positioning for equippable items may require adjustment on each skeleton and item added 

## Version Information

Unreal Engine version 5.7.3

## Onedrive link 
https://cityuni-my.sharepoint.com/:f:/r/personal/namrata_gurung_city_ac_uk/Documents/2025IndividualProject/New%20folder/addf055_ProjectPackageSubmission?csf=1&web=1&e=x1GnPC 

##References

Adapted from: JBarlowTraining (2024), YouTube
Accessed: April 2026, URL:https://youtu.be/Fxwy4H33g44?si=I3X7kSy6QUB34g1Y

Logic informed by: Mind-Brain (2022), Unreal Engine Forums
Accessed: April 2026, URL: https://forums.unrealengine.com/t/detect-player-z-velocity/715404/3 


https://www.youtube.com/watch?v=LM3Tw49G0g8&t=285s

Logic adapted from: 
Accessed: April 2026, 

Logic reused from: 
Accessed: April 2026, URL: 

Logic informed by: JephyDa1st (2022), Unreal Engine Forum
Accessed: April 2026, URL: https://forums.unrealengine.com/t/how-to-check-whether-character-is-on-ground/395981/9 


Logic reused from: Mitchell Theriault, GameDev.tv Team, Ben Tristem (2026), Udemy, Unreal Engine Blueprint course video 
Accessed: April 2026, URL: https://www.udemy.com/share/101Xs63@PH9BtizFdUqgKw3QiGxHVo_GUfDPjhsk_-UQYy__weu66F6Dp2ei0Xb0seDqABvRlA==/ 