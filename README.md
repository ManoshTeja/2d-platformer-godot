# 2D Platformer — Godot 4

A 2D side-scrolling platformer built from scratch in Godot 4 using GDScript.

## Controls
| Action | Keys |
|--------|------|
| Move Left | Arrow Left or A |
| Move Right | Arrow Right or D |
| Jump | Space Bar or Arrow Up |

## Gameplay
- Navigate platforms, avoid enemies, and collect as many coins as you can
- Fall into a killzone and trigger a slow-motion death effect before the scene reloads
- Score is tracked and displayed in real time as you collect coins

## Technical Features

**Player Controller**
- Physics-based movement with gravity integration and smooth deceleration via `move_toward()`
- Idle, run, and jump animation states driven by floor detection and input direction
- Sprite flipping based on movement direction

**Enemy AI**
- Patrol enemy using dual `RayCast2D` sensors to detect platform edges
- Automatically reverses direction and flips sprite to stay on platforms indefinitely

**Game Systems**
- Coin collection with `AnimationPlayer` pickup effect and real-time score tracking
- Global `GameManager` node tracks score and updates UI display
- Killzone mechanic: triggers slow-motion (`Engine.time_scale = 0.5`), waits via `Timer` node, then reloads the scene
- Collision shape cleanup on death to prevent re-triggering

## Built With
- Godot Engine 4
- GDScript
- 2D physics engine (CharacterBody2D, Area2D, RayCast2D)

## How to Run
1. Download and install [Godot 4](https://godotengine.org/download)
2. Clone this repo or download the ZIP
3. Open Godot, click "Import", and select the `project.godot` file
4. Press F5 to run

## Author
Manosh Teja Kanth Perumalla — CS Student at Virginia State University  
[LinkedIn](https://www.linkedin.com/in/manosh-teja-kanth)
