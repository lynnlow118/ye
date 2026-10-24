# ORBITAL // Mission Designer

A zero-dependency browser prototype for a visual, interactive space-mission design game.

## Run it

Open `index.html` in a browser. It uses native HTML/CSS/JavaScript and does not require a build step.

For a local server, use any static server, for example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/space-mission-game/`.

## Current vertical slice

- Visual home screen with central Start Mission and What is this? actions
- Random assignment from 10 missions
- Mission briefing before spacecraft design
- Interactive shipyard with five subsystem categories:
  - propulsion
  - power
  - communications
  - science instrument
  - shielding
- CSS 3D spacecraft model with rotating inspection and zoom
- Visible trade-offs for mass, budget, power, fuel, reach, and reliability
- Launch sequence handoff
- Mission cockpit with radar, beacon, telemetry, and keyboard flight controls
- Failure/repair interaction
- Mission completion loop with persistent archive progress across all 10 missions
- Final archive-complete state with Play again reset flow

## Controls

- Shipyard: drag over the ship to rotate; scroll to zoom; click system cards to swap parts.
- Flight: use W/A/S/D or Arrow Up/Down to pilot and advance the mission.
- Mission tool: open the tool panel when a system event appears; choose a repair response.
- Progress: the home screen shows archived missions; after all 10 are complete, Play again resets the archive.

## NASA grounding used for the prototype

The game’s subsystem model is based on NASA’s overview of common spacecraft systems: structure, data handling, thermal control, attitude and articulation control, telecommunications, electrical power and distribution, and propulsion.

- NASA Science, “Chapter 11: Onboard Systems”:
  https://science.nasa.gov/learn/basics-of-space-flight/chapter11-1/
- NASA JPL Education, “Marsbound! Mission to the Red Planet”:
  https://www.jpl.nasa.gov/edu/resources/lesson-plan/marsbound-mission-to-the-red-planet/

The exact part values in this prototype are deliberately game-balanced rather than flight-certified engineering data. For a classroom release, label all values as simulated and add a teacher-facing reference layer.

## Recommended next upgrade

Move the ship renderer to Three.js or Babylon.js for true mesh-based parts, glTF assets, lighting, orbital scenes, particle effects, and cinematic camera paths. Keep the game state and mission data model in JavaScript, then replace the CSS spacecraft renderer and scene backgrounds one system at a time.
