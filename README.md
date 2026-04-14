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

1. Install Epic Games Launcher 
2. Download the Unreal Engine version 5.7.3.

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
    ├──StylizedFoliage
│      ├── Materials/
│      ├── StaticMeshes/
│      └── Textures/
├── Icons/               # Item icons for UI
├── PCG/                 # PCG graph assets and BP_FootstepActor
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

## Credits, Attribution and Licences


### Logic 

* Reused logic has been declared where relevant, within the porject files and these appear as comments surrounding or encompassing specific pieces of logic. 

### Assets 

* Animations - Sourced from: Miaxamo, accessed: March 2026, URL: https://www.mixamo.com/#/
* Animations converted using: Mixamo Converter - Terribilis Studio, accessed: April 2026, URL: https://terribilisstudio.fr/?section=MC 
* Boot Model for main equipment item- This work is based on "White Boot" (https://sketchfab.com/3d-models/white-boot-8bb0920b41334c84ae7e99144b7a104b) by DarioMQD (https://sketchfab.com/dariomqd98) licensed under CC-BY-4.0 (http://creativecommons.org/licenses/by/4.0/)
* Hoverboard Model for placeholder equipment item - This work is based on "Hoverboard" (https://sketchfab.com/3d-models/hoverboard-30cc9b7eeda64229bb9ac689ef7c03c5) by mister dude (https://sketchfab.com/misterdude) licensed under CC-BY-4.0 (http://creativecommons.org/licenses/by/4.0/)
* Stylized Foliage for spawning - This work is based on "Stylized Foliage" (https://sketchfab.com/3d-models/stylized-foliage-c44857af70d84e448d7e6b2c10567c31) by KZNYKN (https://sketchfab.com/KZNYKN) licensed under CC-BY-4.0 (http://creativecommons.org/licenses/by/4.0/) 
* Icons located in Items/Icons/ - Screenshotted by the author from the sketchfab website on the model pages as placeholder icons
* Third Person Starter Assets - Provided by Unreal Engine on creation of the project

