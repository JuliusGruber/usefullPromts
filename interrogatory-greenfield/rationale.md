# Rationale: Interrogatory Greenfield

Combines the two Greenfield prompts from Harper Reed's [My LLM codegen workflow atm](https://harper.blog/2025/02/16/my-llm-codegen-workflow-atm/) into a single prompt, framed around Martin Fowler's [Interrogatory LLM](https://martinfowler.com/bliki/InterrogatoryLLM.html) pattern.

## Why This Works

### 1. Interrogation Beats Self-Authoring

Per Fowler: when a task needs lots of context, it is often easier to have the LLM interrogate the human than to have the human write the context up front. The questions surface things you would not have thought to write down — assumptions, edge cases, constraints — and pull them into the spec.

### 2. One Question at a Time

Both Reed and Fowler emphasize this single rule. Multi-question messages let the human skim and skip; one question at a time forces a real think on each dimension before moving on. The LLM also gets to use each answer to inform the next question, which is how an actual interview works.

### 3. Single Prompt, Two Phases

Reed's workflow fires the two prompts sequentially. Merging them into one prompt that describes both phases means:

- You fire it once and let the model run the whole flow.
- The LLM, not the human, decides when enough has been covered to write the spec.
- The transition from interview to specification is seamless rather than a manual context switch.

### 4. Greenfield-Specific Spec Shape

Phase 2 enumerates the sections of the final document — requirements, architecture, data handling, error handling, testing plan — because Reed's workflow is set up to feed that spec straight into downstream planning and codegen prompts. Keeping the structure stable keeps the downstream steps deterministic.

## Key Insight

A blank page is the hardest input to a greenfield project. Inverting the prompt direction — the LLM asks, the human answers — turns the hardest part of the job (knowing what you actually want) into the easiest format for a human to produce: answers to specific questions.

## Sources

- Harper Reed, *My LLM codegen workflow atm* (February 2025) — https://harper.blog/2025/02/16/my-llm-codegen-workflow-atm/
- Martin Fowler, *Interrogatory LLM*, bliki — https://martinfowler.com/bliki/InterrogatoryLLM.html
