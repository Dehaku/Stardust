# Stardust: Points of Interest

POIs are the stations and derelict ships you find in space.

Each POI has a spawn weight. When a POI spawns, the game makes a random roll weighted by spawn weight, so a higher weight appears more often. The weights below are placeholders.

| POI | Type | Spawn weight | What it offers |
|---|---|---|---|
| Trade station | Station | 30 | Sells parts and part blueprints for credits, including your first Fabricator and Assembler. Buys unused elements for credits |
| Exchange station | Station | 20 | Takes resources and gives back rare materials. Each one offers 1 to 3 random rare materials, chosen when the station is generated |
| Cargo station | Station | 10 | Takes whole bodies into its open cargo bay and pays credits for their full mass |
| Quest station | Station | 8 | Gives quests (see Quests below) that can reward Specialized producers |
| Derelict freighter | Derelict ship | 12 | Loot: common parts and materials |
| Derelict mining barge | Derelict ship | 6 | Loot: mining tool parts and kinetic ammo |
| Derelict survey ship | Derelict ship | 1 | Rare loot: a Specialized producer |

---

## Quests

Quest stations ask for one of these:

- **Delivery:** bring specific matter or parts to this station. They're low on materials. Pays 2x credits for the matter they want, until their goal is satisfied.
- **Body delivery:** bring a body of a given type. They're low on materials and need a lot of it. Pays 2x for the whole body you deliver, as long as it has some of what they want in it.
- **Volatile packages:** deliver packages to another station. If you collide with anything while carrying them, your Storage bays explode. The blast destroys every block within the bay's size + 2 blocks, and all the matter you had. Pays 2x what a Delivery quest would pay, effectively 4x the base quest tier.
- **Clearing:** harvest the X nearest asteroid-tier bodies. The station sees them as a danger and wants them gone. Pays the same as Volatile packages.

A default quest reward is 100 credits, and the player starts with 100 credits. Other credit values build off those numbers.

---

## Station stock

- Trade stations sell a random set of parts and blueprints, and higher-tier blueprints appear less often.
- Each station has 3 locked trade slots. They reveal one by one as you trade a certain amount of Mass worth of materials and elements with that station.
- Your trades effectively help the station get better stock.
