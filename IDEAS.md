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
- **Part size:** parts take up multiple slots and are always cuboid.
- **Heat:** tracked per part. Heat spreads between neighboring parts over time.
- **Slots:** unlimited. Ships will eventually grow bigger than stars.
- **Physics:** always on. Accelerate and decelerate carefully, especially with a cargo bay full of a body.
- **Converters:** fusion and fission converters take massive amounts of electricity, so the converter chain only works at huge scale.
- **Selling:** unused elements can be sold to stations for credits. Stations sell parts and part blueprints for credits.
- **Tiers:** each part tier is 1 block wider and 10x better than the last. Grinders and generators grow 2 blocks wider per tier and are still 10x better.

---

## Building

- **Copy and paste:** a feature.
- **Build time:** parts take 10 seconds by default. Some parts take longer.
- **Placing parts:** select a block from the build menu, then click a face of an existing block. The new block builds off that surface.

---

## Rare materials

Moved to `MATERIALS.md`.

---

## Space stations

- Stations are spread throughout space.
- Bring a station resources and it gives back rare materials.
- Alternatively, put a whole asteroid into a station's open cargo bay.

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

- Which rare materials do stations give out?
