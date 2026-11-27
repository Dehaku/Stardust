# Stardust: Parts

Modular ship parts. Parts are 1 block unless their function says otherwise. They can take up multiple slots and are always cuboid.

**Cost to make:** the materials and elements it takes to build the part. Every material used is listed in `MATERIALS.md`, and recipes follow the intermediary limit in that file.
**Cost to use:** what the part consumes while running. **None** means it uses nothing. Electricity is given in kW, MW, or GW.
**Heat made:** how much heat the part makes while running: None, Low, Medium, High, or Intense.
**Alternatives:** items in brackets are options, and any one of them works. For example, `[Lithium, Zinc]` means either Lithium or Zinc.
**Tiers:** all values are for tier 1. Each tier up is 10x better and uses 10x the power and makes 10x the heat. Material cost goes up 9x. See IDEAS.md Notes.

| Part | Function | Cost to make | Cost to use | Heat made |
|---|---|---|---|---|
| Hull / Frame | Structural base that other parts attach to | Titanium alloy, Carbon fiber | None | None |
| Reinforced hull | Hull block that's immune to collision damage. Useful for ramming and moving bodies kinetically | Armor plating | None | None |
| Storage bay | Raises maximum matter capacity | Titanium alloy, Polymer | None | None |
| Cargo bay | Carries whole bodies, if it can close on one | Steel, Actuator | 10 kW | None |
| Grinder | Slowly melts bodies in its grind range, collecting matter as the body shrinks. Funnel-shaped intake with a fixed odd shape, and only matter passing through its opening is collected. Massive: 5 blocks wide, even the weakest one (see IDEAS.md Notes) | Steel, Bearing | 100 kW | High |
| Drill | Turns a big body into multiple smaller ones, losing some mass in the process | Tungsten, Steel | 1 kW | Medium |
| Mass cannon | Mining tool. Chips pieces off a body for drills and grinders to work on | Steel, Copper wire | [Kinetic ammo, Regolith slug] | Low |
| Laser cannon | Mining tool. Slices a body precisely in a chosen direction | Glass, Copper wire, Circuit board | 1 MW | High |
| Charge launcher | Mining tool. Launches explosive charges that go off 10 seconds later and shatter a body into many pieces. Cheap, but messy | Steel, Actuator | Explosive charge | Low |
| Tractor beam | Moves matter without touching it | Moovium | 100 kW | Low |
| Thruster | Gives speed | Titanium alloy, Ceramic tile | Propellant | High |
| Fusion converter | Fuses lighter elements into heavier ones | Superconductor coil, Circuit board, Tungsten | 1 GW | Intense |
| Fission converter | Breaks elements into smaller elements | Superconductor coil, Boron, Lead | 1 GW | Intense |
| Fabricator | Makes level 1 materials (made only from elements) | Steel, Actuator, Copper wire | 100 kW | Medium |
| Assembler | Makes level 2 materials (made from level 1 materials), plus Builder drones (level 3) | Circuit board, Actuator, Steel | 100 kW | Medium |
| Builder bay | Holds Builder drones and releases 1 per part being built. Each drone launches outward, curves toward the construction, and returns when it's done | Steel, Actuator, Circuit board | 100 kW | Low |
| Transport bay | Launches a storage drone carrying matter or parts to another ship you own. The sending ship needs one | Steel, Actuator, Circuit board | A low amount of materials per launch, plus electricity that scales with distance and rises exponentially past a short range | Low |
| Electrolysis | Turns water ice into hydrogen and oxygen, and ammonia into nitrogen and hydrogen | Copper wire, Titanium alloy | 100 kW | Low |
| Heat sink | Holds more heat before reaching dangerous levels | Graphite, Ceramic tile | None | None (stores heat) |
| Radiator | Dissipates heat into space. Needs a face open to space, and output scales with how much surface is exposed | Radiator panel, Steel | None | None (removes heat) |
| Insulation | Resists 95% of temperature exchange with neighboring parts | Aerogel, Tungsten | None | None |
| Lead plate | Blocks radiation. A part is protected when its entire face is covered, on at least two faces. A part 5 blocks wide needs 25 plates on one face and 25 on another | Lead | None | None |
| Heat ejector | Launches hot matter out, heavily lowering heat | Titanium alloy, Ceramic tile, Actuator | Matter | None (removes heat) |
| Coolant pump | Moves heat from one part to another on purpose. Built with Cryonite, it moves heat 10x better than with Ammonia or Water ice | Actuator, Copper wire, [Ammonia, Water ice, Cryonite] | 10 kW | None |
| Battery | Increases ship electricity capacity, in tiers from kilowatts to gigawatts and up | [Lithium, Zinc], Copper wire, Polymer | None | Low |
| Solar generator | Makes electricity from a nearby star. Output rises the closer it is and the more it faces the star directly | Glass, Circuit board, Silicon | None | Low |
| Thermal generator | Slowly turns high heat into electricity | Copper wire, Titanium alloy, Graphite | None | None (uses heat) |
| Burner | Makes a lot of heat out of matter | Ceramic tile, Titanium alloy | Pyrium (most heat), or Hydrogen and Oxygen (less heat) | High |
| Fission generator | Makes intense heat out of radioactive material | Lead, Boron, Steel | Uranium | Intense |
| Fusion generator | Makes intense heat out of very little, rare, matter | Superconductor coil, Ceramic tile | Helium-3 | Intense |
| Warp drive | Teleports the vessel | Moovium, Superconductor coil | 1 MW | High |
| Hyperdrive | Lets the vessel go really fast, as long as it's on | Moovium, Circuit board | 1 MW | High |
| Scoop | Collects trace matter from open space, or lots of matter from gas giants and stars, including helium-3 | Titanium alloy, Carbon fiber | 10 kW | Medium |
| Shield generator | Absorbs damage, and protects parts and batteries in range from the effects of solar flares | Superconductor coil, Voidglass | 100 kW | Medium |
| Sensor array | Reveals bodies at range and shows their matter makeup | Glass, Circuit board, Silicon | 10 kW | Low |
| Autopilot | Holds a course or station so you can work on other vessels | Circuit board, Copper wire | 1 kW | None |
| Gyroscope | Rotates the ship without thrust | Bearing, Steel | 10 kW | Low |
| Refinery | Breaks down natural materials, like regolith and basalt, into elements. Doesn't handle water ice or ammonia, which go through electrolysis. Massive: 5 blocks wide, even the weakest one, like the grinder | Steel, Actuator, Ceramic tile | 100 kW | Medium |
| Mooring clamp | Holds a body steady for drills and grinders | Steel, Actuator | 10 kW | None |
| Docking clamp | Joins two vessels so they move as one | Steel, Actuator | 1 kW | None |

---

## Specialized producers

Each one makes a single rare material. They can't be built. They're gained from station quests or by looting derelict ships in the void (rare POIs, see POIS.md). Their running cost is low.

| Part | Function | Cost to make | Cost to use | Heat made |
|---|---|---|---|---|
| Specialized producer [Moovium] | Makes Moovium only | Not buildable | 1 kW | Low |
| Specialized producer [Helium-3] | Makes Helium-3 only | Not buildable | 1 kW | Low |
| Specialized producer [Cryonite] | Makes Cryonite only | Not buildable | 1 kW | Low |
| Specialized producer [Neutronium] | Makes Neutronium only | Not buildable | 1 kW | Low |
| Specialized producer [Pyrium] | Makes Pyrium only | Not buildable | 1 kW | Low |
| Specialized producer [Voidglass] | Makes Voidglass only | Not buildable | 1 kW | Low |
| Specialized producer [Gravitite] | Makes Gravitite only | Not buildable | 1 kW | Low |
| Specialized producer [Starsteel] | Makes Starsteel only | Not buildable | 1 kW | Low |
