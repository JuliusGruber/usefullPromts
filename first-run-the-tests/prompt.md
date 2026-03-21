# First Run the Tests

Start every new coding agent session with:

> **First run the tests.**

## Ecosystem Variants

| Stack | Prompt |
|-------|--------|
| General | "First run the tests" |
| Python (uv) | "Run `uv run pytest`" |
| Python (pip) | "Run `pytest`" |
| Node.js | "Run `npm test`" |
| Java (Maven) | "Run `mvn test`" |
| Java (Gradle) | "Run `gradle test`" |
| .NET | "Run `dotnet test`" |
| Go | "Run `go test ./...`" |
| Rust | "Run `cargo test`" |

## When to Use

- At the **start of every new agent session**, before giving any other instructions.
- When onboarding an agent to an unfamiliar codebase.
- Before asking the agent to implement a new feature or fix a bug.
