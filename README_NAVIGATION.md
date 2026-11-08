# 📚 HOW TO NAVIGATE THE DOCUMENTATION

This repo has a LOT of docs. Here's how to find what you need based on who you are and what you want.

---

## 🎮 YOU JUST WANT TO PLAY

Start here:
1. **[PLAYERS_GUIDE.md](PLAYERS_GUIDE.md)** ← Read this first (5 min read)
   - Step-by-step walkthrough of first 5 minutes
   - What the game mechanics are
   - How to use player commands
   - 4 different play styles

2. **[GAME_FEATURE_SPEC.md](GAME_FEATURE_SPEC.md)** ← Full feature reference
   - Every command and what it does
   - Stats and NPC systems explained
   - All mechanics in one place
   - Comparison to other games

3. **Launch it:**
   ```powershell
   $env:PYTHONIOENCODING="utf-8"
   python dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py
   ```

---

## 💬 YOU WANT TO EXPLAIN THIS TO FRIENDS

Start here:
1. **[HOW_TO_EXPLAIN_THIS.md](HOW_TO_EXPLAIN_THIS.md)** ← Pitch templates
   - Tweet length (30 seconds)
   - Elevator pitch (1 minute)
   - Deep dive (5 minutes)
   - FAQ for common questions

2. **[DISCORD_READY.md](DISCORD_READY.md)** ← Copy-paste for Discord/Twitter
   - Full message ready to paste
   - Short version for character limits
   - FAQ included

3. **[DISCORD_PITCH.md](DISCORD_PITCH.md)** ← Structured explanation
   - One-liner definition
   - Five novel systems explained
   - Live inspection commands
   - How to try it

---

## 🧠 YOU WANT TO UNDERSTAND THE TECH

Start here:
1. **[HONEST_PROJECT_SUMMARY.md](HONEST_PROJECT_SUMMARY.md)** ← What actually works
   - Graded assessment (Engine A, Integration F, Overall B)
   - What's complete vs. incomplete
   - Three paths forward

2. **[REPRODUCIBILITY_AUDIT.md](REPRODUCIBILITY_AUDIT.md)** ← Technical audit
   - Code inspection of spec-to-engine bridge
   - Why specs don't control the engine
   - What's missing and why
   - How long to fix it

3. **[NOVELTY_SUMMARY.md](NOVELTY_SUMMARY.md)** ← Research assessment
   - Each of the 5 novel systems graded
   - Why they're worth attention
   - How they fit together
   - Comparison to published work

4. **[NOVELTY_ANALYSIS.md](NOVELTY_ANALYSIS.md)** ← Deep tech dive
   - Detailed explanation of each system
   - Code architecture
   - Design decisions
   - Academic context

---

## 📖 YOU WANT A QUICK OVERVIEW

Pick one:

**5 minutes:** [START_HERE.md](START_HERE.md)
- Fastest path to understanding
- What it is + how to try it
- Key features at a glance

**10 minutes:** [QUICK_START.md](QUICK_START.md)
- More detail than START_HERE
- All major commands listed
- Common use cases

**20 minutes:** [NOVELTY_SUMMARY.md](NOVELTY_SUMMARY.md)
- Full explanation of why it matters
- Each system broken down
- Research context

---

## 🔍 YOU WANT TO INSPECT THE CODE

See:
- **[NOVELTY_SYSTEMS_ARCHITECTURE.md](NOVELTY_SYSTEMS_ARCHITECTURE.md)** ← Code organization
  - Class hierarchies
  - File structure
  - How systems connect

- **[dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py](dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py)** ← Main engine
  - 4,500+ lines
  - All systems implemented here

- **[xembra.py](xembra.py)** ← XEMBRA terminal system
  - Reactive character interface
  - Alternative UI

---

## 🎯 YOU WANT TO DO SOMETHING SPECIFIC

### "Run the simulator"
→ [QUICK_START.md](QUICK_START.md)

### "Understand what makes it novel"
→ [NOVELTY_SUMMARY.md](NOVELTY_SUMMARY.md)

### "Explain it to technical people"
→ [NOVELTY_ANALYSIS.md](NOVELTY_ANALYSIS.md)

### "Explain it to non-technical people"
→ [HOW_TO_EXPLAIN_THIS.md](HOW_TO_EXPLAIN_THIS.md)

### "Copy-paste a Discord message"
→ [DISCORD_READY.md](DISCORD_READY.md)

### "Understand what's working vs. incomplete"
→ [HONEST_PROJECT_SUMMARY.md](HONEST_PROJECT_SUMMARY.md)

### "See technical audit of specs vs. engine"
→ [REPRODUCIBILITY_AUDIT.md](REPRODUCIBILITY_AUDIT.md)

### "Understand the architecture"
→ [NOVELTY_SYSTEMS_ARCHITECTURE.md](NOVELTY_SYSTEMS_ARCHITECTURE.md)

### "Play it as a game"
→ [PLAYERS_GUIDE.md](PLAYERS_GUIDE.md)

### "See all commands as a reference"
→ [GAME_FEATURE_SPEC.md](GAME_FEATURE_SPEC.md)

### "Know which docs exist and when to read them"
→ You are here! [README_NAVIGATION.md](README_NAVIGATION.md)

---

## 📊 DOCUMENTATION MAP

```
For Players:
  ├─ PLAYERS_GUIDE.md (beginner walkthrough)
  ├─ GAME_FEATURE_SPEC.md (reference)
  └─ QUICK_START.md (fastest launch)

For Explainers:
  ├─ HOW_TO_EXPLAIN_THIS.md (pitch templates)
  ├─ DISCORD_READY.md (copy-paste)
  └─ DISCORD_PITCH.md (structured explanation)

For Developers:
  ├─ NOVELTY_SUMMARY.md (research overview)
  ├─ NOVELTY_ANALYSIS.md (deep technical)
  ├─ NOVELTY_SYSTEMS_ARCHITECTURE.md (code organization)
  └─ REPRODUCIBILITY_AUDIT.md (what's missing)

For Evaluators:
  ├─ HONEST_PROJECT_SUMMARY.md (graded assessment)
  ├─ REPRODUCIBILITY_AUDIT.md (technical audit)
  └─ NOVELTY_ANALYSIS.md (research quality)

Quick Access:
  ├─ START_HERE.md (5 min overview)
  ├─ README.md (GitHub main page)
  └─ INDEX.md (alternative navigation)
```

---

## 🎓 READING PATHS BY INTEREST

### Path 1: Game Enthusiast
1. PLAYERS_GUIDE.md (understand how to play)
2. GAME_FEATURE_SPEC.md (learn all commands)
3. Launch and play!

**Time:** 30 minutes to playable

### Path 2: Technical Explainer
1. HOW_TO_EXPLAIN_THIS.md (pick your pitch)
2. NOVELTY_SUMMARY.md (understand what to pitch)
3. DISCORD_READY.md (copy-paste when asked)

**Time:** 20 minutes to ready

### Path 3: Researcher
1. NOVELTY_SUMMARY.md (overview)
2. NOVELTY_ANALYSIS.md (deep dive)
3. NOVELTY_SYSTEMS_ARCHITECTURE.md (code)
4. Source code (directinspection)

**Time:** 2-3 hours to understand fully

### Path 4: Evaluator (Honest Assessment)
1. HONEST_PROJECT_SUMMARY.md (graded assessment)
2. REPRODUCIBILITY_AUDIT.md (technical findings)
3. NOVELTY_ANALYSIS.md (research quality)
4. Source code (verification)

**Time:** 1-2 hours to complete assessment

### Path 5: Quick Demo
1. START_HERE.md (what is this?)
2. QUICK_START.md (how to run)
3. Launch and run `/lonks`, `/thoughts trop`, `/step 5`
4. Done!

**Time:** 10 minutes

---

## 🔑 KEY FACTS (No Reading Required)

- **What:** Multi-agent AI civilization simulator
- **Novel systems:** 5 (weight-space programming, autonomous epistemology, learned verbs, inner monologue, psi-theta dynamics)
- **Grade:** Engine A, Code A, Integration F, Overall B
- **Status:** Research prototype (works, incomplete integration)
- **Dependencies:** Python 3.12, NumPy only
- **How to run:** `python dynamiclonk-py-v13-lonks-finally-have-ears-say-command-fixed.py`
- **Honest note:** Specs exist but engine doesn't read them (yet)
- **Play time:** 10 minutes to "wow, this is interesting"
- **Open source:** Yes (MIT license)

---

## 📞 STILL CONFUSED?

**"Which file should I read?"**
- If you want to *play*: → PLAYERS_GUIDE.md
- If you want to *explain*: → HOW_TO_EXPLAIN_THIS.md
- If you want to *understand*: → NOVELTY_SUMMARY.md
- If you want to *develop*: → NOVELTY_ANALYSIS.md
- If you want to *evaluate*: → HONEST_PROJECT_SUMMARY.md

**"I just want to know if this is worth my time"**
→ Read HONEST_PROJECT_SUMMARY.md (5 min) then decide

**"I want to show this to someone"**
→ Use DISCORD_READY.md (copy-paste ready)

**"I want to know exactly what works and what doesn't"**
→ Read REPRODUCIBILITY_AUDIT.md

**"I want to understand why this is different from other AI"**
→ Read NOVELTY_ANALYSIS.md sections on each system

---

## ✅ VERIFICATION CHECKLIST

Before you engage with this project, confirm:

- ✅ Engine runs without errors (verified in session)
- ✅ All documentation on GitHub (committed and pushed)
- ✅ Honest assessment included (not overstated claims)
- ✅ Multiple pathways for different audiences
- ✅ Game and research presentations both available
- ✅ Quick-start options (5 min to playable)
- ✅ Deep-dive options (research assessment)
- ✅ Copy-paste ready for social media
- ✅ No dependencies beyond NumPy

---

## 🚀 NEXT STEPS

1. **Pick your role** (player / explainer / developer / evaluator)
2. **Read the matching path** (see above)
3. **Either play or explain** (depending on your role)
4. **Share it with others** (use DISCORD_READY.md if needed)

---

*Last updated: Session 72dbef30*  
*All documentation pushed to: https://github.com/probablyapigeon/wetlonk*
