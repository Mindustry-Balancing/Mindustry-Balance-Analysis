# Terminology

### Disclaimer
This is just a set of terms/concepts that some I would have created to describe the certain aspects of the game in a concise way.  
This doesn't cover every topic/term nor some of these terms would be used by other people (hence inside this personal wiki).  
Still, I will likely use these terms in some of the suggestion posts I generate of in Mindustry Suggestions, or to be used in this Wiki.  

### General

#### Tempo
* Refers to the speed and effeciency of a specific players' action.
* The more effecient a player is maximixing resources, the more tempo or value they have produced compared to low tempo actions.

#### Build Order
* The order and time on which specific buildings are placed given environmental conditions.

#### Pacing
* Refers to the general progression and speed of a game.

#### Role
* A purpose or usecase of a specific piece of content.

#### Actions Per Minute (APM)
* From the community, a general measurement on the attention a player can give at any moment.

#### Accelerated
* Descriptor for game modes or conditions where Tempo is high, and APM matters so much more.
* Examples Include: PvP, Eradication Campaign for Sector Capture, Low Timer Survival/Attack

#### Expansionist
* Descriptor for game modes or conditions where space isn't a large restriction.
* Examples Include: HexPvP, Eviction

#### Restricted
* Descriptor for game modes or conditions where space is limited.
* Examples Include: Optimization of Captured Sectors, Attack under Tech Lock, Anti-Rush PvP

#### Tech
* Refers to the content accessible at a given stage.

#### Tier
* Refers to the current raw resource accessible, usually drilled or pumped.
* Usually for raw resources that unlocks a major part of the tech tree, although can be extended to any raw resource.

#### Tech Lock
* Refers to when a map or game mode restricts access to certain parts of the tech tree for pacing control, map balancing, or as a gimmick.
* Usually by affecting resource accessibility or directly by banning blocks.

#### Asymptotic
* Refers to a behavior or entity that gets better eventually as the game duration increases.

#### Frames Per Second (FPS)
* As stated, it refers to the number of frames the game runs in an individual's computer in a given second.
* Certain entities are affected by this.

#### Ticks Per Second (TPS)
* Similar to FPS, this is the number of ticks the game runs in a server.
* For multiplayer, this is what affects certain entities similar to FPS.

### Unit-Turret (Familiar Background Terms)

#### Damage
* The amount of hitpoints that will be deducted on an opposing entity.  
*"This bullet deals 9 damage."*

#### Health
* The amount of hitpoints an entity has.
* When the health is below 0, it "dies."  
*"It takes 150 damage to kill my unit."*

#### Armor
* An amount that is subtracts incoming damage toward an entity.
* This is applied to both splash damage and direct damage.
* Currently (v147), can only reduce at most by 90%.  
*"This unit's 5 armor reduced bullet's damage from 10 to 5."*

#### Rate of Fire / Fire Rate (RoF)
*1/second* `[60/reload(code)]`
* The number of bullets fired every second.  

Game Code Conversion:  
For every 1 second there are 60 ticks, so to convert from ticks to seconds, use the conversion factor of [1 second/60 tick].  
`1/(reload(code)[tick] * [1 second/60 tick]) -> 1/(reload(code)[second]/60) -> 60/reload(code) in 1/second.`

#### Damage Per Second (DPS)
*damage/second* `[damage*RoF]`
* The amount of damage dealt every second.

#### Range
*tile* `[range(code)/8]`
* Also known as "Effective Range"
* The number of tiles that an entity's distance has at maximum to be fired at.  

Game Code Conversion:  
Every in-game tile inside the code has 8 world unit, so our conversion factor will be [1 tile/8 world unit].  
`range(code) [world unit] * [1 tile/8 world unit] -> range(code)/8 in tile.`

#### Speed
*tile/second* `[speed(code)*7.5]`
* The number of tiles a given moving entity can traverse in a given second.  

Game Code Conversion:  
Use the appropriate conversion units, [1 tile/8 world unit] and [1 second/60 tick] to convert appriopriately.  
`speed(code) [world unit/tick] * [60 tick/1 second] * [1 tile/8 world unit] -> speed(code) * 60/8 [tile/second] -> speed(code)*7.5 in tiles per second.`

### Unit-Turret

#### Wreck Health
* When an air unit dies, it leaves a "wreck" that can absorb damage with its health.

#### Item Bombing
* A strategy that utilizes a phenomenon, where in any unit that dies while holding an item with a high attribute, such as explosiveness, that unit causes an effect, such as an explosion, on where the unit died.  
*"My enemy's item bombing caused a fire inside my coal patch."* 

#### Time To Kill (TTK)
* From the community, refers to the amount of time a specific unit lives under a given defense or defending actor.  
*"Serpulo has a much lower TTK compared to Erekir due to Erekir having higher hp values and low turret dps."*

#### Overrange
* Refers to interactions where a given actor (turret/unit) cannot engage due to being smaller than the effective range of another actor.  
*"Corvus (v146) currently overranges Spectre by having more range than it."* 

#### Item Damage / DamagePerItem / Ammo Efficiency
*damage/item* `[damage*ammoMultiplier/ammoPerShot]`
* General measurement of how much damage a singular item of a given type can deal.

#### Turret Space Efficiency
*DPS/tiles* `[(damage/second)/spaceOccupied]`
* General measurement of how much damage per second an area has given a fixed space.

#### Vitality 
*hp\*speed, hp\*tiles/sec* `[unitHP*speed(code)*7.5]`
* A general measure of the survivability of a unit when getting into range.
* Divide it by the defensive dps to calculate the tiles a unit can travel.

#### Mobility
* A more general term for the manuverability and flexibility of a unit.
* Proportional to speed and agility.

#### Distance from Defense (DFD) 
*tiles* `[DefenseRange - GroupVitality/TotalDefenseDPS]`
* The distance where a group of units died, a general measurement that takes into account the effect of range with dps.

#### Dealt Damage
`[Unit DPS * TTK]`
* The amount of damage the unit has dealt against a defense or piece of content.

#### Mode of Agression (MoA)
* A specific type of role that revolves around when and where a unit can be effective when it comes to dealing damage.

#### Chokepoint / Coverage Number
* The number of built defenses needed to break even with the net cost of the units.
* A general measurement of unit agression.

### Economical and Value

#### Yield
*output/sec (ips, i/s; lu/s; pu/s; etc.)*
* The general output of a building
* Applies to drills, pumps, factories, power-generators, etc.

#### Upfront Cost
* A general term for the net cost when intially placing a building.
* Includes item cost predominantly, but can also include build speed and APM cost considerations.

#### Wiring Cost
* A specific form of cost that is mostly in APM.
* How much time and effort is spent in routing items or liquids for production buildings, core transport, or general logistics.

#### AB-eq
*items*
* An airblast equivalent is the amount of airblasts needed to produce the necessary items in one second.
* Used as the predominant measurement of production cost.

#### Water-eq
*liquids*
* The amount of total water needed.

#### Production Cost
*AB-eq and Water-eq*
* The amount of production needed to produce a piece of content.

#### Build Time
*seconds*
* The amount of time to build something with standard buildspeed. 

#### Ramper
* A descriptor of a building that has low initial cost (usually item cost) but restricted in some way.
* The restrictions are usually high consumption rates or by making it limited on where it can be placed.

#### Scaler
* A descriptor of a building that has high initial cost but not bounded by requirements (usually low consumption rates). 
* These are often resource dumps or sinks and are usually tile or consumption efficient.
* Is inherently asymptotic.

#### TPS Resistance
* A general notion on how much an entity, more commonly associated with blocks or certain schematics, can still be effective or functional as TPS decreases or approaches 0.  
*"Liquid tanks are more TPS resistant than liquid routers because they have a higher storage capacity."*
___
