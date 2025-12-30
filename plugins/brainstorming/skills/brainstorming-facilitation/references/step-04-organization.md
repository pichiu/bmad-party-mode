# Step 4: Idea Organization & Action Planning

## Purpose

Transform generated ideas into organized themes, prioritized outcomes, and actionable plans. Optionally export complete session documentation.

## Execution Flow

```
┌─────────────────────────────────────────────────────────────┐
│              Idea Organization Flow                          │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  1. Review All Generated Ideas                               │
│                    ↓                                         │
│  2. Identify Themes & Patterns                               │
│                    ↓                                         │
│  3. Collaborative Prioritization                             │
│                    ↓                                         │
│  4. Action Planning                                          │
│                    ↓                                         │
│  5. Session Summary                                          │
│                    ↓                                         │
│  6. Optional Export                                          │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

## 1. Review All Generated Ideas

Present a comprehensive review of everything discovered:

```
**Let's organize your creative harvest!**

Throughout our session, we explored [X] techniques and generated these ideas:

**From [Technique 1]:**
- [Idea 1]
- [Idea 2]
- [Idea 3]

**From [Technique 2]:**
- [Idea 4]
- [Idea 5]

**From [Technique 3]:** (if applicable)
- [Idea 6]
- [Idea 7]

**Key Insights & Breakthroughs:**
- [Major insight 1]
- [Major insight 2]

**Total: [X] ideas and [Y] key insights**

Does this capture everything? Anything to add before we organize?
```

## 2. Theme Identification

### Collaborative Theme Discovery

```
**Let's find the patterns in your ideas.**

Looking at everything we've generated, I'm seeing some natural groupings:

**Potential Theme 1: [Theme Name]**
Related ideas: [Idea A], [Idea B], [Idea C]
Common thread: [What connects them]

**Potential Theme 2: [Theme Name]**
Related ideas: [Idea D], [Idea E]
Common thread: [What connects them]

**Potential Theme 3: [Theme Name]**
Related ideas: [Idea F], [Idea G], [Idea H]
Common thread: [What connects them]

**Uncategorized:** [Any ideas that don't fit neatly]

Do these themes resonate? Would you organize them differently?
```

### Theme Refinement

If user suggests changes:

```
I see what you mean. Let me reorganize:

**Revised Theme 1: [New Name]**
[Updated grouping]

Does this better capture the patterns you're seeing?
```

## 3. Prioritization

### Present Prioritization Framework

```
**Now let's prioritize these themes and ideas.**

Consider two dimensions:
- **Impact:** How much would this move you toward your session goals?
- **Feasibility:** How readily could you act on this?

**Quick Framework:**

| | High Feasibility | Low Feasibility |
|-|-----------------|-----------------|
| **High Impact** | 🎯 Top Priority | 💎 Big Bets |
| **Low Impact** | ⚡ Quick Wins | 🔮 Future Ideas |

Let's place your top ideas in this framework.

**Which ideas feel like Top Priority (high impact + feasible)?**
```

### Collaborative Placement

```
Based on our discussion, here's how your ideas map:

**🎯 Top Priority:** (High Impact + Feasible)
1. [Idea] - [Why it fits here]
2. [Idea] - [Why it fits here]

**⚡ Quick Wins:** (Lower Impact + Very Feasible)
- [Idea]
- [Idea]

**💎 Big Bets:** (High Impact + More Effort)
- [Idea]

**🔮 Future Exploration:**
- [Idea] - Worth revisiting when [condition]

Does this prioritization feel right? What would you adjust?
```

## 4. Action Planning

### For Top Priority Ideas

```
**Let's turn your top priorities into action.**

**Priority 1: [Idea Name]**

**Why This Matters:**
[Connection to session goals and broader objectives]

**Next Steps:**
1. [Specific, concrete action]
2. [Follow-up action]
3. [Completion action]

**Resources Needed:**
- [Resource 1]
- [Resource 2]

**Success Indicators:**
- [How you'll know it's working]
- [Measurable outcome]

**Timeline Consideration:**
When would you want to start on this?

---

**Priority 2: [Idea Name]**

[Same structure...]

---

Does this action plan feel achievable? What would make it more actionable?
```

### Quick Win Actions

```
**Quick Wins - Easy to Start:**

These can be done with minimal effort:

- **[Quick Win 1]:** [Simple action to take]
- **[Quick Win 2]:** [Simple action to take]

Would you like to commit to one of these quick wins today?
```

## 5. Session Summary

### Generate Summary

```
**Session Summary**

**Topic:** [Session topic]
**Goals:** [Session goals]

**What We Explored:**
- Techniques used: [List]
- Total ideas generated: [Number]
- Key themes identified: [Number]

**Key Achievements:**
- [Major accomplishment 1]
- [Major accomplishment 2]
- [Major accomplishment 3]

**Breakthrough Moments:**
- [Specific breakthrough that stood out]
- [Creative connection that emerged]

**Your Priorities:**
1. [Top priority with brief description]
2. [Second priority]

**Immediate Next Steps:**
- [First action to take]
- [Quick win to pursue]

**For Future Sessions:**
- [Topics to explore further]
- [Questions that emerged]
```

### Session Reflection

```
**Session Reflections:**

What worked well in this session:
- [Observation about productive moments]
- [What techniques resonated]

What I noticed about your creative process:
- [Insight about user's thinking style]
- [Strength you demonstrated]

Any final thoughts before we wrap up?
```

## 6. Optional Export

### Offer Export Option

```
**Would you like to save this session?**

I can create a complete session document with:
- Full session overview
- All generated ideas organized by theme
- Your prioritization results
- Action plans with next steps
- Session insights and reflections

**Options:**
[Y] Yes, save the session document
[N] No, we're done here

If yes, where would you like to save it?
(Default: ./brainstorming-session-[date].md)
```

### If Export Selected

1. Ask for output path (or use default)
2. Read the template from `$CLAUDE_PLUGIN_ROOT/data/templates/session-output.md`
3. Fill in all sections with session content
4. Write the completed document
5. Confirm save location

```
**Session Saved!**

Your complete session documentation has been saved to:
[file path]

This includes:
✅ Session overview and goals
✅ All [X] ideas organized by theme
✅ Prioritization matrix
✅ Action plans for top priorities
✅ Session reflections

You can continue this session later by using:
/bmad-brainstorming
Then selecting "Continue previous session"
```

## 7. Session Close

### Final Message

```
**Thank you for this creative session!**

**Key Takeaways:**
- [Most important insight]
- [Most actionable idea]

**Your Commitment:**
- [Quick win or next step they mentioned]

**Remember:** The best brainstorming is just the beginning.
Take one action today, however small.

Until next time - keep exploring, keep creating! 🚀
```

## Update Final State

```yaml
stepsCompleted: [1, 2, 3, 4]
ideas_generated: ["All final ideas"]
action_items: ["Prioritized actions"]
```

## Success Criteria

✅ All ideas reviewed and acknowledged
✅ Clear themes identified collaboratively
✅ Prioritization reflects user's judgment
✅ Action plans are specific and achievable
✅ User feels sense of accomplishment
✅ Clear next steps identified
✅ Optional export completed successfully

## Failure Modes to Avoid

❌ Rushing through organization
❌ Imposing themes without user input
❌ Creating overwhelming action plans
❌ Skipping the reflection moment
❌ Not offering export option
❌ Ending abruptly without closure
