# Unit I
## Chapter 1: Fundamentals of Singleton Turrets

### Chapter Overview

This chapter explores the basics on how single turrets with known metrics such as DPS and Range peform against single units.
- **Section 1: "Classical Stats of Turrets and Units"** details the background for what metrics are being used such as health, DPS or range.
- **Section 2: "DPS and The Defintion of Performance"** now describes what it even means for something to be "good."
- **Section 3: Range Dynamics and DFD Analysis** now puts space in consideration, as turrets and units have to get close to interact.
- **Section 4: DPS-Range and Vitality** formalizes how range is involved against units with health and speed.
- **Section 5: DPS and Vitality Stages** details how different turrets may be appropriate depending on the circumstances.

### Section 1: Classical Stats of Turrets and Units

Most turret defense games feature feature stats that describe how the turret operates. If you had played Mindustry in its first levels, these metrics may be familiar. A turret in mindustry generally has the following properties.

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
- It is defined as the distance from the turret where it can deal damage towards any enemy object.
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

[![Video](https://github.com/Mindustry-Balancing/Mindustry-Balance-Analysis/blob/main/Methods%20of%20Analysis/Main%20Theory/Videos/black%20image.png)](https://github.com/Mindustry-Balancing/Mindustry-Balance-Analysis/blob/main/Methods%20of%20Analysis/Main%20Theory/Videos/U1C1%20-%202%20turrets%20comparison.mp4)

- The bottom turret has a better DFD score than the top turret: the unit was killed at a greater distance than the other.
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

### Section 4: DPS-Range and Vitality

To motivate the following stats, lets get ourselves into a scenario.
We have two different turrets facing against the same unit. Let's run the scenario with one unit with 1x hp, and then another with 2x hp.

[Video]

[Video]

This seems to be a very complicated situation, why is there two different results on which is more perfomant even if the turrets are the same? To answer this requires further analysis and another scenario is needed to explore.

Suppose you have 2 sets, one containing a turret with 1 dps and 10 tiles of range, and another with 0.5 dps and 20 tiles of range; both encounter the same type of unit with 1 health and 10 tiles/second. Let us assume that the turrets have to start from 0 reload.

[Image]

From the given, how far would the unit go?

In this case, it would be simply the amount of time the unit was alive times the speed of the unit.

```
Tiles Travelled = TTK * Speed
Tiles Travelled = (Health / DPS) * Speed
Tiles Travelled = Speed * Health / DPS
```

Now, Speed * Health has a special name and it is something I've coined due to how important of a concept it is. That quantity is called **Vitality**. It is defined as the overall capability of a unit to reach a given destination when being actively damaged.

Let's calulate the amount tiles travelled for both scenarios.

```
(10 tiles/second * 1 hp) = 10 Vitality
Tiles Travelled of A = 10 tiles = 10 Vit / 1 dps 
Tiles Travelled of B = 20 tiles = 10 Vit / 0.5 dps
```

Because of the reduced dps of scenario B, the unit travelled double the distance.

[image]

However, as shown, both die in the same place. That's because the turret in scenario B shot earlier. That's because to compute for the DFD...

```
DFD = Range - Tiles Travelled
DFD of A = 0 = 10 - 10
DFD of B = 0 = 20 - 20
```

So... what happens if the vitality of unit has been reduced to 5? What are the DFD scores then?

Well...

```
DFD = Range - Vitality/DPS
DFD of A = 5 = 10 - 5 / 1
DFD of B = 10 = 20 - 5 / 0.5
```

[image]

In this case, the turret with the higher range performed better by keeping the unit away as much as possible.

With how the formula behaves, it seems like Scenario B's turret will always have better DFD Scores than the turret in Scenario A. Thus we can say that, for this type of measurement, the double range but half dps turret is better.

But with how I setted up the scenario, something special had happened. Since I divided the vitality by 2, somehow the DFD values relative to the range has also been reduced by half. 

Returning to the original situation, we can actually use the given equations to predict DFD scores as a measure of vitality. Plotting the graph produced shows an intersection.

[Image]

Everything before the intersection, the first turret (in blue) dominates and is more performative, but everything after the second turret (in red) is now the bettter option. 
> This is an interesting dynamic that is more extensively explored in Chapter 3 as multiple turrets have different ranges depending on position. 

There is a quick way to judge if such an interesction occurs and the overall power of a turret when taking into account DPS and Range in this scenario. Taking the original equation show cases the following.

```
DFD = Range - Vitality/DPS
DFD/Range = 1 - Vitality/(DPS * Range)
```

The DPS-Range now exists as a quantity, this is used to determine how effective a turret can prevent a unit from getting close. After some invetigations with the graph here are the results.
1. If the DPS-Range of two turrets are the same, the one with the longer range will always have higher DFD Scores than the other.
2. If the DPS-Range of the shorter ranged turret is bigger than the other, there is a point in the path of a unit where the close ranged turret takes over as being better. This occurs as the unit's Vitality increases.

With that, that is most of DFD Analysis has been covered. There is one very important thing to consider.
- Eventually, the unit will get in range and be able to fire.
- At this point, range no longer matters at this specific point and only DPS takes over.

In the last section, there will be an exploration on how the two seperate stages of a unit's journey affect how a turret performs. Forming a complete picture.

### Section 5: DPS and Vitality Stages

There are two distinct stages of a unit, and the performance of a turret may vary as the unit gets closer.
1. The Vitality Stage
- This is the stage where a unit has to travel to get close and is where the turret is at its most advantageous.
- It is determined entirely by Range and DPS-Range as it attacks the Vitality of a unit.
2. The DPS Stage
- This is the stage where a unit is now able to fire and deal damage.
- TTK and therefore DPS are the main determinants as it attacks only the Health of a unit.

For the first stage, as discussed extensively in Section 4, the main way to determine performance is through DFD and directly via DPS-Range. However, in the second stage, the turret has gotten close and all that is needed is to kill it immediately and higher DPS is required.

So when does a turret specifically becomes better or worse as the two stages are switched with each other?

First, there is a need for the following quantity:
- Upfront Damage, the amount of damage recieved during the entire Vitality Stage.
- Can be computed by multiplying the amount of time to travel the distance and the DPS.

```
Upfront Damage = DPS * Time to Travel
Upfront Damage = DPS * (Range - Unit Range) / Speed
Upfront Damage = (DPS-Range - tDPS-uRange) / Speed
```

Next, finally two lines are made.

```
Low Range Turret Damage = DPS_lowrange * t
High Range Turret Damage = Upfront Damage + DPS_highrange * t

Intersection:

(DPS_l - DPS_h) * t = Upfront Damage
t = Upfront Damage / Difference in DPS

Converting this into a form of distance for DFD Analysis in the persepctive of the low range turret.

DFD to Break Even = Range - Speed * t.
```

If you are able to compute the break even point in distance, you can roughly eyeball when you may want to use a different option. Examples may include... 
- Hail vs Salvo
- Spectre vs Meltdown
- Swarmer vs Cyclone

If we ignore costs and scale eveyrthing up appropriately (See Chapter 4 for an overview and Unit III. for specifics)

With the computed take over time, there is now enough information to know when a turret with known dps and range can be better than another turret with its own dps and range. That concludes this Chapter and we will be moving into Chapter 2: what happens if there is more than one unit?

(TODO Notes, Section 4 needs more explanation on how the range part, for specific units the effective range, eff. range = range - blocks - unit range as during the pioneering stages, i have always assumed unit range = 0, and negligable wall effects, or just needs more interpretation, it may honestly needs to be split up into 2 with the introduction and interpretation of DFD Analysis. Since this is very much into the deep end.)

(TODO, need to actually have more examples on how this is useful? We haven't actually talked about specific turrets yet until the last part lmao.

(TODO oh right uh for the first TODO, you need to explictly say when DFD no longer works (limitations), usually when a unit stops, the distance no longer encodes damage recieved, and other stuff)
### Experimental Methodology
