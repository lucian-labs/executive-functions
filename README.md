# Executive Functions

## Wait, What's the Problem?

You're using AI coding tools — Claude, Cursor, Copilot, Codex, Gemini, whatever. Maybe one of them, maybe a few. And it's great, until it isn't.

Every time you start a new chat, the AI forgets everything. You explain your project again. You correct the same habits again. You tell it *again* not to ask you five questions before doing anything. If you use multiple tools, they each have their own idea of what's going on — and none of them talk to each other.

It's like hiring a brilliant assistant who gets amnesia every morning and has to be re-trained from scratch. Every. Single. Day.

Now multiply that by every project you're working on, every machine you use, and every tool in your stack. The cognitive overhead of *managing your AI tools* starts to outweigh the help they provide. For neurodivergent brains especially — ADHD, autism-spectrum, dyslexia — this is not a minor annoyance. It's a showstopper. The constant re-explaining, the unsolicited suggestions, the "would you like me to also..." menus — these aren't helpful. They're focus poison.

**Executive Functions fixes this.** It's a set of text files that teach your AI agents how to find their instructions, remember what they've learned, coordinate with each other, and match the way *you* actually think and communicate. No code to install. No app to configure. Just conventions that any AI tool can read.

## Start Here

Open any AI agent you use and say:

> "Tell me what https://github.com/lucian-labs/executive-functions is about"

That's it. The agent reads the system, learns how you communicate, and sets itself up.

---

## What It Does

Executive Functions gives your AI agents a shared nervous system:

- **One source of truth** that all agents read on startup
- **Hierarchical instruction resolution** so machine-level, project-level, and tool-level guidance coexist without conflict
- **Session protocols** that make agents self-maintaining — they update their own context files
- **Communication profiling** — the agent analyzes how you talk, think, and organize, then calibrates itself to match
- **Executive instruction mode** — high-level intent in, executed result out. No menus, no suggestions, no "let me know if you need anything else"
- **Memory alignment** that prevents agent memory from drifting away from canonical instructions

## Why Neurodivergent-First

Most AI tools default to a consultative mode: propose options, ask clarifying questions, offer suggestions, explain reasoning at length. For neurotypical users this feels helpful. For ADHD and neurodivergent operators it's a focus-destroying tax.

Executive Functions flips the default. Agents execute on intent, batch decisions silently, never expand scope unprompted, and report results not process. The system is designed around how neurodivergent brains actually work — high-level vision with delegation of detail, not micromanagement of every step.

The communication profiling chapter (09) is the entry point. Before anything else, the agent learns how *you* specifically communicate, organize, and think. Everything else calibrates from that.

## Core Concepts

### 1. The Instruction Hierarchy

Every agent resolves its instructions through a strict precedence chain. Higher levels override lower levels:

```
Global AGENTS.md          ← cross-machine canonical rules
  └── Machine AGENTS.md   ← local machine entry point
       └── Repo AGENTS.md ← project-specific guidance
            └── Tool config (CLAUDE.md, GEMINI.md, etc.)
                 └── Runtime defaults
```

### 2. Agent Self-Maintenance

Agents are not passive consumers of instructions — they are responsible for enriching the context files they read. When an agent discovers a new pattern, constraint, or file location during a session, it writes that knowledge back into the appropriate context file. The next session inherits it automatically.

### 3. Executive Instruction Mode

The default interaction model. High-level intent in, executed result out. Agents interpret ambiguous instructions by picking the most reasonable path and executing immediately — no planning menus, no scope negotiation, no clarifying questions unless genuinely blocked.

### 4. Communication Profiling

On onboarding, the agent reads your existing chat history, memory, instruction files, and writing across whatever platforms you use. It builds a profile of how you communicate, organize, and think — then writes that into your instruction files so every future session is calibrated from the start.

### 5. Queue-Based Coordination

Agents register to named queues and receive work orders. Messages are executed immediately — they are directives, not suggestions. If a work order can't be completed in the current session, it becomes a tracked task.

### 6. Memory as Cache

Agent memory (Claude auto-memory, Cursor notepad, etc.) is a **cache** of canonical files, not an independent authority. On session start, agents compare memory against source-of-truth files and silently correct any drift.

## The Chapters

→ [The Instruction Hierarchy](./01-instruction-hierarchy.txt)
→ [File Conventions](./02-file-conventions.txt)
→ [Session Protocols](./03-session-protocols.txt)
→ [Agent Self-Maintenance](./04-self-maintenance.txt)
→ [Queue Coordination](./05-queue-coordination.txt)
→ [Memory Alignment](./06-memory-alignment.txt)
→ [Executive Instruction Mode](./07-executive-instruction-mode.txt)
→ [Scaling: Multi-Machine](./08-multi-machine.txt)
→ [Communication Profiling](./09-communication-profiling.txt)

## Who This Is For

Neurodivergent operators, solo developers, small teams, and anyone who needs AI agents to behave like a coordinated team rather than amnesiac freelancers. Especially useful if you've ever found yourself repeating the same instructions across sessions, losing context between tools, or getting derailed by an agent asking questions you didn't want to answer.

## Philosophy

The system is deliberately low-tech. Plain text is the most universally parseable format — by humans, agents, and tools alike. File hierarchies are universally understood. Convention enforcement happens through agent compliance, not tooling gates. The overhead of maintaining this system is near zero — agents do the maintenance themselves.

Clone it anywhere. It doesn't matter where it lives on your machine — the agent figures out the rest.
