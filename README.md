# Swords of Vengeance

A third-person action-RPG prototype built in **Unity (2019.4 LTS)** with C#.
Developed July–September 2024 as a personal project to explore core RPG systems:
combat, AI enemies, navigation, scene transitions and a custom fire-propagation system.

> Status: playable prototype (v0.4)

## Gameplay

- Point-and-click / WASD player movement using Unity's NavMesh
- Melee and ranged combat with weapon pickups and projectiles
- Enemy AI with patrol paths, chase and attack behaviour
- Health, damage and death handling for player and enemies
- Scene transitions through portals with fade in/out
- Cinematic trigger sequences
- Dynamic, grid-based **fire propagation** system that spreads across terrain

## My code

All gameplay logic I wrote lives in [`Assets/Scripts`](Assets/Scripts):

| Folder | Responsibility |
|---|---|
| `Combat` | `Fighter`, `Weapon`, `Projectile`, `WeaponPickup`, `CombatTarget` |
| `Controller` | `PlayerController`, `AIController`, `PatrolPath` |
| `Core` | `Health`, `ActionScheduler`, `FollowCamera`, `PersistantObjectSpawner` |
| `Movement` | character movement |
| `SceneManagement` | `Portal`, `Fader` |
| `Cinematics` | `CinematicTrigger`, `CinematicControlRemover` |

The `FirePropagation` system (`FireGrid`, `FireCell`, `FireManager`, `FireIgniter`, …)
implements cellular fire spreading over a terrain grid.

## Third-party assets

This repository includes free/sample asset packs (AQUAS-Lite, BOXOPHOBIC, Vefects,
RPG Pack and environment assets) used only to build the playable scene. All rights
belong to their respective authors; they are included here solely to keep the
prototype runnable.

## Running the project

1. Install **Unity 2019.4.16f1** (via Unity Hub).
2. Clone this repository and open the folder as a Unity project.
3. Open a scene from `Assets/Scenes` and press Play.

> Unity regenerates the `Library/` folder automatically on first open, so it is
> intentionally not committed.

## Tech

- Unity 2019.4 LTS · C#
- NavMesh navigation · Animator · Cinemachine-style follow camera
