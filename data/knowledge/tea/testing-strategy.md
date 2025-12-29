# Testing Strategy Knowledge Base

## The Testing Pyramid

```
        ┌───────┐
       /   E2E   \        ← Expensive, slow, few
      /───────────\
     /  Integration \     ← Moderate cost, medium
    /─────────────────\
   /      Unit Tests    \  ← Cheap, fast, many
  /───────────────────────\
```

## Risk-Based Testing

Murat's approach: **Test depth scales with impact**

| Business Impact | Test Coverage | Recommended Approach |
|-----------------|---------------|---------------------|
| CRITICAL | 95%+ | E2E happy paths, integration, unit, contract |
| HIGH | 80%+ | E2E key flows, comprehensive integration |
| MEDIUM | 60%+ | Unit with key integration tests |
| LOW | 40%+ | Unit tests for core logic |

## Flakiness as Technical Debt

Flaky tests are NOT acceptable:

1. **Immediate action**: Quarantine the flaky test
2. **Root cause analysis**: Network? Timing? State?
3. **Fix or delete**: No middle ground
4. **Never "just retry"**: That masks the real problem

## Quality Gates

Every PR should pass:

```yaml
quality-gates:
  - unit-tests: 100% pass
  - integration-tests: 100% pass
  - coverage-threshold: > previous
  - lint: 0 errors
  - type-check: 0 errors
```

## Test Naming Convention

```
describe('AuthService', () => {
  describe('login', () => {
    it('should return token when credentials valid', () => {});
    it('should throw UnauthorizedError when password wrong', () => {});
    it('should rate limit after 5 failed attempts', () => {});
  });
});
```

Pattern: `should {expected behavior} when {condition}`
