# Rationale: First Run the Tests

Based on Simon Willison's agentic engineering pattern: [First run the tests](https://simonwillison.net/guides/agentic-engineering-patterns/first-run-the-tests/).

## Why This Works

### 1. Verification Over Assumption

If code has never been executed, it is pure luck if it actually works in production. Running the tests first establishes a known-good baseline and ensures the agent is working with code that compiles and passes.

### 2. Codebase Onboarding

When an agent runs the tests, it discovers the test infrastructure, reads the test files, and learns how existing features behave. Tests are executable documentation — they show the agent what the code is supposed to do, not just what it looks like.

### 3. Testing Mindset

An existing passing test suite nudges the agent to write tests for any new changes it makes. The agent sees that testing is a norm in this project and follows suit.

### 4. Maximum Signal in Minimal Words

Four words — "first run the tests" — encode a substantial amount of software engineering discipline:

- They signal that a test suite exists.
- They force the agent to discover how tests are executed in this project.
- The test count reveals project complexity and encourages deeper exploration.
- They establish the expectation that subsequent work should also be tested.

### 5. Connection to TDD

This pattern pairs naturally with red/green TDD. By starting from a green test suite, the agent can confidently make changes and verify nothing breaks — the same feedback loop that makes TDD effective for human developers.

## Key Insight

Traditional excuses for skipping tests — they take too long to write, they need constant rewrites during rapid development — no longer apply when an agent can produce and maintain them in minutes. Tests are no longer optional when working with coding agents.

## Source

Simon Willison, *Agentic Engineering Patterns*, Chapter 2: "First run the tests" (February 2026).
