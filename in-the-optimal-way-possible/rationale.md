# Rationale: In The Optimal Way Possible (ITOWP)

Based on a LinkedIn post by Jeffrey Emanuel ([@jeffreyemanuel](https://www.linkedin.com/in/jeffreyemanuel/)) framed as an "Agent Coding Lifehack."

## The Original Tip

> Agent Coding Lifehack:
>
> This one sounds about as silly as adding "make no mistakes" at the end of your request, but I've been having great results from liberally sprinkling "in the optimal way possible" (ITOWP for short) at the end of prompts.
>
> It makes the model think way harder.

## Why This Works

### 1. It Shifts the Objective From "Done" to "Best"

Without a quality bar, an agent's implicit goal is "produce something that satisfies the request." Appending "in the optimal way possible" replaces that with "produce the best version of this." The agent now has to compare alternatives instead of emitting the first plausible one.

### 2. It Forces Trade-off Reasoning

"Optimal" only has meaning relative to constraints — performance, readability, memory, simplicity, extensibility. The phrase pushes the model to surface those axes and reason about them, rather than defaulting to whatever pattern is most common in its training data.

### 3. It's a Low-Cost Thinking Trigger

Like "think step by step," "ultrathink," or "check with fresh eyes," ITOWP is a short phrase that reliably nudges the model into a more deliberate reasoning mode. It costs four words and a handful of tokens but changes the response distribution noticeably.

### 4. It Pairs Well With Review Prompts

ITOWP works at request time; pair it with a follow-up review prompt ("Check over everything again with fresh eyes…") to compound the effect. The first pass aims for optimal; the second pass catches whatever the first pass missed.

## Why It Sounds Silly But Works

Emanuel himself flags that this feels as silly as adding "make no mistakes." The mechanism is the same as other phatic prompt boosters: the words don't carry literal new information, but they shift the model into a state where it allocates more reasoning effort. The lift is empirical, not theoretical — try it and compare.

## Source

Jeffrey Emanuel, LinkedIn post, "Agent Coding Lifehack: …liberally sprinkling 'in the optimal way possible' (ITOWP for short) at the end of prompts."
