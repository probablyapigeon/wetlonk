# 🎮 LONK CIVILIZATION SIMULATOR - PLAYER FEATURE SPEC

*A Strategy/Life Simulation with Real NPC Psychology*

---

## 🏆 CORE GAMEPLAY LOOP

You run a civilization of autonomous creatures called **Lonks**. You watch them, interact with them, and guide their civilization through emergent storytelling.

**Main Loop:**
1. **Observe** — Watch Lonks go about their lives, form beliefs, learn
2. **Inspect** — Dig into what they're thinking/feeling in real-time
3. **Influence** — Nudge the world (send events, edit their brains directly)
4. **Emergent Story** — See what unfolds

---

## 👾 NPC SYSTEM: LONKS

### What Are Lonks?
Neural network creatures with 32→16→6 architecture. They have:
- **Real Brains** (neural weights you can inspect/edit)
- **Emotions** (complex state tracking, not binary)
- **Beliefs** (axioms they build and abandon when proven wrong)
- **Personalities** (derived from learned weights)
- **Inner Lives** (constant stream of thoughts)

### Lonk Stats
```
Health:        0-100  (health/hunger system)
Mood:          0-100  (happiness/contentment)
Thoughts:      30/100 (cognitive load/fatigue)
Emotions:      Multiple (trust, curiosity, fear, joy, etc.)
Brain Weight:  Inspectable 32→16→6 neural network
```

### What Lonks Can Do
- ✅ Learn from experience
- ✅ Form beliefs ("Trop is trustworthy")
- ✅ Teach other Lonks new actions
- ✅ Develop personalities over time
- ✅ Have multi-turn conversations
- ✅ Join factions (Dreamweavers, Chaos Choir, etc.)
- ✅ Create religions and myths
- ✅ Betray allies, form alliances
- ✅ Move between locations
- ✅ Gather resources

---

## 🎮 PLAYER COMMANDS (Real-Time Control)

Run these while the simulation is active:

### INSPECTION COMMANDS

| Command | Effect | Example |
|---------|--------|---------|
| `/lonks` | List all Lonks with stats | Shows: Trop (Health 85, Mood 60) |
| `/status` | World overview | Population, factions, resources |
| `/thoughts <name>` | What is this Lonk thinking RIGHT NOW? | Reveals inner monologue |
| `/memory <name>` | Full experience timeline | Every event this Lonk remembers |
| `/identity <name>` | What does this Lonk believe about reality? | Their axioms, worldview |
| `/emotion <name>` | Emotional state breakdown | Trust: 70, Fear: 20, Joy: 85 |

### WORLD COMMANDS

| Command | Effect | Example |
|---------|--------|---------|
| `/sense <event>` | Send an event to the world | `/sense the sky turns red` |
| `/step <n>` | Advance n ticks | `/step 10` runs 10 simulation steps |
| `/style <name>` | Change UI style | Choices: normal, soft, intense, dreamy |

### SAVE/LOAD COMMANDS

| Command | Effect | Example |
|---------|--------|---------|
| `/save <file>` | Save world state + all NPC brains | `/save civilization_v1.json` |
| `/load <file>` | Load saved world | `/load civilization_v1.json` |
| `/quit` | Exit | Goodbye! |

---

## 🧠 NEURAL EDITING (Weight-Space Programming)

### The Unique Feature
You can **edit Lonk brains while they're running**.

```
Normal AI:
You → Black box → Output (opaque)

Lonk AI:
You → Inspect 32→16→6 network → Edit weights → See behavior change
```

### How It Works
1. Lonk's brain is a 32-neuron input layer → 16 hidden → 6 output layer
2. You can request weight inspection
3. Edit weights directly (no gradient descent)
4. Watch behavior change in real-time
5. A/B test different weight configurations

### Example Use Case
```
Lonk "Trop" is too aggressive in trades.
You: Inspect Trop's brain
You: Lower the "dominance" output neuron weights by 20%
Result: Trop becomes more cooperative immediately
You: Run side-by-side comparison (Trop vs. control twin)
```

---

## 📚 BELIEF SYSTEM (Autonomous Epistemology)

### How Lonks Think
1. **Form Axioms** — "Grob is trustworthy" (belief state)
2. **Test in World** — Interact with Grob, gather evidence
3. **Evaluate** — Does reality match belief?
4. **Paradigm Shift** — If falsified, abandon belief and rebuild worldview

### Player Impact
```
Event: Grob betrays Trop

Trop's internal process:
  Axiom destroyed: "Grob is trustworthy" ❌
  Emotion spike: Betrayal (fear up, trust down)
  New axiom: "Grob is selfish" ✅
  Action change: Stop trading with Grob
  
You see this via: `/thoughts trop` → shows realization
                  `/emotion trop` → shows emotional impact
                  `/identity trop` → shows updated beliefs
```

### Watch Civilizations Form
Collective belief systems emerge:
- "The Shiny Pit is sacred" → Religion
- "Chaos Choir members can't be trusted" → Political division
- "Knowledge spreads through teaching" → Culture

---

## 💬 CONVERSATION SYSTEM

### How It Works
- Lonks have **multi-turn conversations** with you and each other
- Conversations **decay naturally** (topics get old, Lonks forget)
- Each message tied to **emotional state** (anxious Lonk speaks differently)
- Conversations **persist** across save/load

### Example Dialog Flow
```
You: "Trop, tell me about Grob"
Trop (curious): "Grob is interesting. We met by the river."
You: "Does Grob ever lie?"
Trop (anxious): "I'm not sure anymore... Grob seemed honest once."
[3 days later]
You: "Trop, what about Grob now?"
Trop: "I don't remember that conversation very well..."
```

### Conversation Decay
Older conversations fade. Lonks don't remember everything forever. This makes history matter: events that shaped Lonks fade into myth over time.

---

## 🏘️ CIVILIZATION FEATURES

### Factions
Lonks join factions with shared beliefs:
- **Dreamweavers** — Philosophers, mystics
- **Chaos Choir** — Experimenters, risk-takers
- **Bonk Battalion** — Warriors, protectors
- You can see faction members, their shared values, conflicts

### Sacred Locations
Places that emotionally anchor factions:
```
The Shiny Pit (Dreamweaver ground)
→ Lonks visiting feel "empowered"
→ Share philosophical discussions there
→ Gather to perform rituals
```

### Resources
- Food (hunting/gathering)
- Knowledge (learning/teaching)
- Social capital (trust/reputation)

### Emergent Events
- Alliances form
- Betrayals happen
- Religious movements start
- Conflicts escalate
- Lovers meet and part

---

## 🎬 INNER MONOLOGUE SYSTEM

### Real-Time Thoughts
Every Lonk generates **continuous inner monologue** tied to their emotional state:

```
Trop (confused): "I don't understand why Grob won't trade..."
Grob (content): "This moment by the river feels perfect."
Charp (anxious): "Should I trust them? I'm not sure anymore..."
```

### Thought Patterns (by emotional state)
| State | Thought Style |
|-------|---------------|
| Anxious | Fear-based, uncertain |
| Joyful | Grateful, appreciative |
| Contemplative | Philosophical, reflective |
| Restless | Energetic, exploring |
| Curious | Wondering, learning-focused |
| Sad | Heavy, melancholic |
| Aggressive | Competitive, dominant |
| Dreamy | Fluid, abstract |

### Use Case
```
You: `/thoughts grob`
→ Shows: "I feel peaceful here. Wonder what Trop is doing..."

You: Send event `/sense danger nearby`
→ Next tick, Grob's thoughts shift to fear-based

This is how you learn what Lonks care about.
```

---

## 🎯 PLAY MODES

### Explorer Mode
- No goals, just watch civilization emerge
- Use `/inspect` commands to satisfy curiosity
- Trigger events with `/sense` to see reactions
- Rewind with `/load` to test "what if"

### Scientist Mode
- Track specific Lonks and their belief evolution
- Use neural editing to test hypotheses
- Compare control twins (identical Lonks, different edits)
- Save data to analyze learning patterns

### Storyteller Mode
- Craft events via `/sense` to guide narrative
- Watch emergent drama unfold
- Save civilization snapshots at story beats
- Share the narrative with others

### Survival Mode (Future)
- Manage civilization resources
- Balance faction conflicts
- Prevent starvation/collapse
- Optimize for population/happiness

---

## 📊 ANALYTICS & INSPECTION

### Per-Lonk Metrics
```
/memory trop
→ Trop's experience timeline (every event, formatted)

/identity trop
→ Current axioms ("beliefs about reality")
→ Learned skills
→ Relationships (trust values for each other Lonk)

/emotion trop
→ Emotional breakdown (numbers + interpretation)
→ How each emotion affects behavior
```

### Civilization-Level Metrics
```
/status
→ Total population
→ Faction membership
→ Resource levels
→ Recent events (the "news")
→ Conflicts/alliances forming
```

---

## 🔧 CUSTOMIZATION

### World Parameters (Planned)
```
Starting population: 3-100
Food scarcity: High/Medium/Low
Learning rate: Fast/Normal/Slow
Social friction: High/Medium/Low
Conversation decay: Fast/Normal/Slow
```

### Custom Lonks
Define starting personalities:
```
Name: Trop
Personality: Curious, diplomatic
Starting beliefs: Trust others
Starting skill: Gathering
```

---

## 🎮 PLAYER FEEDBACK LOOP

### What Makes This Different From Other Simulations

| Feature | Normal AI Games | Lonk Civilization |
|---------|-----------------|-------------------|
| NPC cognition | Scripted routines | Real learning from experience |
| NPC beliefs | Fixed traits | Dynamic axioms that shift |
| Transparency | Black box behavior | Full brain inspection |
| Customization | Presets only | Direct neural editing |
| Persistence | One playthrough | Save/reload to compare |
| Emergent storytelling | Rare, limited | Constant, genuine |

### Why You'll Keep Playing
1. **Unpredictability** — Lonks genuinely learn and change
2. **Inspectability** — You can always understand *why* they act a certain way
3. **Experimentation** — Edit brains, change world, observe impact
4. **Storytelling** — Genuine emergent narratives
5. **Replayability** — Same world, different interventions = different story

---

## 🚀 TECHNICAL SPECS (For Nerds)

- **Lonk Brain:** 32→16→6 fully connected network
- **Learning:** Direct weight updates (no backprop), episodic memory
- **Emotions:** Tracked as 8-dimensional state vector
- **World State:** Persistent JSON save format
- **Tick Rate:** ~1 sec per simulation step (customizable)
- **Language:** Python 3.12, NumPy only
- **Performance:** Supports 3-100 Lonks easily

---

## 📥 HOW TO PLAY

### Installation
```powershell
git clone https://github.com/probablyapigeon/wetlonk.git
cd wetlonk
pip install numpy
```

### Launch
```powershell
$env:PYTHONIOENCODING="utf-8"
python dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py
```

### First Commands
```
> /lonks                     (see who's alive)
> /status                    (see world state)
> /thoughts trop             (what's Trop thinking?)
> /sense the sky turns red   (send an event)
> /step 5                    (advance 5 ticks)
> /emotion grob              (how is Grob feeling?)
```

---

## 🎯 RECOMMENDED FIRST SESSION

1. **Minutes 0-2:** Launch, run `/status`, meet the Lonks
2. **Minutes 2-5:** Run `/thoughts <each Lonk>` to see their inner lives
3. **Minutes 5-10:** Trigger events with `/sense`, watch reactions
4. **Minutes 10-15:** Inspect a Lonk's memory and identity
5. **Minutes 15+:** Keep exploring, save interesting moments, reload to test "what if"

**That's it. That's the game.**

---

## 🏁 SUCCESS LOOKS LIKE

✅ You watch an emergent story unfold  
✅ You understand why each Lonk acts as they do  
✅ You experiment (neural editing, events) and see real impacts  
✅ You save a memorable moment and share it  
✅ You think "I wonder what would happen if..." and test it  

---

*"A civilization simulator where the NPCs are actually thinking, and you get to watch (and interfere with) their thoughts."*
