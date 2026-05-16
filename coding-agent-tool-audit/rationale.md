# Rationale: Tool Audit

Based on Stephane Derosiaux's article: [Claude Code told me what tools it needs to work faster](https://sderosiaux.substack.com/p/claude-code-told-me-what-tools-it).

## Why This Works

### 1. The Agent Knows Its Own Dependencies

Claude Code generates recommendations based on its knowledge of what tools its codebase-analysis features depend on. It knows what it can invoke and what happens when those tools are missing. Asking it directly leverages that self-knowledge.

### 2. Multi-Dimensional Analysis

The prompt asks across four dimensions — installed, missing, broken, redundant — rather than just "what should I install?" This surfaces broken configs and unnecessary clutter alongside gaps, giving a complete picture of the environment.

### 3. Impact-Based Prioritization

By asking to "prioritize by impact on your ability to help me," the response is ranked by practical value rather than presented as a flat list. Critical gaps surface first.

### 4. The Agent Audits Itself

In the author's experience, Claude launched six parallel subagents, looped through every binary in PATH, parsed Homebrew packages, checked MCP server configuration, inspected shell aliases, and cataloged global npm installs. It returned a prioritized report: critical gaps, high-value upgrades, broken configs, and things to uninstall.

## What It Typically Surfaces

- **Faster search tools** (ripgrep, fd, fzf) — shorter commands mean fewer syntax errors and less wasted context.
- **Structured output tools** (git-delta, xh) — cleaner output the AI can parse more accurately.
- **Ad-hoc data tools** (DuckDB) — one SQL query replaces writing Python scripts or chaining jq.
- **Automation tools** (watchexec, just) — reduce back-and-forth and save context tokens.
- **Static analysis tools** (semgrep) — deterministic code analysis versus "the AI thinks this looks like a bug."

## Key Insight

We set up laptops for new engineers — we give them .env files, IDE extensions, CLIs, and credentials. We must do the same for the AI writing code with us. The best way to get more from your AI coding assistant isn't just a better prompt, it's a better PATH.

## Source

Stephane Derosiaux, *Claude Code told me what tools it needs to work faster*, Substack (2025).
