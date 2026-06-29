# 📄 **Adventure Generation API Specification**  
### *Continuity Adventure System — Forest of Echoes Edition*  
**File Path:** `continuity/adventure/reference/adventure-generation-api-spec.md`

---

## 1. Purpose  
This specification defines the **Adventure Generation API**, which transforms user‑provided story elements into a complete, reversible, ND‑paced multi‑mode adventure.

The API supports:

- **World‑Builder Mode**  
- **Character‑Creator Mode**  
- **Story‑Weaver Mode**  
- **Multi‑Mode Adventure Loop**  
- **Optional Systems** (Echo Tokens, Resonance Map, Stillness Sanctuaries)

This document is intended for contributors, designers, and system integrators.

---

## 2. API Overview  
The Adventure Generation API accepts **story fragments** and outputs a structured adventure composed of:

- World Node  
- Character Node  
- Story Node  
- Adventure Loop  
- Chapter Sequence  
- Optional Systems  

The API is **deterministic in structure**, **non‑deterministic in content**, and **reversible in output**.

---

## 3. Input Specification  
The API accepts any combination of the following element types.

### 3.1 World Elements  
```
type: world
examples:
- "a clearing with blue mosslight"
- "a tree that hums when approached"
- "fog that remembers footsteps"
```

### 3.2 Character Elements  
```
type: character
examples:
- "a wanderer who hears future echoes"
- "hesitant but curious"
- "ability: resonance tracking"
```

### 3.3 Story Elements  
```
type: story
examples:
- "a whisper that leads nowhere"
- "a hum that fades when noticed"
- "soft quest: follow the quietest sound"
```

### 3.4 Mood Elements  
```
type: mood
examples:
- "calm but slightly eerie"
- "slow pacing"
- "gentle disorientation"
```

### 3.5 Symbolic Elements  
```
type: symbol
examples:
- "an echo shaped like a memory"
- "a mosslight pulse that feels like déjà vu"
```

Inputs may be provided in any order and any quantity.

---

## 4. Output Specification  
The API produces a structured adventure object with the following fields:

```
Adventure {
    world_node: WorldNode
    character_node: CharacterNode
    story_node: StoryNode
    loop: AdventureLoop
    chapters: Chapter[]
    optional_systems: OptionalSystems
}
```

---

## 5. World Node Schema  
```
WorldNode {
    name: string
    biome: string[]
    stability: string
    hazards: string[] (symbolic only)
    stillness_nodes: string[]
}
```

**Generated from:** world + mood + symbol elements.

---

## 6. Character Node Schema  
```
CharacterNode {
    name: string
    intent: string
    tone: string
    ability: string
    ecology_link: string
    reversible_traits: string[]
    safety_header: string
}
```

**Generated from:** character + mood + symbol elements.

---

## 7. Story Node Schema  
```
StoryNode {
    name: string
    soft_quest: string
    reversible_scene: string
    pacing_membrane: string
    gentle_arc: string
    stillness_checkpoint: string
}
```

**Generated from:** story + mood + symbol elements.

---

## 8. Adventure Loop Schema  
```
AdventureLoop {
    sequence: [
        "WorldNode",
        "CharacterNode",
        "StoryNode"
    ]
    reversible: true
}
```

The loop always follows:

```
World → Character → Story → World → Character → Story → …
```

---

## 9. Chapter Schema  
The API generates **four reversible chapters**.

```
Chapter {
    id: number
    title: string
    description: string
    reversible: true
}
```

Chapters are derived from the combined element pool.

---

## 10. Optional Systems Schema  
```
OptionalSystems {
    echo_tokens: EchoToken[]
    resonance_map: ResonanceMap
    stillness_sanctuaries: Sanctuary[]
}
```

These are generated only if relevant symbolic or mood elements are provided.

---

## 11. Example API Input  
```
{
    "elements": [
        "a soft hum behind a tree",
        "a wanderer who hesitates before stepping forward",
        "a pool that reflects sound instead of light"
    ]
}
```

---

## 12. Example API Output (Simplified)  
```
Adventure {
    world_node: {
        name: "Resonance Tree Hollow",
        biome: ["echo-moss", "resonance trees"],
        stability: "gentle",
        hazards: ["soft disorientation"],
        stillness_nodes: ["quiet pocket under the roots"]
    },
    character_node: {
        name: "The Hesitant Listener",
        intent: "follow the softest sound",
        tone: "quiet curiosity",
        ability: "hear future echoes",
        ecology_link: "mosslight resonance",
        reversible_traits: ["hesitant ↔ bold"],
        safety_header: "ND-paced, reversible"
    },
    story_node: {
        name: "Hum Behind the Bark",
        soft_quest: "approach the faint hum",
        reversible_scene: "hum fades if overwhelmed",
        pacing_membrane: "slow, steady",
        gentle_arc: "confusion → clarity",
        stillness_checkpoint: "root pulse"
    },
    loop: {
        sequence: ["WorldNode", "CharacterNode", "StoryNode"],
        reversible: true
    },
    chapters: [...],
    optional_systems: {...}
}
```

---

## 13. Safety & Continuity Requirements  
The API must enforce:

- ND‑paced output  
- reversible scenes  
- non‑coercive progression  
- symbolic hazards only  
- no collapse engines  
- no metaphysical triggers  
- continuity‑safe structures  

---

## 14. Versioning  
```
Adventure Generation API — v1.0
Forest of Echoes Edition
```

---

## 15. Closing  
This API spec formalizes how adventures are generated from fragments inside the Continuity Adventure System.  
It is now ready to be pinned in your repo.

---
