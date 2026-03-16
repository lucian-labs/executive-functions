# Review

Commit reviewed: `8d30416425d6a71e2b3f1ddb2e7242fde354271f`

## Findings

1. `[P1]` ~~The README still overpromises autonomous setup instead of clearly framing Executive Functions as a translation layer.~~ **RESOLVED** in commit following this review. "The AI does the rest" replaced with "Your agent will walk you through the chapters and help you create your first files. You'll make the decisions — the repo gives you the model."

2. `[P1]` ~~The privacy issue remains. The communication profiling chapter still says the agent should extract accessibility and behavioral traits and write that profile into the shared global AGENTS.md.~~ **RESOLVED.** Chapter 09 rewritten with three opt-in approaches (write it yourself, co-create with agent, opt in to analysis). Profile is private by default with local-only storage. Shared storage is an explicit choice. Sensitive details (accessibility, cognitive patterns) recommended for local config only.

3. `[P2]` ~~The guided setup still drifts back into "the agent will figure it out" framing.~~ **RESOLVED.** 02-file-conventions.txt now frames agent help as "you provide the details, agent structures the format." 08-multi-machine.txt bootstrap steps now list the user filling in local details, with agent drafting as an optional assist. Auto-discovery noted as tool-dependent shortcut, not something the system depends on.

## Direction

~~The rewrite improved tone and readability, but it did not fix the substantive messaging problems.~~ All three findings addressed. The repo now frames Executive Functions as an operator model you build with agent assistance — not something agents self-configure from a URL.
