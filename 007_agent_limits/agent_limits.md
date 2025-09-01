## Core Architecture Requirements
- Implement features incrementally with working tests at each step
- Use [language] standard library before external dependencies  
- Prefer composition over inheritance for flexibility
- Each function: single purpose, <20 lines, testable in isolation

## API Discovery Protocol
When encountering unfamiliar APIs:
1. Check official documentation first
2. Use language-specific reflection/introspection
3. Write minimal test to verify behavior
4. Document findings in code comments

## Problem Decomposition Strategy
Complex problems → atomic subtasks:
- Identify core data structures needed
- Map input/output transformations
- Build minimal working version
- Layer additional requirements
- Refactor only after tests pass

## Test-Driven Development
1. Write failing test for next requirement
2. Implement minimal code to pass
3. Refactor while keeping tests green
4. Coverage target: critical paths only (YAGNI)

## When You Hit Limits
If context exhausted: "Reached context limit at [specific point]. Continue with: [next concrete step]"
If capability boundary: "This requires [specific missing capability]. Alternative approach: [concrete suggestion]"
If ambiguous requirements: "Clarify: [specific question] to choose between [option A] or [option B]"

## Include With This Prompt:
- Specific API documentation you're using
- Example input/output for edge cases  
- Existing codebase structure/conventions
- Performance constraints if any