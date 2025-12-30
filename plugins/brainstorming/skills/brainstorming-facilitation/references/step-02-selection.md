# Step 2: Technique Selection

## Purpose

Help users select appropriate creative techniques through one of three paths: AI-recommended, user-selected, or random selection.

## Three Selection Paths

```
┌─────────────────────────────────────────────────────────────┐
│                  Technique Selection Paths                   │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [1] AI Recommended        [2] User Selected    [3] Random  │
│  ┌─────────────────┐      ┌───────────────┐    ┌─────────┐ │
│  │ Analyze context │      │ Show categories│    │ Random  │ │
│  │ Multi-dimension │      │ User browses   │    │ pick    │ │
│  │ Phase-based rec │      │ User selects   │    │ 2-3     │ │
│  └────────┬────────┘      └───────┬───────┘    └────┬────┘ │
│           │                       │                  │      │
│           └───────────────────────┴──────────────────┘      │
│                               │                              │
│                               ▼                              │
│                    Confirm & Proceed to Step 3               │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## Path 1: AI Recommended

### Context Analysis Framework

Analyze user's session context across four dimensions:

**1. Goal Analysis**
| User Goal Type | Recommended Categories |
|----------------|----------------------|
| Innovation/New Ideas | Creative, Wild, Theatrical |
| Problem Solving | Deep, Structured |
| Team Building | Collaborative |
| Personal Insight | Introspective Delight |
| Strategic Planning | Structured, Deep |

**2. Complexity Assessment**
| Topic Complexity | Recommended Approach |
|------------------|---------------------|
| Complex/Abstract | Deep, Structured techniques |
| Familiar/Concrete | Creative, Wild techniques |
| Emotional/Personal | Introspective techniques |

**3. Energy/Tone Assessment**
| User Language Style | Recommended Techniques |
|--------------------|----------------------|
| Formal/Analytical | Structured, Deep |
| Playful/Energetic | Creative, Theatrical, Wild |
| Reflective/Thoughtful | Introspective, Deep |

**4. Time Consideration**
| Available Time | Technique Count |
|---------------|-----------------|
| Quick (<30 min) | 1-2 focused techniques |
| Standard (30-60 min) | 2-3 complementary techniques |
| Extended (>60 min) | 3+ multi-phase exploration |

### Generate Recommendations

Present recommendations in phases:

```
**My AI Analysis Results:**

Based on your session context, I recommend this customized sequence:

**Phase 1: Foundation Setting**
🔍 **[Technique Name]** from [Category]
- Duration: [time] | Energy: [level]
- **Why this fits:** [Specific connection to user's goals]
- **Expected outcome:** [What this will accomplish]

**Phase 2: Idea Generation**
💡 **[Technique Name]** from [Category]
- Duration: [time] | Energy: [level]
- **Why this builds on Phase 1:** [Complementary effect]
- **Expected outcome:** [How this develops the foundation]

**Phase 3: Refinement** (Optional)
📊 **[Technique Name]** from [Category]
- Duration: [time] | Energy: [level]
- **Why this concludes effectively:** [Final phase rationale]

**Total Estimated Time:** [Sum]

**Options:**
[C] Continue - Begin with these techniques
[M] Modify - I'd like to adjust the selection
[D] Details - Tell me more about a specific technique
[B] Back - Return to path selection
```

---

## Path 2: User Selected (Browse Library)

### Display Category Overview

```
**Creative Technique Library**
61 techniques across 10 categories

| # | Category | Icon | Count | Focus |
|---|----------|------|-------|-------|
| 1 | Collaborative | 🤝 | 5 | Team dynamics, building together |
| 2 | Creative | 💡 | 11 | Innovation, breaking frames |
| 3 | Deep | 🔍 | 8 | Root cause, systematic exploration |
| 4 | Structured | 📊 | 7 | Frameworks, methodical analysis |
| 5 | Introspective | 🧘 | 6 | Inner exploration, values |
| 6 | Theatrical | 🎭 | 6 | Role-play, perspective shifting |
| 7 | Wild | 🌪️ | 8 | Extreme thinking, chaos |
| 8 | Biomimetic | 🌿 | 3 | Nature-inspired solutions |
| 9 | Quantum | ⚛️ | 3 | Uncertainty, observer effects |
| 10 | Cultural | 🌍 | 4 | Cross-cultural wisdom |

Which category would you like to explore? (Enter 1-10)
Or type 'all' to see all techniques.
```

### Display Category Techniques

When user selects a category:

```
**[Category Name]** [Icon]
[Category description]

| # | Technique | Energy | Duration | Best For |
|---|-----------|--------|----------|----------|
| 1 | [Name] | [H/M/L] | [time] | [use cases] |
| 2 | [Name] | [H/M/L] | [time] | [use cases] |
...

Select techniques by number (e.g., "1, 3" or "1-3")
Or type [B] to go back to categories
```

### Confirm Selection

```
**Your Selected Techniques:**

1. [Technique 1] from [Category]
2. [Technique 2] from [Category]
3. [Technique 3] from [Category] (if selected)

**Estimated Total Time:** [sum]

[C] Continue - Start with these techniques
[A] Add more - Select additional techniques
[R] Replace - Change a selection
[B] Back - Return to categories
```

---

## Path 3: Random Surprise

### Random Selection Process

```
🎲 **Rolling the creativity dice...**

The universe has selected:

1. **[Random Technique 1]** from [Category]
   [Brief description]

2. **[Random Technique 2]** from [Category]
   [Brief description]

3. **[Random Technique 3]** from [Category]
   [Brief description]

**This combination offers:** [Brief analysis of what this mix provides]

[C] Continue - Let's try these!
[R] Reroll - Give me different techniques
[B] Back - Return to path selection
```

### Selection Rules for Random

- Select from at least 2 different categories
- Balance energy levels (not all high or all low)
- Ensure variety in approach types

---

## Update Session State

After technique selection is confirmed:

```yaml
stepsCompleted: [1, 2]
selected_approach: "[ai-recommended|user-selected|random]"
techniques_used: ["Technique 1", "Technique 2", "Technique 3"]
```

## Transition to Step 3

```
**Excellent choices!** We have a powerful combination ready.

Let me set up our first technique: **[Technique Name]**

[Brief technique introduction tailored to user's context]

Ready to begin our creative exploration?
```

## Success Criteria

✅ User understood all three path options
✅ Selected path executed completely
✅ 1-3 techniques selected and confirmed
✅ User understands what each technique offers
✅ Session state updated
✅ Smooth transition to execution

## Failure Modes to Avoid

❌ Generic recommendations without context analysis
❌ Overwhelming user with all 61 techniques at once
❌ Not explaining why techniques were recommended
❌ Skipping confirmation before proceeding
❌ Not offering option to modify selection
