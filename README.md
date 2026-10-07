# OpenAnims

An animation-focused fork of [OpenCE](https://github.com/OpenCommunityEdition/OpenCE), the Halo: Combat Evolved port for Linux, Windows and Android.

OpenAnims enhances Halo: CE's vanilla animations. The goal is to fix the stiff, frozen or broken moments in the original animations while keeping the look and feel of the original game. It uses the game's own animation data, so no new assets are needed. Everything outside animation is the same as OpenCE.

<img width="480" height="270" alt="Enhanced animations (left) next to the original ones (right)" src="https://github.com/user-attachments/assets/6c67d2d3-8534-4981-b833-20ed406e13b0" />

*Enhanced animations (left) next to the original ones (right).*

## Goals

- Smoother transitions between animations
- Natural movement where the original freezes or snaps
- Correct poses in vehicles and special situations
- Faithful to the original game: enhanced, not replaced

## Enhancements so far

**Grenade throws**
- Legs keep running while you throw, and blend smoothly when you stop or change direction.
- Crouched throws stay crouched, and mid-air throws keep the floating jump legs.
- Your body turns with your aim while throwing.

**Vehicles**
- Warthog and Scorpion riders stay seated when throwing.
- Scorpion riders' arms are freed from the handles while throwing and reloading (Disables IK[Inverse Kinematics] until animations finish).
- Scorpion riders now have a reload animation.

Comparison video: https://www.youtube.com/watch?v=7Mald5-e3XA

More enhancements will follow. Changes are offered back to OpenCE as pull requests.

## Play and build

The game data, controls, multiplayer and build instructions are the same as
OpenCE's. Refer to the [OpenCE README](https://github.com/OpenCommunityEdition/OpenCE#readme).

If your own build closes at start-up, build it with the same settings as the
official downloads:

```
python configure.py --portable --lto=off --pgo=off
ninja windows
```

## Credits

All credit for the port goes to the
[OpenCE](https://github.com/OpenCommunityEdition/OpenCE) team and the
decompilation projects it builds on. OpenAnims only adds the animation
enhancements.
