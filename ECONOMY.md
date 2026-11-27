# Stardust: Economy

Credit prices and quest payouts. All numbers are placeholders to tune later, and they build off two anchors: a default quest pays 100 credits, and the player starts with 100 credits.

## Pricing rules

- **Elements are the keystone.** Each element has a price per 1 Mass, set by rarity tier. Everything else is built from those prices.
- **Every step adds 1.2x.** A material is worth the sum of the elements inside it, times 1.2. A material made from another material is worth its sum times 1.2 again. A part is worth the sum of its materials times 1.2 once more. The 1.2x stands for the effort and electricity of making it.
- **Equal shares.** Until recipe amounts are set, each input in a recipe is an equal share of the output's Mass. A material's price per Mass is the average of its inputs times 1.2.
- **Natural materials are priced by what they break down into.** The price is the sum of their elements, with no markup. See the breakdown tables in `MATERIALS.md`.
- **Rare materials** are priced like any made material, then times 10 as a rarity premium.
- **Parts:** every block needs 10 Mass of materials, split equally across the part's listed materials. A part's price is the sum of its materials times 1.2.
- **Stations:** they buy and sell elements and materials at exactly their value. They buy and sell parts at the part's price.

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

### Natural materials

Priced by their breakdown, with no markup.

| Material | Breakdown | Credits per Mass |
|---|---|---|
| Regolith | 40% Oxygen, 20% Silicon, 15% Aluminum, 10% Iron, 10% Calcium, 5% Titanium | 1.1 |
| Basalt | 45% Oxygen, 23% Silicon, 12% Iron, 8% Aluminum, 7% Calcium, 5% Magnesium | 1.0 |
| Water ice | 89% Oxygen, 11% Hydrogen | 1.0 |
| Ammonia | 82% Nitrogen, 18% Hydrogen | 1.0 |

Water ice and Ammonia can also be made from elements. When they are, they use the breakdown shares above and no markup.

### Made materials

Step 1 means made from elements only, and step 2 means made from a step 1 material.

| Material | Step | Credits per Mass |
|---|---|---|
| Polymer | 1 | 1.2 |
| Ceramic tile | 1 | 1.2 |
| Glass | 1 | 1.2 |
| Propellant | 1 | 1.2 |
| Graphite | 1 | 1.2 |
| Explosive charge | 1 | 1.2 |
| Steel | 1 | 1.2 |
| Aerogel | 1 | 1.2 |
| Titanium alloy | 1 | 2.4 |
| Copper wire | 1 | 3.6 |
| Carbon fiber | 2 | 1.3 |
| Radiator panel | 2 | 1.3 |
| Armor plating | 2 | 1.4 |
| Bearing | 2 | 1.4 |
| Regolith slug | 2 | 1.4 |
| Kinetic ammo | 2 | 2.5 |
| Superconductor coil | 2 | 2.8 |
| Actuator | 2 | 2.9 |
| Circuit board | 2 | 13.8 |
| Builder drone | 3 | 7.2 |

If a recipe lists alternatives, the first one is used for pricing.

### Rare materials

Recipe price times 1.2 per step, then times 10.

| Rare material | Credits per Mass |
|---|---|
| Helium-3 | 12 |
| Cryonite | 20 |
| Pyrium | 20 |
| Voidglass | 25 |
| Moovium | 28 |
| Starsteel | 64 |
| Neutronium | 78 |
| Gravitite | 78 |

Starsteel includes Helium-3 at its full price of 12, which is why it costs more than its other ingredients suggest.

---

## Parts

A part's price is 12 times the average price per Mass of its materials, per block. That's 10 Mass per block, times 1.2. Parts are 1 block unless stated otherwise.

Grinders and Refineries are 5 blocks wide. I assumed a 5 × 5 × 5 cube, 125 blocks, so their price is the per-block price times 125. Tell me if the depth should be different.

| Part | Price per block | Blocks | Tier 1 price |
|---|---|---|---|
| Fission converter | 35.2 | 1 | 35.2 |
| Heat sink | 14.4 | 1 | 14.4 |
| Radiator | 15.1 | 1 | 15.1 |
| Gyroscope | 15.8 | 1 | 15.8 |
| Reinforced hull | 17.3 | 1 | 17.3 |
| Storage bay | 21.6 | 1 | 21.6 |
| Thruster | 21.6 | 1 | 21.6 |
| Burner | 21.6 | 1 | 21.6 |
| Hull / Frame | 22.3 | 1 | 22.3 |
| Scoop | 22.3 | 1 | 22.3 |
| Fusion generator | 24.0 | 1 | 24.0 |
| Cargo bay | 24.5 | 1 | 24.5 |
| Charge launcher | 24.5 | 1 | 24.5 |
| Mooring clamp | 24.5 | 1 | 24.5 |
| Docking clamp | 24.5 | 1 | 24.5 |
| Drill | 25.2 | 1 | 25.2 |
| Insulation | 25.2 | 1 | 25.2 |
| Heat ejector | 25.9 | 1 | 25.9 |
| Mass cannon | 28.8 | 1 | 28.8 |
| Thermal generator | 28.8 | 1 | 28.8 |
| Fission generator | 28.8 | 1 | 28.8 |
| Coolant pump | 29.9 | 1 | 29.9 |
| Fabricator | 30.7 | 1 | 30.7 |
| Battery | 31.2 | 1 | 31.2 |
| Electrolysis | 36.0 | 1 | 36.0 |
| Lead plate | 36.0 | 1 | 36.0 |
| Solar generator | 64.2 | 1 | 64.2 |
| Sensor array | 64.2 | 1 | 64.2 |
| Assembler | 71.7 | 1 | 71.7 |
| Builder bay | 71.7 | 1 | 71.7 |
| Transport bay | 71.7 | 1 | 71.7 |
| Laser cannon | 74.6 | 1 | 74.6 |
| Fusion converter | 78.6 | 1 | 78.6 |
| Autopilot | 104.6 | 1 | 104.6 |
| Shield generator | 168.0 | 1 | 168.0 |
| Warp drive | 184.8 | 1 | 184.8 |
| Hyperdrive | 251.0 | 1 | 251.0 |
| Tractor beam | 336.0 | 1 | 336.0 |
| Grinder | 15.8 | 125 | 1,980 |
| Refinery | 21.1 | 125 | 2,640 |

Specialized producers aren't sold, so they have no price.

- **Starting credits:** the 100 starting credits buy a Fabricator (30.7), with enough left for a few cheap parts.
- **Tiers:** each tier costs 9x the one before, matching the material cost rule. A Fabricator is 30.7, then 276, then 2,487 credits.
- **Blueprints:** a blueprint costs 10x the part price for the same tier. A tier 1 Fabricator blueprint is about 307 credits.

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
| Regolith covering | 40% | 400 | 1.1 | 440 |
| Iron | 30% | 300 | 1 | 300 |
| Nickel | 20% | 200 | 3 | 600 |
| Silicon | 10% | 100 | 1 | 100 |
| **Whole body** | | **1,000** | | **1,440** |

- **Body delivery quest:** 2x the whole body is 2,880 credits.
- **Mining only the wanted Nickel:** 200 Mass delivered at 2x is 1,200 credits.
- **Selling the whole body to a Cargo station:** pays for the full Mass at market, 1,440 credits.

Moving the whole body pays more than twice as much as mining the part they want, which is the reason to put in the effort.

---

## Things to watch

- **Buy and craft loop:** stations sell matter at its value and buy made goods at 1.2x per step. Buying elements, crafting them into a part and selling it returns about 1.7x the elements' cost, limited only by build and crafting time. The 1.2x is meant to cover electricity, but electricity has no price here, so nothing stops the loop except how fast you can craft.
- **Converters:** a converter can turn cheap elements into pricier ones, like 9 Helium (9 credits) into 4 Beryllium (12 credits). Massive electricity is the only limit.
- **Cheap parts:** most parts cost 15 to 100 credits per block, which is a fraction of one quest. Only Grinders and Refineries, and the Moovium and Voidglass parts, cost much more.
- **Lead plates:** at 36 credits each, covering both faces of a 5-wide part takes 50 plates and 1,800 credits.
