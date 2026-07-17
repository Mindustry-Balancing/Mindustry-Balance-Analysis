{
  "name": "nsr od",
  "block": {
    "overdrive-projector": {
      "speedBoost": 1.25,
      "useTime": 240,
      "itemCapacity": 30.0,
      "speedBoostPhase": 0.25,
      "consumes": { "power": { "usage": 8.0 } },
      "phaseRangeBoost": 28.0,
      "requirements": [
        "titanium/240",
        "metaglass/100",
        "silicon/200",
        "plastanium/60"
      ]
    },
    "overdrive-dome": {
      "speedBoost": 1.6,
      "itemCapacity": 50.0,
      "consumes": {
        "remove": ["items"],
        "power": { "usage": 32.0 },
        "items": {
          "items": ["silicon/5", "phase-fabric/1"]
        }
      },
      "useTime": 120.0,
      "requirements": [
        "lead/800",
        "silicon/600",
        "titanium/450",
        "plastanium/300",
        "surge-alloy/200",
        "phase-fabric/120"
      ]
    }
  }
}

So. overdrive projector has comparable bcost to a thorium reactor. Power cost equivalent to two surge smelters. Upkeep is half an unoverdriven phase weaver. Base +25%, phase +25%.

Overdrive Dome has comparable bcost to multirecon; surge cost is slightly below surge tier turrets and phase cost is a **fifth** of exponentialrecon's. Power cost is quadruple from the projector's. Upkeep is one unoverdriven phase weaver and abit less than half a silicon crucible. +60%.