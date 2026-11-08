# 🎮 LONK CIVILIZATION SIMULATOR - PLAYER'S GUIDE

*A beginner-friendly walkthrough for people who want to play, not read research papers*

---

## WHAT IS THIS GAME?

You're the **Observer** of a civilization. Lonks (cute alien creatures) live, learn, interact, and build societies. Your job is to watch, inspect, influence, and see what story emerges.

**TL;DR:** *Creatures with real AI brains. You watch them think. You can edit their brains. Cool emergent drama happens. 100% offline. No API calls. Privacy-first.*

---

## 🔒 PRIVACY FIRST

This game is **completely offline**:
- ✅ No internet needed
- ✅ No API calls
- ✅ No data tracking
- ✅ Runs on your machine only
- ✅ All computation local

(See NO_API_CALLS.md if you want technical details.)

---

## THE FIRST 5 MINUTES

### Step 1: Launch It
```powershell
$env:PYTHONIOENCODING="utf-8"
python dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py
```

You'll see:
```
🌍 Initializing Lonk civilization...
🏳️ Trop joins the faction: Dreamweavers!
🌍 Trop wanders into The Shiny Pit
...
🧬 [steady] >
```

This is good. The prompt `🧬 [steady] >` is where you type commands.

### Step 2: Meet the Lonks
```
> /lonks
```

Output:
```
🧬 Lonks in civilization:
  Trop: Health=100, Mood=50, Thoughts=0
  Grob: Health=100, Mood=60, Thoughts=0
  Charp: Health=100, Mood=60, Thoughts=0
```

Three Lonks exist. That's your civilization.

### Step 3: See What They're Thinking
```
> /thoughts trop
```

Output:
```
🧬 Trop's Current Thoughts:
  "I wonder what the world holds today..."
  "These dreams feel important somehow."
```

Trop is thinking. Not scripted. Tied to emotions.

### Step 4: Advance Time
```
> /step 5
```

This runs 5 simulation ticks. Lonks act, feel, think, learn.

### Step 5: See What Changed
```
> /emotions grob
```

Output:
```
🧬 Grob's Emotional State:
  Joy: 65 (content, pleased)
  Trust: 55 (cautiously optimistic)
  Curiosity: 70 (interested in surroundings)
  Fear: 20 (relaxed)
```

Grob's emotions are concrete numbers tied to actual decisions.

---

## CORE MECHANICS

### 1. NPCs Have Real Brains

Each Lonk has a **neural network** (32 inputs → 16 hidden → 6 outputs).

Think of it like this:
```
[Sensory input] → [Lonk's brain processes] → [Decision/action]
```

The brain is:
- **Real:** Trained weights, not random
- **Inspectable:** You can see exact neuron values
- **Editable:** You can change weights mid-game and watch behavior shift
- **Learnable:** Weights update as Lonks experience the world

### 2. Lonks Form Beliefs

Lonks don't have fixed traits. They build **axioms** (beliefs) from experience:

```
Event 1: Grob trades fairly with Trop
Trop's brain: "Grob seems trustworthy" ✅

Event 2: Grob lies to Trop
Trop's brain: Contradiction detected! Belief system unstable.
Trop's response: Emotional spike (betrayal, fear)
New axiom: "Grob is deceptive" ✅

Result: Trop avoids Grob now.
```

You watch this happen in real-time:
```
> /thoughts trop
"Grob betrayed me... I don't know if I can trust them again."

> /identity trop
Axiom: "Grob cannot be trusted"
Relationship: Grob (Trust: -30, recent betrayal)
```

### 3. Emotions Drive Behavior

Lonks have 8 emotional dimensions:
- **Joy** → generous, creative
- **Fear** → cautious, withdrawn
- **Curiosity** → explorative, experimental
- **Anger** → aggressive, confrontational
- **Trust** → cooperative, open
- **Disgust** → dismissive, critical
- **Surprise** → reactive, alert
- **Sadness** → withdrawn, reflective

Same situation, different emotional states = different choices.

### 4. Inner Monologue is Continuous

Every Lonk is always thinking:

```
Trop (curious):      "I wonder what's beyond the mountains..."
Grob (joyful):       "This peace feels so right."
Charp (anxious):     "What if I'm not strong enough?"
```

It's **not dialogue**—it's their actual internal state rendered as text.

### 5. Learning Spreads Between Lonks

One Lonk learns how to hunt. Another watches. The second Lonk now knows hunting too.

Knowledge doesn't vanish. It propagates through the civilization like culture.

---

## YOUR PLAYER COMMANDS

### INSPECTION (Read-Only)

```
/lonks                    List all Lonks + stats
/status                   World overview (population, factions, events)
/thoughts <name>          What is <name> thinking right now?
/memory <name>            <name>'s experience timeline
/identity <name>          <name>'s beliefs, skills, relationships
/emotion <name>           <name>'s emotional state (8 values)
```

### WORLD CONTROL

```
/sense <event>            Send an event to the world
                          Example: /sense the sky turns red
                          
/step <n>                 Advance n ticks (default 1)
                          Example: /step 10

/style <name>             Change UI style
                          Choices: normal, soft, intense, dreamy, steady
```

### PERSISTENCE

```
/save <filename>          Save world + all Lonk brains as JSON
/load <filename>          Load previously saved world
/quit                     Exit
```

---

## GAME FLOW: THE FIRST SESSION

### Phase 1: Observation (5 mins)
- `/lonks` — Meet everyone
- `/thoughts <each lonk>` — Hear their inner voices
- `/status` — See what's happening in the world
- `/step 3` — Advance a few ticks
- `/emotion grob` — See how emotions changed

**Goal:** Understand the basic state of the world.

### Phase 2: Interaction (10 mins)
- `/sense something interesting` — Send an event
- Watch what Lonks do next
- `/thoughts <name>` — See how they react
- `/step 5` — Advance to let them process
- Repeat with different events

**Goal:** See how Lonks respond to external input.

### Phase 3: Analysis (10 mins)
- `/memory trop` — See Trop's full history
- `/identity grob` — See Grob's worldview
- `/emotion charp` — Understand Charp's emotional state
- `/thoughts <name>` — Check if feelings match internal state

**Goal:** Understand why each Lonk makes the choices they do.

### Phase 4: Experimentation (Ongoing)
- `/save my_world_v1.json` — Save this moment
- `/sense crazy_event` — Trigger something
- `/step 10` — Let it play out
- `/load my_world_v1.json` — Reload the save
- Try something different second time
- Compare outcomes

**Goal:** Answer "what if?" questions.

---

## PLAY STYLES

### Style 1: Naturalist (Passive Observer)
- Just watch the simulation
- Use `/inspect` commands to understand behavior
- Don't trigger events; let civilization grow naturally
- Take notes on emergent stories

**Why:** See what Lonks do when left alone.

### Style 2: Scientist (Experimenter)
- Trigger events
- Save state
- Reload and try different intervention
- Compare outcomes
- Use `/memory` to track who learned what

**Why:** Test "if I do X, what happens?"

### Style 3: Storyteller (Creative Director)
- Use `/sense` to craft narrative beats
- Trigger drama
- Watch emergent plots unfold
- Save at story climaxes
- Share the narrative with friends

**Why:** Let Lonks tell a story you co-author.

### Style 4: Hacker (Neural Editor)
- Inspect individual Lonk brains
- Edit neural weights
- Watch immediate behavior change
- A/B test Trop with original weights vs. modified
- Gather data on "why does this neuron matter?"

**Why:** Understand the connection between brain and behavior.

---

## EXAMPLE SESSION: THE BETRAYAL ARC

### Tick 0-10
```
> /step 10
[Trop and Grob interact multiple times, build relationship]

> /identity trop
Axiom: "Grob is my ally"
Relationship: Grob (Trust: +85)
```

### Tick 10-20
```
> /sense grob_steals_trop_food
[World event sent]

> /thoughts trop
"Grob took my food... Why would they do that?"

> /emotion trop
Fear: 75 (spiked), Trust: 25 (crashed)
```

### Tick 20-30
```
> /step 5
[Let Lonks react]

> /thoughts grob
"Trop's avoiding me now. I didn't think they'd care..."

> /memory trop
[Timeline shows Grob betrayal as major event]
```

### Tick 30-40
```
> /identity trop
Axiom: "Grob cannot be trusted"
Relationship: Grob (Trust: -40)

> /thoughts trop
"I'll avoid that area. Too risky."
```

### Tick 40+
```
[Lonks naturally separate, stop cooperating]
[This changes faction dynamics]
[Other Lonks take sides]
[You have a civilization drama arc]

> /save betrayal_arc.json
[Keep the story for later]
```

**You didn't script this. Lonks built it.**

---

## WHAT MAKES THIS UNIQUE

### vs. The Sims
- Sims: Scripted behavior with random variation
- Lonks: Genuine learning from experience

### vs. Other Simulation Games
- Usually: Black-box NPC behavior
- Lonks: You can see exactly why they decide things

### vs. Traditional AI Systems
- Usually: Can't edit live weights
- Lonks: Edit brains mid-simulation, watch changes instantly

### vs. Rule-Based Game AI
- Usually: Hardcoded behaviors
- Lonks: Learned behaviors, adaptable, emergent

**Lonks:** Real learning + Full transparency + Direct manipulation

---

## TIPS FOR MAXIMUM FUN

1. **Take Saves Seriously**
   - Save before big events
   - Reload to try different things
   - Compare outcomes
   - This is how you explore "what if"

2. **Read the Inner Monologue**
   - `/thoughts <name>` is your window into motivation
   - It's not dialogue; it's real cognition rendered as speech
   - Pay attention to mood/emotion shifts in the thoughts

3. **Track Relationships**
   - `/identity <name>` shows who trusts/distrusts whom
   - Watch how relationships form and break
   - See how beliefs about each other change

4. **Use Events Strategically**
   - `/sense` isn't for spam; use it for major story moments
   - Let the simulation run naturally most of the time
   - Intervene only when you want to test something

5. **Save Interesting Moments**
   - Emergent stories are precious
   - Save before you reload
   - You might want to replay it later

---

## TROUBLESHOOTING

**Q: I don't see much happening**  
A: Run `/step 20` to advance more ticks. Stuff takes time.

**Q: The Lonks seem random**  
A: They're not random; they're learning. Use `/memory` and `/identity` to see what shaped them.

**Q: Can I edit weights manually?**  
A: Not yet through the CLI, but the code supports it. That's future work.

**Q: Why do Lonks forget things?**  
A: Conversations decay naturally. It's more realistic; not everything lasts forever.

**Q: Can I add more Lonks?**  
A: Edit the startup code in the Python file. Future versions will have a CLI for this.

---

## WHAT YOU'RE REALLY EXPERIENCING

You're watching an AI system where:

1. **Learning is real** — Not simulated, actual weight updates from experience
2. **Cognition is visible** — You can inspect why it decided something
3. **Beliefs evolve** — Not fixed traits, dynamic worldviews
4. **Emotions matter** — They directly affect decisions
5. **Knowledge spreads** — Skills and beliefs propagate through society
6. **Emergence is genuine** — Stories you didn't write unfold before you

This isn't a game with NPCs. It's more like **watching an alien civilization come to life**, where you can see their thoughts and occasionally nudge their world.

---

## NEXT STEPS AFTER YOUR FIRST SESSION

- Read **GAME_FEATURE_SPEC.md** for full command list
- Read **HOW_TO_EXPLAIN_THIS.md** for how to pitch this to friends
- Check GitHub for updates: https://github.com/probablyapigeon/wetlonk
- Experiment with `/sense` events you think will be interesting
- Track specific Lonks across multiple sessions
- Build a civilization story arc over time

---

## ONE MORE THING

This is a **research prototype**, not a finished product.

- **Works:** All the core stuff (learning, beliefs, emotions, inspection)
- **Missing:** Some UI polish, config file support, more customization
- **But:** What's there is genuinely novel

That's why you should play it: not because it's a polished game, but because it's showing something that hasn't been done this way before.

Now go. Launch it. Mess with it. See what stories your Lonks tell.

`python dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py`

---

*Questions? Check the full docs at https://github.com/probablyapigeon/wetlonk*
