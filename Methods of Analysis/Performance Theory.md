# Performance Theory
The branch that deals with how the performance of turrets and units is measured.

Under this branch, multiple statistics on content are utilized such as DPS, Vitality, TTK, DFD, DPI, Upfront Cost, Production Cost and many more which are used to compare and evaluate how a specific piece of content performs. This is the blood on how turrets or units are compared.

This does not account for pacing and eco, which is under Tempo Analysis, which varies map to map or even gamemode to gamemode. _[See Tempo Analysis]()_

---

(Draft)

For Units, the main concepts utilized would be the following.

- Vitality
    - Health * Speed
    - Evaluates how well a unit can survive the turret's initial dealt damage (upfront damage), while travelling into range.

- Inflicted Damage
    - TTK * DPS
    - The amount of total damage a unit can deal with a defense, and is a good standard measurement of performance.
    - Typically on any estimations, this takes into account...
        - Remainder Health from the Initial Vitality Stage, then converted to TTK via the Defense's DPS
        - DPS is the Net DPS (DPS - Mender Rates - Auxilary Reductions)

From here, the turret stats have been contextualized as

- DPS
    - Straight Foward Analysis, and is the main robust way to reduce the units from winning, by killing them faster.

- DPS * Range
    - Used in the Vitality Stage, measures how well
    - When calculating, 
        - Usually "Range" is the net Tiles Needed To Travel for a unit To start shooting.
        - Range - Unit Range
        - For more than one turret, all of the factors is accounted in the Scaling Function S (Defense Thickness, Number of Turrets, Compactibility, Unit Target, etc.)



... (Future Section, maybe Niche Analysis starts here?)

Certain behaviors are present...

Those with short range, typically have higher DPS rates and help more in the Inflicted Damage Stage of an Attack.

Those with longer range, typically focus more on DPS*range overall since they have better scalability (S), and can potentially remove units early on or even all.

During the Vitality Stage, units are at their weakest where depending on formation type (Line or Blob), could reach a point where the number of units starts to become increasingly ineffective...

(As a good concrete example, this phenomenon is why the Overrange Meta exists as the forcus is more on preventing units getting into range).

