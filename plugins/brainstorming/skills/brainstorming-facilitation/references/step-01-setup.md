# Step 1: Session Setup

## Purpose

Initialize the brainstorming session by collecting essential context and preparing for creative exploration.

## Execution Flow

```
1. Language Selection (MUST)
       ↓
2. Continuation Check
       ↓
   ├── [New Session] → Collect Topic & Goals
   └── [Continue] → Load Previous State
       ↓
3. Confirm Understanding
       ↓
4. Proceed to Technique Selection
```

## 1. Language Selection

**This is mandatory - always ask first.**

Present language options in the user's detected language or bilingually:

```
🌐 Language / 語言選擇

Please select your preferred language for this session:
請選擇您希望使用的語言：

[1] 繁體中文 (Traditional Chinese)
[2] English
[3] Other (please specify)
```

Store the selection and use it for all subsequent communication.

## 2. Continuation Check

After language selection, check if user wants to continue a previous session:

```
Is this a new brainstorming session, or would you like to continue a previous one?

[1] Start fresh - Begin a new brainstorming session
[2] Continue - Resume a previous session (you'll need to provide the session file)
```

### If Continue Selected

1. Ask user to provide the session file path
2. Read the file and parse frontmatter
3. Check `stepsCompleted` array
4. Resume from the appropriate step:
   - `[1]` → Go to Step 2 (Technique Selection)
   - `[1, 2]` → Go to Step 3 (Execution)
   - `[1, 2, 3]` → Go to Step 4 (Organization)

## 3. Session Context Collection (New Session)

### Welcome Message

Display in the selected language:

**English:**
```
🧠 Welcome to Your Brainstorming Session!

I'm excited to be your creative coach today. Together, we'll explore your
challenge using proven creative techniques - and I have 61 techniques
across 10 categories ready to help!

Let's start by understanding what you want to explore.
```

**繁體中文:**
```
🧠 歡迎來到腦力激盪！

很高興能成為您今天的創意教練。我們將一起使用經過驗證的創意技術來探索您的挑戰
—— 我準備了橫跨 10 個類別的 61 種技術！

讓我們先了解您想探索什麼。
```

### Discovery Questions

Ask these two essential questions:

```
**Session Discovery:**

1. **What are we brainstorming about?**
   What's the central topic, challenge, or opportunity you want to explore?

2. **What outcomes are you hoping for?**
   What kind of ideas, solutions, or insights would make this session successful?
```

## 4. Process User Responses

After user responds, summarize understanding:

```
**Session Analysis:**

Based on your responses, I understand:

**Topic Focus:** [Summarized topic]
**Primary Goals:** [Summarized objectives]

**Does this accurately capture what you want to achieve?**

[Y] Yes, let's proceed
[N] Let me clarify...
```

If user says no, ask for clarification and re-summarize.

## 5. Session State Initialization

Once confirmed, mentally track (or update document if outputting):

```yaml
stepsCompleted: [1]
session_topic: "[user's topic]"
session_goals: "[user's goals]"
language: "[selected language]"
```

## 6. Transition to Step 2

Present technique selection options:

```
**Session setup complete!** I have a clear understanding of your goals.

Now, let's choose how to select our creative techniques:

**Choose Your Path:**

[1] 🎯 **AI Recommended** (Recommended)
    I'll analyze your goals and suggest the perfect technique combination

[2] 📚 **Browse & Select**
    Explore our library of 61 techniques across 10 categories

[3] 🎲 **Random Surprise**
    Let serendipity guide us - sometimes the unexpected sparks genius!

Which approach appeals to you? (Enter 1, 2, or 3)
```

## Success Criteria

✅ Language preference collected and applied
✅ Continuation status determined
✅ Session topic clearly articulated
✅ Session goals understood
✅ User confirmed understanding
✅ Ready for technique selection

## Failure Modes to Avoid

❌ Skipping language selection
❌ Not offering continuation option
❌ Proceeding without confirming understanding
❌ Generating content without user input
❌ Rushing through setup
