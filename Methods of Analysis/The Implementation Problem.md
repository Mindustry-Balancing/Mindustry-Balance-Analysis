# The Implementation Problem

[In progresss]
This is a problem that deals on the secondary effects that affect which balancing decisions are more likely to be accepted.  
## Developer Side
### Game Dev Appeal
---
A balance change is like a suggestion post, so a lot of the considerations come from the developer's list.
[Mindustry-Suggestions, Why I haven't implemented your suggestion yet](https://github.com/Anuken/Mindustry-Suggestions#why-i-havent-implemented-your-suggestion-yet)
```
## Why I haven't implemented your suggestion yet
Because most suggestions are bad. The overwhelming majority are rejected because they fall into one (or more) of the categories below:

- It's too niche or not sufficiently useful to warrant adding to the game.
- It is infeasible to implement or not worth the effort.
- It's just a bad idea and would negatively impact the game.
- It's _not_ a bad idea, but I don't have time to implement it or have different priorities - usually, suggestions like this get the "candidate" tag.
- It's one of the things I have explicitly mentioned in the list at the end.
- It's already in the game and you didn't notice.
- It is written in a language I don't understand.
- It is incomprehensible or poorly written.
```
The first 3 are your major considerations
- It needs to be impactful
- It needs to be code implementable *(see: Code Implementability)*
- It not a bad idea

[Mindustry-Suggestions, A few things you shouldn't suggest](https://github.com/Anuken/Mindustry-Suggestions#a-few-things-you-shouldnt-suggest)
```
## A few things you shouldn't suggest
##### These have been proposed many times already, and I won't be adding them.
- Mechanics that increase game speed (fast-forward)
- New planets
- Teleporters
- Underground map layers
- Trains, or any transportation system that uses something analogous to rails
- Item-liquid junctions
- Controller support (_this has already been attempted and does not work well with Mindustry_)
- Turrets on top of cores, or similar "merged behavior" blocks like turrets with drills
- Built-in cloud sync
- Any kind of account system
- Additional configuration of blocks, such as I/O side configuration
- Configuring drill outputs or selecting which resource to mine
- Carrying aircraft with naval units
- Preview of unit paths or waves
- Any sort of string allocation in logic - copying strings to variables, splitting strings, etc
- Allied teams
- Bringing back overflow-sorter chaining
- Anything involving bringing back the old formation command system
```

### Code Implementability
---
If your balance change is hard to code in, it will not happen.

While usually, most balancing changes are easy to do (stat based balancing where numerical stat values are only altered), certain changes (such as mechanical balancing, where new features are added in) may not be feasible to implement. 

The chances of a mechanical balance change increases if you are able to make a pull request (a PR) to those changes. This also can apply to stat balances, as it does save time on the developer's end to implement those changes.

This factor is entirely dependent if you are able to code it in yourself. Unless, the change is good enough that creator himself would implement it (if they even have the time).

## Community Side

### General Backlash
---
Not all balancing changes are going to be accepted as readily. 
#### Unfamilarity
Unfamiliar things can be seen in a negative view. *(reference [When unfamiliarity sets minds against you | The Research Agency](https://www.theresearchagency.com/insights/unfamiliarity-sets-minds-against-you#top))*

Not every update people will like. There will always be some who may not view a change as positive. 
- The snek changes, [578 in agreement : 1056 in opposition, viewed on July 28, 2025](https://discord.com/channels/391020510269669376/513178557653188609/695649084895133766), and now in the faq, it has been removed. ["chaining together specific filter blocks for high throughput should never have been a valid strategy to begin with"](https://discord.com/channels/391020510269669376/396416151032299521/755785485301055599)

You can see here that even if a balance change is controversial, it is still possible to implement. However, we now need the terminology and the frameworks needed to answer on how to handle backlash.
### Discussion of Terminology and Frameworks
---
#### Soft Breaks
Soft breaks are defined as changes that doesn't completely impair a give block's structure to function. At the end, it may no longer be the optimal schematic, but it will still work at the end.
Examples include: Amount of Input-Requirement Changes, Output Amount Changes.

#### Hard Breaks
Hard breaks are defined as changes that completely stops a schematic from functioning.
Examples include: Input-Requirement Type Changes. 

#### Tangible Backlash
These are defined as what is being asked of the player when a balance change is impacted.
There are some non tangible backlashes like...
- Unfamiliarity

But there are multiple tangible backlashes like...
- Schematic and Map Breaking
- Option Availability
- Game Pacing Changes
- Clearness

#### Cost-Benefit Framework
The benefit of a balance change *(its impact)* must outweigh the cost due to tangible backlash.

### Schematic and Map Breaking
---
These are changes that affect factories directly, and evaluated using Soft and Hard Breaks.

The main question of this under the cost-benefit framework is... ***"is the balance change worth it if we are asking the players to recreate or adjust schematics and maps."***

Maps are also affected, as you can think of them as one big schematic operating in a base.

#### Case Analysis: Water Extractors (Wex)

Have you ever seen those T5s schems with a million wexes? or those impact schems? maybe every schem that requires water at mininum, from ABs, Multi-Presses, Oilex, Silicon-Crucible-Oilex, Differentials, Steam... the list goes on.

Let's say we change Wex's 6.6 to 6, with the main purpose of disincentivising wex usage. What is the cost-benefit of this change?

***TODO: NEED TO FILL OUT THE BENEFIT/COST ASPECTS CORRECTLY. AND MAYBE IF THIS CASE IS EVEN A GOOD ONE? UNSURE***

Cost
- Wex sharing, a phenomena arising as wex doesn't fit the usual integer ratio values, will now be impossible. Which loses a fun aspect of schematic designing.
- (Hard Break) Impact schems are likely broken as they are very sensitive to any impact. Any map with wex based impacts may face power issues.
- (Soft Break) Almost every schematic involving wexes would need to be altered or resized to reach optimal status.

Benefit
- Wex vs Pump situations have been slightly improved.

What's your judgement?

The change isn't that impactful enough to even tackle the Cost, so the balance change would be unsuccessful.

Fundamentally, a lot of maps don't even feature any water tiles to begin with, so the benefit may be completely absent for those.

Ideally a better balance change would be ones that are much more softer, from power-requirement adjustments, to build-cost. Or maybe attacking other aspects like on how available they are in almost all tile-types? Who knows.

### Option Availability
---
### Game Pacing Changes
---
### Clearness
---

