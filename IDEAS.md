# Stardust: Ideas

A scratch space for thoughts before building anything. Nothing here is decided.

Space game about harvesting asteroids, moons, planets, and stars, all while making yourself into a technological celestial body.

---

## Game

- Single-player.
- Endless sandbox. Your rank title and the percentage to the next rank are the main milestones.
- The universe is procedurally generated from a seed, using the spawn weights in `BODIES.md` and `POIS.md`.
- All ships you own keep running in real time while you control a different one.

---

## Ships

Ships are made of modular parts. The full parts list, with cost to make and cost to use, is in `PARTS.md`.

---

## Notes

- **Matter:** any element or material that gets harvested, such as iron, silicon, helium, or hydrogen.
- **Grinders:** always have odd funnels that make resource gathering more challenging. The funnel is a fixed odd shape, and only matter passing through its opening is collected, so facing and mooring matter. They're massive: 5 blocks wide, even the weakest one. This encourages moving bodies to stations.
- **Part size:** parts are 1 block unless stated otherwise. Parts can take up multiple slots and are always cuboid.
- **Heat:** tracked per part. Heat spreads between neighboring parts over time. An overheated part shuts down until it cools to ambient temperature (21°C).
- **Radiators:** a radiator needs a face open to space, and its output scales with how much of its surface is exposed. Big ships have a heat problem deep inside, so surface area becomes a design goal.
- **Stars:** heat rises the closer you get. Cooling, Insulation, and Starsteel let you go nearer, and overheated parts shut down. The danger is a gradual limit, not a wall.
- **Distances:** asteroid fields and moons sit in clusters near stations, with long empty gaps between regions. Local play is slow and tactile, and hyperdrive is for crossing the gaps.
- **Hazards:** environmental only, and nothing hunts you. See Hazards below.
- **Slots:** unlimited. Ships will eventually grow bigger than stars.
- **Physics:** always on. Accelerate and decelerate carefully, especially with a cargo bay full of a body.
- **Converters:** fusion and fission converters take massive amounts of electricity, so the converter chain only works at huge scale.
- **Stock:** tracked per ship.
- **Mining tools:** the mass cannon, laser cannon, and charge launcher are mining tools, not combat weapons.
- **Mass cannon:** chips pieces off a body for drills and grinders to work on. Kinetic ammo is the cost.
- **Laser cannon:** slices a body precisely in a chosen direction, using heat and electricity.
- **Charge launcher:** charges explode 10 seconds after launch and shatter a body into many pieces. Cheap, but messy.
- **Starting out:** players get their first Fabricator and Assembler from stations, since both need level 2 materials to build.
- **Selling:** unused elements can be sold to stations for credits. Stations sell parts and part blueprints for credits. Stations buy at 0.8x of an item's value and sell at full value. A blueprint unlocks building that part yourself, and you can still buy finished parts from stations without it.
- **Credits:** prices and quest payouts are in `ECONOMY.md`. Elements are priced per Mass by rarity tier. Materials and parts are worth the sum of what's inside them, times 1.2 for each step.
- **Tiers:** there are 10 size tiers for now, and more may be added later, so the rule is a formula. A part is a cube, and its width is its starting width plus 2 for each tier above the first. Most parts start at 1 wide, so a Radiator goes 1, 3, 5, and so on up to 19 wide (19×19×19). Generators and converters start at 3 wide and reach 21 wide at tier 10. The Grinder and Refinery start at 5 wide (5×5×5) and reach 23 wide at tier 10. Material cost, output, heat, and power use all scale with the part's block count. Output also gets a small bonus for bigger parts, a placeholder 1.1x for each tier above the first, so one big part beats the same volume of small parts a little and is easier to manage.

---

## Building

- **Copy and paste:** a feature.
- **Build time:** parts take 10 seconds by default. Some parts take longer.
- **Placing parts:** select a block from the build menu, then click a face of an existing block. The new block builds off that surface.
- **Builder drones:** a Builder bay releases 1 drone per part being built. Each drone launches outward, curves toward the construction, and returns when it's done.
- **Facing:** every part snaps to the 3D grid and rotates in 90° steps before you place it.
- **Connections:** electricity and storage are ship-wide pools. Only heat depends on neighboring parts.
- **Damage:** collisions can destroy blocks, and Reinforced hull is immune. Blocks that lose their connection to the ship drift away as loose bodies.
- **Paying:** the full cost leaves ship storage when you place a block. Cancelling a block that's still waiting for a drone refunds it.
- **Flight model:** full center of mass and torque. Block mass shifts the center of mass, and off-center thrust spins the ship, so thruster placement and gyroscopes matter.
- **Sizes:** every part has a fixed size per tier. Parts aren't stretchable, except Lead plates, which scale in width like other parts but stay 1 block deep: 1×1×1, 3×3×1, 5×5×1, 7×7×1, and so on.
- **Build timing:** you can build at any time, even while flying. Drones chase the ship.
- **Builder bay capacity:** each Builder bay holds a set number of drones, and higher tiers hold 10x more. More bays means faster building.
- **Block mass:** a block weighs what its materials weigh (its cost to make, in mass units). Material choices change how a ship flies.
- **Camera:** free orbit camera. A translucent ghost of the part follows your cursor onto the face you point at.
- **Copy and paste:** box-select blocks and copy them. Paste as a ghost you can rotate and move, then confirm. The full cost is taken from storage and drones build it.
- **Removing blocks:** drones take the part off and bring it back to storage as a part. You can hold parts in storage and place them later, the same as parts bought from stations.
- **Stored parts:** they use storage space by mass, the same unit as matter.
- **Placing stored parts:** placing a part you already have takes the part's normal build time.
- **Unlocking tiers:** each tier of each part is its own blueprint, bought at trade stations. You rebuild larger and the old part goes back to storage.
- **Selling parts:** stations buy parts at full price, the same as they sell them for.
- **Loose blocks:** blocks broken off by a collision drift as salvage. You can recover them with a tractor beam or cargo bay.
- **Starting ship:** a tiny working ship with a hull, a thruster, a small storage bay, a battery, a solar generator, and a tier 1 grinder. You can mine right away, then buy your first Fabricator and Assembler. A trade station is in sight at the start, so the first loop is mine a nearby body, sell elements there, and buy your first machines.
- **Drones:** Builder drones can't be lost. They always return safely.
- **Mass units:** the unit is called Mass. It's an abstract unit, and scales are fudged heavily since whole solar systems can't be simulated accurately.

---

## Celestial bodies

Body types, what they're made of, and spawn weights are in `BODIES.md`.

---

## Celestial ranks

- Your ship's total mass sets your title: Asteroid, then Moon, Planet, and Star.
- A simple display shows your current title and the percentage of the way to the next rank.
- Ranks are just titles. They don't unlock anything.

---

## Hazards

Environmental only. Nothing hunts you.

- **Radiation:** comes from fission sources and stars, and makes you lose control briefly.
  - Thrusters fire randomly for 1–3 seconds every 5–15 seconds.
  - Gyroscopes and other control parts malfunction, and the ship turns and rotates in random directions for 1–3 seconds every 5–15 seconds.
  - Each control part can go off randomly if it's unprotected.
  - Lead plates protect a part when they cover its entire face, on at least two faces. A part 5 blocks wide needs 25 Lead plates on one face and 25 on another. Lead plates scale in width but not depth (1×1×1, 3×3×1, 5×5×1, 7×7×1, and so on) and cost the same per block.
- **Solar flares:** cause massive heat in exposed ship parts and rapidly drain your batteries. Shield generators protect parts and batteries in range from the effects of flares.
- **Gravity:** strong gravity near big bodies.
- **Volatile packages:** a quest hazard. See `POIS.md`.

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
- Transfers: from the vessel list, a ship with a Transport bay can send matter or parts to any other ship you own. The Transport bay launches a storage drone to the destination. Each launch costs a low amount of materials, plus electricity that scales with distance. The electricity cost rises exponentially past a short range, so ships are encouraged to stay close.

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

- What does the early game look like after the starting ship?
- Units are measured in Mass. How does mined element Mass turn into material amounts? This decides the amounts in material recipes.
- Do Specialized producers need their rare material's recipe inputs, or do they make it from nothing?
- What mass does each celestial rank need?
- Gas giants, comets, and neutron stars are named as harvest sources but aren't in `BODIES.md` yet. Should they be added?
- What's the right size bonus for bigger parts? The placeholder is 1.1x output for each tier above the first.
