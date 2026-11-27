# Stardust: Economy

Credit prices and quest payouts. All numbers are placeholders to tune later, and they build off two anchors: a default quest pays 100 credits, and the player starts with 100 credits.

Elements are priced by rarity tier (approach 1), materials by their recipe (approach 2), and parts and blueprints by price class anchored on the starting 100 credits (approach 4).

---

## Elements

Priced per 1 Mass, by rarity tier.

| Tier | Credits per Mass |
|---|---|
| Common | 1 |
| Uncommon | 3 |
| Rare | 10 |
| Very rare | 30 |

| Element | Tier | Credits per Mass |
|---|---|---|
| Hydrogen | Common | 1 |
| Helium | Common | 1 |
| Lithium | Uncommon | 3 |
| Beryllium | Uncommon | 3 |
| Boron | Uncommon | 3 |
| Carbon | Common | 1 |
| Nitrogen | Common | 1 |
| Oxygen | Common | 1 |
| Fluorine | Rare | 10 |
| Neon | Uncommon | 3 |
| Magnesium | Common | 1 |
| Aluminum | Common | 1 |
| Silicon | Common | 1 |
| Phosphorus | Uncommon | 3 |
| Sulfur | Common | 1 |
| Chlorine | Uncommon | 3 |
| Argon | Uncommon | 3 |
| Potassium | Uncommon | 3 |
| Calcium | Common | 1 |
| Titanium | Uncommon | 3 |
| Chromium | Uncommon | 3 |
| Manganese | Uncommon | 3 |
| Iron | Common | 1 |
| Nickel | Uncommon | 3 |
| Copper | Uncommon | 3 |
| Zinc | Uncommon | 3 |
| Tungsten | Uncommon | 3 |
| Platinum | Rare | 10 |
| Gold | Very rare | 30 |
| Uranium | Rare | 10 |
| Lead | Uncommon | 3 |
| Neodymium | Rare | 10 |

---

## Materials

Priced per 1 Mass.

- **Found materials** use a flat price: Regolith 0.5, Basalt 1, Water ice 1.
- **Made materials** cost the average price of their inputs times 1.2, a 20% markup for each step. Until recipe amounts are set, each input counts as an equal share of the Mass. If a recipe lists alternatives, the first one is used.

| Material | Credits per Mass |
|---|---|
| Regolith | 0.5 |
| Basalt | 1 |
| Water ice | 1 |
| Polymer | 1.2 |
| Ceramic tile | 1.2 |
| Glass | 1.2 |
| Propellant | 1.2 |
| Ammonia | 1.2 |
| Graphite | 1.2 |
| Explosive charge | 1.2 |
| Steel | 1.2 |
| Aerogel | 1.2 |
| Carbon fiber | 1.3 |
| Radiator panel | 1.3 |
| Armor plating | 1.4 |
| Bearing | 1.4 |
| Regolith slug | 1.0 |
| Titanium alloy | 2.4 |
| Kinetic ammo | 2.5 |
| Superconductor coil | 2.8 |
| Actuator | 2.9 |
| Copper wire | 3.6 |
| Builder drone | 7.2 |
| Circuit board | 13.8 |

### Rare materials

Priced like a made material, then times 10 because they're not meant to be easily produced.

| Rare material | Credits per Mass |
|---|---|
| Helium-3 | 12 |
| Cryonite | 20 |
| Pyrium | 20 |
| Starsteel | 21 |
| Voidglass | 25 |
| Moovium | 28 |
| Neutronium | 78 |
| Gravitite | 78 |

---

## Parts and blueprints

Each part has a price class, and a tier 1 part costs the class price.

| Class | Tier 1 price | Parts |
|---|---|---|
| Block | 10 | Hull / Frame, Lead plate, Storage bay |
| Basic | 50 | Reinforced hull, Heat sink, Radiator, Insulation, Battery, Mooring clamp, Docking clamp, Thermal generator |
| Standard | 100 | Cargo bay, Drill, Mass cannon, Charge launcher, Thruster, Gyroscope, Autopilot, Electrolysis, Scoop, Sensor array, Coolant pump, Heat ejector, Solar generator, Burner, Fabricator |
| Advanced | 300 | Grinder, Refinery, Laser cannon, Assembler, Builder bay, Transport bay, Shield generator, Tractor beam |
| Heavy | 1,000 | Fusion converter, Fission converter, Fission generator, Fusion generator, Warp drive, Hyperdrive |

Specialized producers aren't sold, so they have no price.

- **Tiers:** each tier costs 9x the one before, matching the material cost rule. A Standard part is 100, then 900, 8,100, and 72,900 credits.
- **Blueprints:** a blueprint costs 10x the part price for the same tier. A tier 1 Standard blueprint is 1,000 credits.
- **Selling parts:** stations buy parts at their full price.

---

## Quests

A default quest pays 100 credits.

| Quest | Payout | Example |
|---|---|---|
| Delivery | 2x market price for the matter they want, until their goal is satisfied | A goal of 50 Mass of Iron at 1 credit pays 100 credits |
| Body delivery | 2x the value of the whole body, as long as it has some of what they want | See the body example below |
| Volatile packages | 2x a Delivery quest | The same 50 Mass of Iron goal pays 200 credits |
| Clearing | Same as Volatile packages | 200 credits for the default size |

### Body value

A body's value is every element and material in it, including its covering, at the prices above. The station pays 2x that total for a body it asked for.

Example: a 1,000 Mass asteroid, covered in regolith.

| Part of the body | Share | Mass | Credits per Mass | Value |
|---|---|---|---|---|
| Regolith covering | 40% | 400 | 0.5 | 200 |
| Iron | 30% | 300 | 1 | 300 |
| Nickel | 20% | 200 | 3 | 600 |
| Silicon | 10% | 100 | 1 | 100 |
| **Whole body** | | **1,000** | | **1,200** |

- **Body delivery quest:** 2x the whole body is 2,400 credits.
- **Mining only the wanted Nickel:** 200 Mass delivered at 2x is 1,200 credits.
- **Selling the whole body to a Cargo station:** pays for the full Mass at market, 1,200 credits.

Moving the whole body pays twice as much as mining the part they want, which is the reason to put in the effort.

---

## Things to watch

- **Converters and value:** a converter can turn cheap elements into pricier ones. For example, 9 Helium (9 credits) becomes 4 Beryllium (12 credits). The massive electricity cost has to outweigh the credit gain, so electricity needs a price too.
- **Full-price part sales:** parts built from materials worth a few credits sell for 10 to 1,000. If a player can craft a part and sell it at the station price, that's a profit loop. A cap on how many parts a station will buy, or a lower buy price, would stop it.
- **Equal input shares:** material prices assume each recipe input is an equal share of Mass. They'll change when recipe amounts are set.
