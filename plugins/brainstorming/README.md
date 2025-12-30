# Brainstorming Plugin

Interactive brainstorming facilitation for Claude Code - AI-powered creative coaching with 61 techniques across 10 categories.

## Features

- **61 Creative Techniques**: Comprehensive technique library covering diverse thinking styles
- **10 Categories**: Collaborative, Creative, Deep, Structured, Wild, Theatrical, Introspective, Biomimetic, Quantum, Cultural
- **3 Selection Paths**: AI-recommended, user-selected, or random surprise
- **Interactive Coaching**: True back-and-forth dialogue, not just Q&A
- **Session Continuity**: Resume interrupted sessions seamlessly
- **Optional Output**: Export complete session documentation

## Technique Categories

| Category | Count | Focus |
|----------|-------|-------|
| Creative | 11 | Innovation, breaking frames |
| Deep | 8 | Root cause analysis, deep exploration |
| Wild | 8 | Extreme thinking, boundary breaking |
| Structured | 7 | Systematic analysis, frameworks |
| Introspective | 6 | Inner exploration, values clarification |
| Theatrical | 6 | Role-playing, perspective shifting |
| Collaborative | 5 | Team dynamics, diverse voices |
| Cultural | 4 | Cross-cultural wisdom, fusion |
| Quantum | 3 | Quantum-inspired thinking |
| Biomimetic | 3 | Nature-inspired solutions |

## Usage

Start a brainstorming session:

```
/bmad-brainstorming
```

Or with a topic:

```
/bmad-brainstorming How can we improve user onboarding?
```

### Session Flow

1. **Language Selection**: Choose your preferred language
2. **Topic & Goals**: Define what you want to explore
3. **Technique Selection**: Choose from 3 paths
   - AI Recommended (personalized suggestions)
   - User Selected (browse the library)
   - Random Surprise (serendipity-driven)
4. **Interactive Execution**: Coaching-style exploration
5. **Idea Organization**: Prioritize and plan actions
6. **Optional Export**: Save session documentation

### During the Session

- The AI acts as a **creative coach**, not just a question-asker
- Explore ideas deeply before moving on
- Say "next technique" anytime to switch
- Ideas are captured organically throughout

### Ending the Session

The session concludes after idea organization. You can:
- Export a complete session document
- Continue refining in conversation
- Start a new session anytime

## Architecture

```
brainstorming/
├── .claude-plugin/
│   └── plugin.json           # Plugin manifest
├── commands/
│   └── bmad-brainstorming.md # Main command
├── skills/
│   └── brainstorming-facilitation/
│       ├── SKILL.md          # Core facilitation skill
│       └── references/
│           ├── step-01-setup.md
│           ├── step-02-selection.md
│           ├── step-03-execution.md
│           └── step-04-organization.md
├── data/
│   ├── techniques-index.json # 61 techniques database
│   └── templates/
│       └── session-output.md # Output template
└── README.md
```

## Credits

This plugin is adapted from the [BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD) project by BMad Code, LLC - an AI-driven agile development framework with specialized workflows.

## License

MIT License - See [LICENSE](LICENSE) for details.

BMad and BMAD-METHOD are trademarks of BMad Code, LLC.
