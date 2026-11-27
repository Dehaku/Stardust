# Stardust: Economy

Credit prices and quest payouts. All numbers are placeholders to tune later, and they build off two anchors: a default quest pays 100 credits, and the player starts with 100 credits.

## Pricing rules

- **Elements are the keystone.** Each element has a price per 1 Mass, set by rarity tier. Everything else is built from those prices.
- **Every step adds 1.2x.** A material is worth the sum of the elements inside it, times 1.2. A material made from another material is worth its sum times 1.2 again. A part is worth the sum of its materials times 1.2 once more. The 1.2x stands for the effort and electricity of making it.
- **Equal shares.** Until recipe amounts are set, each input in a recipe is an equal share of the output's Mass. A material's price per Mass is the average of its inputs times 1.2.
- **Natural materials are priced by what they break down into.** The price is the sum of their elements, with no markup. See the breakdown tables in `MATERIALS.md`.
- **Rare materials** are priced like any made material, then times 10 as a rarity premium.
- **Parts:** every block needs 10 Mass of materials, split equally across the part's listed materials. A part's price is the sum of its materials times 1.2.
- **Stations:** they sell elements, materials, and parts at full value, and buy them at 0.8x. Quest payouts use full value, not the 0.8x buy rate.

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

Grinders and Refineries are 5 × 5 × 5 cubes, 125 blocks, so their price is the per-block price times 125. Generators and converters start at 3 × 3 × 3, 27 blocks, so their price is the per-block price times 27. The Solar generator is flat, 3 × 3 × 1, 9 blocks, so its price is the per-block price times 9.

| Part | Price per block | Blocks | Tier 1 price |
|---|---|---|---|
| Fission converter | 35.2 | 27 | 950.4 |
| Heat sink | 14.4 | 1 | 14.4 |
| Radiator | 15.1 | 1 | 15.1 |
| Gyroscope | 15.8 | 1 | 15.8 |
| Reinforced hull | 17.3 | 1 | 17.3 |
| Storage bay | 21.6 | 1 | 21.6 |
| Thruster | 21.6 | 1 | 21.6 |
| Burner | 21.6 | 1 | 21.6 |
| Hull / Frame | 22.3 | 1 | 22.3 |
| Scoop | 22.3 | 1 | 22.3 |
| Fusion generator | 24.0 | 27 | 648.0 |
| Cargo bay | 24.5 | 1 | 24.5 |
| Charge launcher | 24.5 | 1 | 24.5 |
| Mooring clamp | 24.5 | 1 | 24.5 |
| Docking clamp | 24.5 | 1 | 24.5 |
| Drill | 25.2 | 1 | 25.2 |
| Insulation | 25.2 | 1 | 25.2 |
| Heat ejector | 25.9 | 1 | 25.9 |
| Mass cannon | 28.8 | 1 | 28.8 |
| Thermal generator | 28.8 | 27 | 777.6 |
| Fission generator | 28.8 | 27 | 777.6 |
| Coolant pump | 29.9 | 1 | 29.9 |
| Fabricator | 30.7 | 1 | 30.7 |
| Battery | 31.2 | 1 | 31.2 |
| Electrolysis | 36.0 | 1 | 36.0 |
| Lead plate | 36.0 | 1 | 36.0 |
| Solar generator | 64.2 | 9 | 577.8 |
| Sensor array | 64.2 | 1 | 64.2 |
| Assembler | 71.7 | 1 | 71.7 |
| Builder bay | 71.7 | 1 | 71.7 |
| Transport bay | 71.7 | 1 | 71.7 |
| Laser cannon | 74.6 | 1 | 74.6 |
| Fusion converter | 78.6 | 27 | 2,122.2 |
| Autopilot | 104.6 | 1 | 104.6 |
| Shield generator | 168.0 | 27 | 4,536.0 |
| Warp drive | 184.8 | 1 | 184.8 |
| Hyperdrive | 251.0 | 1 | 251.0 |
| Tractor beam | 336.0 | 1 | 336.0 |
| Grinder | 15.8 | 125 | 1,980 |
| Refinery | 21.1 | 125 | 2,640 |

Specialized producers aren't sold, so they have no price.

- **Starting credits:** the 100 starting credits buy a Fabricator (30.7), with enough left for a few cheap parts.
- **Tiers:** a part's price is its per-block price times its block count, since cost follows volume. A Radiator is 15.1 at tier 1 (1 block), then 408 (27 blocks), then 1,890 (125 blocks), up to about 103,700 at tier 10 (6,859 blocks).
- **Blueprints:** a blueprint costs 10x the part price for the same tier. A tier 1 Fabricator blueprint is about 307 credits. A blueprint unlocks the ability to build that part yourself. You can still buy finished parts from stations without it.
- **Lead plates:** they scale in width but not depth (1×1×1, 3×3×1, 5×5×1, 7×7×1, and so on) and cost the same per block. A 5×5×1 plate is 25 blocks, or 900 credits.

---

## Quests

A default quest pays 100 credits. Quest payouts use full value, not the 0.8x station buy rate.

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
- **Selling the whole body to a Cargo station:** pays for the full Mass at the 0.8x buy rate, 1,152 credits.

Moving the whole body pays more than twice as much as mining the part they want, which is the reason to put in the effort.

---

## Worked examples

Seven parts, shown from elements up. Prices are per 1 Mass, a block is 10 Mass, and each recipe splits its Mass equally between its inputs. Each step adds 1.2x.

### Radiator (1 block)

| Stage | Item | Made from | Credits per Mass |
|---|---|---|---|
| 0 | Aluminum, Carbon, Iron | Elements | 1 each |
| 1 | Graphite | Carbon | 1.2 |
| 1 | Steel | Iron, Carbon | 1.2 |
| 2 | Radiator panel | Aluminum, Graphite | 1.32 |

Part: 5 Mass Radiator panel (6.6) + 5 Mass Steel (6.0) = 12.6, times 1.2 = **15.1 credits**. The raw elements inside are worth 10, so the part is 1.5x its elements.

### Solar generator (3×3×1, 9 blocks)

| Stage | Item | Made from | Credits per Mass |
|---|---|---|---|
| 0 | Silicon, Oxygen, Calcium, Copper, Gold | Elements | 1, 1, 1, 3, 30 |
| 1 | Glass | Silicon, Oxygen, Calcium | 1.2 |
| 1 | Copper wire | Copper | 3.6 |
| 2 | Circuit board | Copper wire, Silicon, Gold | 13.84 |

Part, per block: 3.33 Mass each of Glass (4.0), Circuit board (46.1), and Silicon (3.3) = 53.5, times 1.2 = **64.2 per block**, or **577.8 credits** for 9 blocks. The raw elements are worth 44.4 per block, and Gold is about 75% of that.

### Warp drive (1 block)

| Stage | Item | Made from | Credits per Mass |
|---|---|---|---|
| 0 | Calcium, Phosphorus, Potassium, Copper, Titanium, Aluminum, Helium | Elements | 1, 3, 3, 3, 3, 1, 1 |
| 1 | Copper wire | Copper | 3.6 |
| 1 | Titanium alloy | Titanium, Aluminum | 2.4 |
| 1 | Moovium | Calcium, Phosphorus, Potassium, then times 10 | 2.8 × 10 = 28 |
| 2 | Superconductor coil | Copper wire, Titanium alloy, Helium | 2.8 |

Part: 5 Mass Moovium (140) + 5 Mass Superconductor coil (14) = 154, times 1.2 = **184.8 credits**. The raw elements are worth only 21.7, so the part is about 8.5x its elements. The Moovium rarity premium is nearly all of that.

### Builder bay (1 block)

| Stage | Item | Made from | Credits per Mass |
|---|---|---|---|
| 0 | Iron, Carbon, Copper, Silicon, Gold | Elements | 1, 1, 3, 1, 30 |
| 1 | Steel | Iron, Carbon | 1.2 |
| 1 | Copper wire | Copper | 3.6 |
| 2 | Actuator | Copper wire, Steel | 2.88 |
| 2 | Circuit board | Copper wire, Silicon, Gold | 13.84 |

Part: 3.33 Mass each of Steel (4.0), Actuator (9.6), and Circuit board (46.1) = 59.7, times 1.2 = **71.7 credits**. The raw elements are worth 47.8, so the part is 1.5x its elements. The Transport bay uses the same materials and costs the same. The Builder drones a bay holds are priced separately, as a step 3 material at 7.2 per Mass.

### Fabricator (1 block)

| Stage | Item | Made from | Credits per Mass |
|---|---|---|---|
| 0 | Iron, Carbon, Copper | Elements | 1, 1, 3 |
| 1 | Steel | Iron, Carbon | 1.2 |
| 1 | Copper wire | Copper | 3.6 |
| 2 | Actuator | Copper wire, Steel | 2.88 |

Part: 3.33 Mass each of Steel (4.0), Actuator (9.6), and Copper wire (12.0) = 25.6, times 1.2 = **30.7 credits**. The raw elements are worth 20, so the part is 1.5x its elements. The starting 100 credits buy one and leave 69.3.

### Grinder (tier 1, 5×5×5, 125 blocks)

| Stage | Item | Made from | Credits per Mass |
|---|---|---|---|
| 0 | Iron, Carbon | Elements | 1 each |
| 1 | Steel | Iron, Carbon | 1.2 |
| 1 | Graphite | Carbon | 1.2 |
| 2 | Bearing | Steel, Graphite | 1.44 |

Part, per block: 5 Mass Steel (6.0) + 5 Mass Bearing (7.2) = 13.2, times 1.2 = **15.8 per block**, or **1,980 credits** for 125 blocks. It takes 1,250 Mass of materials, made of about 469 Iron and 781 Carbon. Those elements are worth 1,250, so the part is about 1.6x its elements.

### Lead plate (1×1×1)

| Stage | Item | Made from | Credits per Mass |
|---|---|---|---|
| 0 | Lead | Element | 3 |

Part: 10 Mass of Lead is 30, times 1.2 = **36 credits**. It's one step at 1.2x. A 5×5×1 plate is 25 blocks, or 900 credits.

---

## Things to watch

- **Buy and craft loop:** stations sell at full value and buy at 0.8x. Each crafting step adds 1.2x, so one step loses 4% (1.2 × 0.8 = 0.96), two steps gain 15% (1.44 × 0.8 = 1.15), and three steps gain 38% (1.73 × 0.8 = 1.38). The loop only pays for deeper chains, and electricity has no price here, so crafting speed is the only limit. A buy rate of 0.7 would break even at two steps, and 0.5 would stop the loop entirely.
- **Converters:** a converter can turn cheap elements into pricier ones, like 9 Helium (9 credits) into 4 Beryllium (12 credits). Massive electricity is the only limit.
- **Cheap parts:** most parts cost 15 to 100 credits per block, which is a fraction of one quest. Only Grinders and Refineries, and the Moovium and Voidglass parts, cost much more.
- **Lead plates:** at 36 credits per block, covering both faces of a 5-wide part takes 50 blocks of plate and 1,800 credits, whether they're placed as one flat plate per face or as single blocks.
