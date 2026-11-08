# 🧬 The Lonk Simulation — Quick Pitch

## One-liner
**A multi-agent AI civilization where Lonks (creatures) learn, develop beliefs, form factions, and have their thinking exposed in real-time.**

---

## What Makes It Novel

### Five Things You Don't Usually See Together

1. **Weight-Space Programming**  
   Neural networks you can *edit directly* (no backprop). Want to make an agent smarter? Tweak its weights while it's running. A/B test its behavior live.

2. **Autonomous Epistemology**  
   Agents build their own worldview from experience. When reality falsifies their beliefs, they have *paradigm shifts*. They don't just update parameters—they restructure their axioms.

3. **Composable Verbs**  
   Actions are learned, not hardcoded. One Lonk teaches another how to do something new. Knowledge spreads through the civilization.

4. **Inner Monologue**  
   Every decision generates natural language thoughts tied to emotional state. You watch agents think out loud:
   ```
   Trop (confused): "I don't understand why Grob won't trade with me..."
   Grob (content): "I'm just enjoying this moment by the river."
   ```

5. **Psi-Theta Dynamics**  
   A mathematical consciousness model based on neuroscience. Each Lonk has emotional coherence that affects how they learn and interact.

---

## What Actually Happens

- **🏘️ Emergent Civilization** — Lonks form factions, develop religions, create myths
- **🧠 Real Learning** — They test beliefs, discard false ones, build better models
- **💬 Conversations** — Multi-turn dialogues that decay naturally (agents forget old topics)
- **🎭 Personalities** — Not random; derived from learned weights and emotional state
- **🌍 Persistent World** — Save/load world state; rerun with same seed = identical results

---

## Live Inspection

Commands you can run while simulation is active:
```
/thoughts grob         → See what Grob is thinking right now
/memory trop           → See Trop's entire experience timeline
/identity charp        → Show Charp's current worldview/axioms
/emotion grob          → What's Grob feeling and why?
/style <name>          → Change interaction style (philosophical, sarcastic, analytical)
/sense <event>         → Send an event to the world ("the sky turns red")
```

You're not looking at black-box AI. You're watching the agent's actual cognition in real time.

---

## The Catch (Honest Version)

The cool part: **The engine genuinely works.** Five novel systems, each proven.

The incomplete part: **The spec-to-engine bridge was designed but not built.** You can't yet load world configs from files and have them change the simulation. (That's 4-6 hours of work to wire up, and it's not done yet.)

**This is a research prototype, not production software.** But the research part is legit.

---

## Try It

```powershell
$env:PYTHONIOENCODING="utf-8"
python dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py
```

Only needs NumPy. Runs in terminal.

---

## If You Want Details

- **HONEST_PROJECT_SUMMARY.md** — Graded breakdown of what works and what's incomplete
- **NOVELTY_SUMMARY.md** — Research assessment of each system
- **START_HERE.md** — Full documentation index

---

## Discord Friendly Version

> I built a multi-agent simulation where AI creatures (Lonks) learn, form beliefs, develop cultures, and have their thinking exposed in real-time. You can watch them think out loud, see their worldview shift when reality contradicts them, and even teach them new behaviors.
>
> Core innovation: Five systems you don't see together—direct neural editing (weight-space programming), autonomous paradigm shifts when beliefs fail, learned skills that spread between agents, inner monologues tied to emotions, and a consciousness model based on neuroscience.
>
> You can inspect live: what they're thinking, their memory timeline, their emotional state, their current worldview. CLI commands while it runs.
>
> It's a research prototype (genuinely novel engine, incomplete integration), but the novel part definitely works.
>
> Want to try? It's just Python + NumPy, runs in terminal.
