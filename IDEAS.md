# Stardust: Ideas

A scratch space for thoughts before building anything. Nothing here is decided.

Space game about harvesting asteroids, moons, planets, and stars, all while making yourself into a technological celestial body.

---

## Ships

Ships are made of modular parts. The full parts list, with cost to make and cost to use, is in `PARTS.md`.

---

## Notes

- **Matter:** any element or material that gets harvested, such as iron, silicon, helium, or hydrogen.
- **Grinders:** always have odd funnels that make resource gathering more challenging. They're massive: 5 blocks wide, even the weakest one. This encourages moving bodies to stations.
- **Part size:** parts are 1 block unless stated otherwise. Parts can take up multiple slots and are always cuboid.
- **Heat:** tracked per part. Heat spreads between neighboring parts over time. An overheated part shuts down until it cools to ambient temperature (21°C).
- **Slots:** unlimited. Ships will eventually grow bigger than stars.
- **Physics:** always on. Accelerate and decelerate carefully, especially with a cargo bay full of a body.
- **Converters:** fusion and fission converters take massive amounts of electricity, so the converter chain only works at huge scale.
- **Stock:** tracked per ship.
- **Mining tools:** the mass cannon, laser cannon, and charge launcher are mining tools, not combat weapons.
- **Starting out:** players get their first Fabricator and Assembler from stations, since both need level 2 materials to build.
- **Selling:** unused elements can be sold to stations for credits. Stations sell parts and part blueprints for credits.
- **Credits:** each element has a base price from its atomic weight times a rarity multiplier. Exact numbers wait on the mass units question below.
- **Tiers:** each part tier is 1 block wider than the last, and its output, heat, and power use all go up 10x. Grinders and generators grow 2 blocks wider per tier, with the same 10x. Material cost goes up 9x per tier, so one big part is slightly cheaper than ten small ones and easier to manage.

---

## Building

- **Copy and paste:** a feature.
- **Build time:** parts take 10 seconds by default. Some parts take longer.
- **Placing parts:** select a block from the build menu, then click a face of an existing block. The new block builds off that surface.
- **Builder drones:** a Builder bay releases 1 drone per part being built. Each drone launches outward, curves toward the construction, and returns when it's done.

---

## Celestial bodies

Body types, what they're made of, and spawn weights are in `BODIES.md`.

---

## Celestial ranks

- Your ship's total mass sets your title: Asteroid, then Moon, Planet, and Star.
- A simple display shows your current title and the percentage of the way to the next rank.
- Ranks are just titles. They don't unlock anything.

---

## Space stations

Station types and spawn weights are in `POIS.md`.

- Stations are spread throughout space.
- Bring an Exchange station resources and it gives back rare materials.
- Put a whole body into a Cargo station's open cargo bay and get paid credits for its full mass. There are no fees, only what it cost you to move it. Stations are excited to receive bodies.

---

## Control

- Build multiple ships.
- Detach control from a ship and control any ship you own.
- No limit on how far away you can control a ship from.
- Vessel list: a rearrangeable, scrollable, foldable list of the vessels you own. It shows each vessel's current activity and lets you take control of one.

---

## Crafting menu

- Lists every recipe you've unlocked, for parts and materials.
- Each recipe has a min/max double slider for auto production. When stock drops to the min, crafting starts. When stock reaches the max, it stops. The min can't go above the max.
- Groups: make custom groups and fold or unfold each one.
- Each group has an on/off switch that toggles all of its recipes at once.
- Drag recipes between groups to move them.
- Paint-drag to set machines, like Rimworld's work priority menu: click and hold a recipe in one machine's slot, then drag across other machines' slots. Each slot the drag passes over is set to that recipe. Example: in a line of 5 unset fabricators, set one to Kinetic ammo, drag from it across the other 4, and all 5 are set to Kinetic ammo.

---

## Open questions

- Which rare materials does each Exchange station give out?
- What's the starting ship, and what does the early game look like?
- Stock is per ship, so how do ships transfer matter and parts between each other?
- Units will be measured by mass. How does mined element mass turn into material amounts? This decides the amounts in material recipes.
- Do Specialized producers need their rare material's recipe inputs, or do they make it from nothing?
- What mass does each celestial rank need?
- Gas giants, comets, and neutron stars are named as harvest sources but aren't in `BODIES.md` yet. Should they be added?
