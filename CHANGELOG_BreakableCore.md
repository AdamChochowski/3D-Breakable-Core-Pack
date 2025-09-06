Changelog – 3D Breakable Core Pack (CatBorg Studio)

All notable changes to the 3D Breakable Core Pack Unity asset will be documented in this file.  
This project adheres to Semantic Versioning and follows the Keep a Changelog format.


---

### [4.06] – Current  
Summary: Enhanced Fade Off system, UV remapping, improved object respawn handling, and added custom damage actions.

Added  
- Fade Off Effects SO – Fade Off Effects are no longer hardcoded enums; they are now ScriptableObjects, independent from the 3D Breakable Core Pack.
- Users now have 8 initial Fade Off Effect SOs:  
  - None  
  - DisapearAllParts  
  - DisapearKeepKeyPart  
  - PieceShrinkAllPartsFade  
  - ObjectShrinkFade  
  - PieceShrinkFadeAllParts  
  - PieceShrinkKeepKeyPartsFade  
  - SinkAllParts  
  - SinkKeepKeyPart
- ActionTaken.CustomDamage – New action allowing users to set initial item durability and deal custom damage via:
  - ConductAction(int _damageCustom = 0)
  - ConductAction(Vector3 _hitPoint, Vector3 _forceVector, int _damageCustom = 0)
  - Designed to be usable during OnCollisionEnter.

Changed
- UV Map - All Items models from 3D Brakable Core Pack were again unvraped in Blender, as preparation for coming soon Fade Off Effect Dissolve 

Fixed  
- Object Respawn – Respawn time will be counted from end of Fade Off Effect allowing for proper reset of Item components.  
 

---

### [4.05] – 2025-06-27  
Summary: Bug fixes, global loot sound support, and new sample sounds.

Added  
- Global Loot Sound Array – assignable at a global level, with per-item override support  
- Free sample loot drop sounds  

Fixed  
- Object Pooling & FadeOffEffects – the main item part now remains in the scene after destruction (when neither pooling nor respawn is enabled)  
- Minor bugs  

---

### [4.04]  
Summary: Introduced Force Transfer on destroy and new demo scenes.

Added  
- Force Transfer on destroy  
- Two new demo scenes presenting Force Transfer  

---

### [4.03]
Summary: New AddForceOnCall component and bug fixes.

Added  
- AddForceOnCall component – allows adding force during item destruction in a predictive way  

Fixed  
- Minor bugs  

---

### [4.02]  
Summary: Flash effect improvements and preparations for expansion.

Added  
- Flash effect now works with mesh renderers under child transforms  

Changed  
- Internal changes in preparation for Lamps for 3D Breakable Core Pack  

---

### [4.01]
Summary: Demo scene fix and Unity package update.

Added  
- Unity 2021.3.7f1 support package  

Fixed  
- Demo scenes quick fix  

---

### [4.00]
Summary: Major redesign with Scriptable Objects, new pottery models, and updated documentation.

Added  
- New ActionType: Required Force  
- Items redesigned to use Scriptable Objects  
- Loot Items redesigned to use Scriptable Objects  
- New pottery models  
- Fully remade documentation  
- New “HowTo” YouTube tutorial series  

Changed  
- Asset design updated to support external addon packages  

---

### [3.03] 
Summary: Unity 6 support and bug fixes.

Fixed  
- Minor bugs  

Changed  
- Unity 6 readiness  

---

### [3.02]
Summary: New demo scene for raycast destruction.

Added  
- Scene 13 – Destroy by Raycast Hit  

---

### [3.01]
Summary: Prefab handling improvements and bug fixes.

Added  
- Custom items now support Fade Off Effects  

Fixed  
- Disabled “Generate Colliders” option for Mesh Import due to bugs  
- All prefabs now default to Layer: Default instead of Layer 31  
- Improved folder structure  

---

### [3.00] 
Summary: Major update with inspector redesign, new destruction features, and improved models.

Added  
- Remade custom inspectors for Destroyable_WholeItem and Destroyable Manager  
- Destroy Sounds feature  
- Object Spawner with override option  
- Loot Table algorithms: Roulette Wheel Selection / Independent Probability Checks  
- Fade Off feature (None / Disappear / Sink)  
- Respawn After Destruction  

Changed  
- Improved model topology  

---

### [2.24] 
Summary: Destroyable Manager auto-setup improvement.

Added  
- DestroyableManager (with default setup) is now auto-added if omitted  

---

### [2.23] 
Summary: Integration and bug fix update.

Fixed  
- Missing TAG error  

Changed  
- Destroyables moved to Layer 31 to simplify project integration  

---

### [2.22]
Summary: Scene adjustments and new rotation script.

Added  
- Item rotation script  

Fixed  
- Item rearrangements in Scene 1  
- Minor bugs  

---

### [2.21] 
Summary: Visual Scripting compatibility fix.

Fixed  
- Bug related to Unity.VisualScripting usage  

---

### [2.20]  
Summary: Major interaction expansion with new action types and explosions.

Added  
- Rewritten OnCollisionEnter with new ConditionTypes  
- ActionTypes: Destroy, DamageConstant, DamageRandom, ChanceRandom  
- Updated custom editors: Destroyable_Manager and Destroyable_WholeItem  
- Item Flash effect  
- Item-level overrides for Destroyable_Manager settings  
- Explosions and 6 explosive barrel items  
- Scene 8 – ClickToDestroy (Explosive Item)  
- Scripts for automating custom prefab setup  

Fixed  
- Pooling system bug where CustomFast items didn’t disappear  

Changed  
- Updated documentation  

---

### [2.10] 
Summary: Custom item workflow and demo improvements.

Added  
- Detailed demo scenes  
- Custom item support  
- New “HowTo” YouTube tutorials  

---

### [2.00]  
Summary: Major update with new items, rebranding, and visual improvements.

Added  
- 12 Wooden Barrels and 12 Wooden Boxes  
- Enhanced demo scenes  
- Improved Destroyable Manager with group sound assignment  

Changed  
- Asset renamed from 3D Breakable Pottery Lowpoly Pack → 3D Breakable Core Pack  
- All items repainted to match new CatBorg palette  

---

### [1.3] 
Summary: Added destruction sounds.

Added  
- 12 pottery breaking sound clips  
- Option to play destruction sound after item break  

---

### [1.2]
Summary: Scene and editor improvements.

Added  
- New scene demonstrating object pooling  
- Custom Editor visuals for DestroyableManager  

Changed  
- OnCollisionEnter behaviours (None, Destroy, SingleTagComparison, MultipleTagComparison)  

Fixed  
- Demo scenes updated for easier learning  

---

### [1.1]
Summary: Simplified collision-based destruction.

Added  
- User-friendly OnCollisionEnter behaviours  
- Scene 3 – OnCollision  
- Tutorial video demonstrating setup  

---

### [1.0.0] 
First Release  
