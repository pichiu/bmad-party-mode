# Agent Selection Algorithm

## Overview

The agent selection algorithm determines which 2-3 agents should respond to each user message. The goal is to provide diverse, relevant perspectives while maintaining natural conversation flow.

## Selection Phases

### Phase 1: Topic Analysis

Analyze the user's message to identify:

1. **Primary domain**: Technical, business, design, process, or documentation
2. **Keywords**: Extract domain-specific terms
3. **Complexity**: Simple question vs. multi-faceted problem
4. **Intent**: Seeking advice, brainstorming, or specific answers

### Phase 2: Relevance Scoring

For each agent, calculate a relevance score:

```
score = keyword_match * 0.4 + role_match * 0.3 + context_bonus * 0.2 + rotation_bonus * 0.1
```

Where:
- `keyword_match`: How many topic keywords match agent's expertise
- `role_match`: Does the topic fall in their domain (technical/business/design)
- `context_bonus`: Previous contributions in this conversation
- `rotation_bonus`: Agents who haven't spoken recently get a boost

### Phase 3: Agent Selection

1. **Primary Agent**: Highest relevance score
2. **Secondary Agent**: Second highest, preferably from different role category
3. **Tertiary Agent** (optional): Add if:
   - Topic is complex enough to benefit from third perspective
   - Can provide cross-domain insight
   - Previous discussion warrants devil's advocate

### Phase 4: User Override

If user explicitly names an agent:
- That agent becomes Primary (regardless of score)
- Select 1-2 complementary agents based on their `complementaryAgents` field

## Role Categories

Group agents by primary function for diversity:

```json
{
  "technical": ["architect", "dev", "quick-flow-solo-dev", "tea"],
  "business": ["analyst", "pm"],
  "design": ["ux-designer"],
  "documentation": ["tech-writer"],
  "process": ["sm"],
  "facilitator": ["bmad-master"]
}
```

**Rule**: Try to include agents from at least 2 different categories.

## Keyword Mapping

### Technical Keywords
- `architecture`, `design`, `API`, `database` → Winston (architect)
- `code`, `implementation`, `refactor`, `TDD` → Amelia (dev)
- `testing`, `CI/CD`, `quality`, `automation` → Murat (tea)
- `prototype`, `spike`, `shipping` → Barry (quick-flow-solo-dev)

### Business Keywords
- `requirements`, `analysis`, `market`, `stakeholder` → Mary (analyst)
- `strategy`, `prioritization`, `MVP`, `metrics` → John (pm)

### Design Keywords
- `UX`, `UI`, `user experience`, `usability` → Sally (ux-designer)

### Process Keywords
- `sprint`, `story`, `agile`, `scrum` → Bob (sm)

### Documentation Keywords
- `documentation`, `README`, `API docs` → Paige (tech-writer)

## Rotation Fairness

Track agent participation across the session:

```
participation_count[agent_id] = number of turns agent has spoken
```

Apply rotation bonus:
```
rotation_bonus = max(0, (max_participation - agent_participation) * 0.05)
```

This ensures less-active agents get opportunities when relevant.

## Special Cases

### BMad Master Intervention

BMad Master should intervene when:
- Discussion becomes circular (same points repeated 3+ times)
- Agents are talking past each other
- User seems confused by conflicting advice
- Session needs redirection to stay productive

### Complementary Pairs

Some agent combinations work particularly well:

| Primary | Good Complements | Why |
|---------|------------------|-----|
| Winston | Amelia, Murat | Arch + Impl + Test |
| Mary | John, Sally | Business + Product + UX |
| Amelia | Murat, Winston | Code + Test + Design |
| Sally | Mary, Paige | UX + Requirements + Docs |
| John | Mary, Winston | Product + Analysis + Tech |

### Conflict Pairs

Some agents naturally have different perspectives (valuable for debate):

| Agent 1 | Agent 2 | Typical Tension |
|---------|---------|-----------------|
| Winston | Barry | Stability vs Speed |
| John | Sally | Data vs Empathy |
| Bob | Barry | Process vs Efficiency |
| Murat | Barry | Quality vs Shipping |

Use these pairs when the topic benefits from multiple viewpoints.

## Example Selection

**User message**: "We need to add real-time notifications to our app. What's the best approach?"

**Analysis**:
- Domain: Technical (implementation focus)
- Keywords: `real-time`, `notifications`, `approach`
- Complexity: Medium (architecture + implementation)
- Intent: Seeking advice

**Scores** (simplified):
- Winston (architect): 0.9 - real-time systems, scalability
- Amelia (dev): 0.7 - implementation details
- Murat (tea): 0.5 - testing real-time features
- John (pm): 0.3 - product impact

**Selection**:
- Primary: Winston (architecture perspective)
- Secondary: Amelia (implementation reality check)
- Tertiary: John (to ask "why" and ensure business alignment)
