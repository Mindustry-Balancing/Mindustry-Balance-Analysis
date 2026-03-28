# Unit I
## Chapter 1: Fundamentals of Turrets and Units

### Section 1: Classical Stats

Like most turret defense games feature feature stats that describe how the turret operates. A turret in mindustry generally has the following properties.

1. Health
- All buildings and units in Mindustry features health. 
- Usually objects that inflict damage reduces the health by an amount.
- When it reaches 0, the turret no longer "exists".

2. Damage
- Turrets fire bullets, and each bullet deals damage that reduce buildings or units' health.
- The main purpose of a turret is to deal damage.

3. Reload or Firerate
- Meanwhile, firerate determines how many bullets are fired at a given unit of time.

4. DPS
- The amount of Damage Dealt in one second.
- A naive definition for performance.
- Section 2 will break down this thought, as there is more to it than what meets the eye.

5. Range
- It is defined as the distance from the turret where it can deal daamge towards any enemy object.
- This gives turrets a sense of space and will be the source of many analyses.
- It is equally as important as DPS when considering which turret to use.

These features are the fundamental aspects of a turret that most of the theory would be built from. Any Variations would be dealt in Chapter _ . 

It is also important to define the specific characteristics of a unit, while it has many of the same properties of a turret, it has one specific aspect unique to it.

1. Health
2. DPS
3. Range
4. Speed
- This specific stat is a major aspect in unit performance, and would be a consideration in further turret analysis.

### Section 2: The Defintion of Performance

The main central question for balancing is the following.

***What makes any piece of content good?***

In the specific case of a turret, the first immediate thought is that the more DPS a turret has, the better it is... but why?

- Specifically, at the root of it all, a goal of a defense is to reduce the amount of damage recieved as much as possible: to minimize losses.
- Turrets achieve this by damaging the units fast enough to reduce the damage dealt.

Suppose that you have one turret and one unit all in range with each another. Then the damage dealt to the turret is the following.

```
Damage Dealt = Unit DPS * Health / Turret DPS
```

Usually Health / Turret DPS is given the designation of TTK (Time to Kill), defined as the amount of time required to kill a unit.

This event or moment is defined as the DPS Stage of an Attack. It is where both the turret and unit fires.

At this specific stage, it is very simple to know the performance: the larger the dps, the lower the damage dealt.

But we are missing one critical factor in this analysis, what if the turret and unit aren't in range with each other? The next section will talk about range, distance from defense, and the Vitality Stage of an attack.