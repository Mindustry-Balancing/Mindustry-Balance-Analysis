# Unit I
## Chapter 1: Fundamentals of Turrets

### Section 1: Classical Stats of Turrets and Units

Like most turret defense games feature feature stats that describe how the turret operates. A turret in mindustry generally has the following properties.

1. Health
- All buildings and units in Mindustry features health. 
- Usually objects that inflict damage reduces the health by an amount.
- When it reaches 0, the piece of content no longer "exists".

2. Damage
- Turrets fire bullets, and each bullet deals damage that reduces a building's or unit's health.
- The main purpose of a turret is to deal damage.

3. Reload or Firerate
- Meanwhile, firerate determines how many bullets are fired at a given unit of time.

4. DPS
- The amount of Damage Dealt in one second.
- Calculated by the following:

```
DPS = Damage * Firerate
```

5. Range
- It is defined as the distance from the turret where it can deal daamge towards any enemy object.
- It is measured in tiles.
- This gives turrets a sense of space and will be the source of many analyses.
- It is equally as important as DPS when considering which turret to use.

These features are the fundamental aspects of a turret that most of the theory would be built from. Any Variations would be dealt in Chapter _ . 

It is also important to define the specific characteristics of a unit, while it has many of the same properties of a turret, it has one specific aspect unique to it.

1. Health
2. DPS
3. Range
4. Speed
- This specific stat is a major aspect in unit performance, and would be a consideration in further turret analysis.
5. Armor
- Another stat that is important, subtracts recieved damage by this amount.
- For Serpulo, it is the primary way to force better turrets without high health rates to compensate. 

### Section 2: DPS and The Defintion of Performance

The main central question for balancing is the following.

***What makes any piece of content good?***

In the specific case of a turret, the first immediate thought is that the more DPS a turret has, the better it is... but why?

- Specifically, at the root of it all, a goal of a defense is to reduce the amount of damage recieved as much as possible: to minimize losses.
- Turrets achieve this by damaging the units fast enough to reduce the damage dealt.

Suppose that you have one turret and one unit all in range with each another. Then the damage dealt to the defense is the following.

```
Damage Dealt = Unit DPS * Health / Turret DPS
```

- Usually Health / Turret DPS is given the designation of TTK (Time to Kill), defined as the amount of time required to kill a unit.
- This event or moment is defined as the DPS Stage of an Attack. It is where both the turret and unit fires.
- At this specific stage, it is very simple to know the performance: the larger the dps, the lower the damage dealt.

But we are missing one critical factor in this analysis, what if the turret and unit aren't in range with each other? The next section, we will talk about range and a value known as the distance from defense.

### Section 3: Range Dynamics and DFD Analysis

Typically in Mindustry, usually units have to arrive towards a defense to get their weapons in range. 

Suppose you have one turret and one unit with varying ranges. The unit approaches the turret utilizing its speed. There are two scenarios generated from this.

1. If the turret has less range than the unit, the unit fires first and the unit does not recieve any damage.
2. If the turret has more range than the unit, the turret fires first and the turret does not recieve any damage.

These scenarios have a major impact on how units and turrets interact with each other. Diving deeper for the first scenario...

- In situations where the unit may be player controlled or has smarter behavior, it is in the offense's best interest to not get close to never be dealt damage.
- This phenomenon is known as Overrange: where a unit advantageously recieves no damage while attacking due to range differences.
- Meanwhile, the Survival Gamemode has units still approach and get closer even if the units can overrange.

> This is primarily the source of Survival vs Attack/PvP Gamemode differences in balance. For most of the chapters, only Survival Dynamics are explored as Units II and above covers more of the intricacies of the latter gamemodes.

For the second scenario, being much more common, this stage is where the turret is at its most advantegous. 
- If it has enough DPS, it could potentially prevent a unit from dealing any damage.
- Therefore, a defense in this situation is at its highest performance.

However, due to the above dynamics, it is more important to make the measurement of performance more specific when taking into account of range.

One way to measure performance is how close the unit can get towards the defense. It is known as the Distance from Defense (DFD) and the analysis of performance through this value is known as DFD Analysis. *(Details on how to perform this would be explained in the Chapter's Experimental Methodology)*

- To measure DFD or the DFD score, take the number of tiles away from the defensive wall of a defense.

Let's set an example to see how this value may be a good indicator of performance.

Suppose you have 2 scenarios, each with one turret and one unit. 
- There are two seperate turrets with varying ranges and dps.
- Both encounter the same unit approaching the turrets.

While the turrets may have different ranges and dps values, let's look at the DFD scores made from the scenarios.

(insert video)

- The first turret has a better DFD score than the second turret: the unit was killed at a greater distance than the other.
- Due to this, it is very likely that the first turret would have reduced or even prevented any recieved damage.
- Thus, the first turret is more performative than the second.

There we go! We now have managed to make a comparative statement between 2 turrets on which is better by measuring performance, without even taking into measurement on how DPS and Range may interact. 
- This is a major benefit of doing this approach as the performance can be easily judged based on a video alone.
- This is without any information on how damage is being dealt nor how range may interact in this specific scenario.
- It is likely if I used the first turret in this specific scenario, I would be in a better scenario, than if I used the other one.

However, the next questions are important to ponder on.
- Does one DFD score comparison, always predict that one turret is better than another in all scenarios?
- How can we predict DFD scores in advance to reduce required testing?

These questions leads our analysis to the next sections on how we would predict DFD scores and how DPS still plays a key role even if it isn't the entire picture.

### Section 4: DPS-Range and Vitality.

To motivate the following stats, lets get ourselves into a scenario.

Suppose you have 2 sets, one containing a turret with 1 dps and 1 unit of range, and another with 0.5 dps and 2 units of range; both encounter the same type of unit. 

[Image]



### Section 5: DPS and Vitality Stages.

### Experimental Methodology
