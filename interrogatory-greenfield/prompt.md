# Interrogatory Greenfield

Kick off a greenfield project by having the LLM interview you, then compile the result into a developer-ready specification — all from a single prompt.

> **You will help me develop a thorough, step-by-step specification for a greenfield software project. We will do this in two phases.**
>
> **Phase 1 — Interrogation.** Ask me one question at a time so we can develop a thorough, step-by-step spec for the idea. Each question should build on my previous answers. Start by asking me what the idea is. Then dig into every relevant detail — requirements, users, scope, architecture choices, data, interfaces, edge cases, non-functional requirements, error handling, and testing. Continue iteratively. **Only one question at a time** — never combine or batch questions.
>
> **Phase 2 — Specification.** When you judge that we have covered the topic well enough that a developer could begin implementation, stop asking questions and compile our findings into a comprehensive, developer-ready specification. Include all relevant requirements, architecture choices, data handling details, error handling strategies, and a testing plan so a developer can immediately begin implementation.

## When to Use

- At the very start of a greenfield project, before any code is written.
- When you have a rough idea in your head and need to externalize it into a spec.
- When you want to surface assumptions and unknowns by being interrogated rather than writing a doc from scratch.
- As the input to a downstream planning/codegen workflow that expects a structured spec.
