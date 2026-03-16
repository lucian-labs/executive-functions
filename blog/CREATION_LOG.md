# Executive Functions — Creation Log

**Date:** 2026-03-16
**Session:** Single continuous chat, Elijah Lucian + Claude Opus 4.6
**Repo:** https://github.com/lucian-labs/executive-functions

---

## Genesis

**The spark:**
> "this is a chat to create an orchestration process for people to replicate my ground control and agentic process. we will create a public repo for it."

The idea: take the entire agentic orchestration system Elijah had built for himself — GroundControl, AGENTS.md hierarchy, queue coordination, memory alignment, session protocols — and extract the *pattern* into something anyone could use. Not the software. The thinking.

**First constraint, immediately:**
> "the entire thing is meant to be orchestrative, no code, no frameworks, no scripts"

This set the tone for everything that followed. The repo would contain only text. The orchestration is conceptual, not programmatic. Agents read conventions and comply — there's no enforcement layer.

---

## Key Decisions (Chronological)

### Format: Markdown → Plain Text
> "if markdown is too heavy for llms to parse, choose a more optimal text format"
> "it doesn't need to be read by a human"

The chapter files were originally .md. Elijah flagged that markdown syntax (tables, fences, bold markers) burns tokens without adding semantic value for LLMs. All chapters converted to .txt with compressed prose. README stayed .md for GitHub rendering — the one file humans actually see first.

**Decision:** README.md for humans, .txt for agents. Two audiences, two formats.

### Communication Profiling as Core Feature
> "the ai should help the user determine their own communication styles, and part of the onboarding of this project is a deep analysis on the users chats and interactions, gathering context on how they communicate and self organize"

This elevated the system from "agent instruction management" to something more personal — a system that *learns the operator* before doing anything else. The agent mines existing chat history, memory, commit messages, and writing samples to build a communication profile.

> ".claude/projects, .codex/projects, etc. but don't give hard paths, just let the llms figure it out"

No hardcoded paths. The agent discovers its own platform's storage. This was a deliberate anti-pattern rejection — most tools over-specify paths and break on different setups.

### Neurodivergent-First Design
> "the target demographic is adhd and neurodiverse"
> "it shouldn't matter where a user installs this repo"

Two constraints in one message. The system had to be:
1. Designed around ADHD/neurodivergent cognition, not adapted for it as an afterthought
2. Location-independent — clone anywhere, agent figures out the rest

This reframed the entire README. The "Why Neurodivergent-First" section emerged directly from this moment.

### The One-Prompt Onboarding
> "top thing in the readme, is tell your LLM to 'look at [this repo] and tell me what it is in my own words'"

Then refined to:
> 'also the "start here" should literally say: "tell me what https://github.com/lucian-labs/executive-functions is about"'

The entire onboarding collapsed to a single sentence you paste into any AI tool. No clone step. No install. No reading. Just: ask the agent. The agent does the rest.

**This is the thesis of the project in miniature:** the agent carries the cognitive load.

### Repo Organization: Personal → Org
Moved from `ELI7VH/executive-functions` to `lucian-labs/executive-functions`. The project is a Lucian Labs offering, not a personal repo.

---

## Quotes (Direct, Unedited)

> "the entire thing is meant to be orchestrative, no code, no frameworks, no scripts"

> "if markdown is too heavy for llms to parse, choose a more optimal text format"

> "it doesn't need to be read by a human"

> "the ai should help the user determine their own communication styles, and part of the onboarding of this project is a deep analysis on the users chats and interactions, gathering context on how they communicate and self organize"

> "don't give hard paths, just let the llms figure it out"

> "the target demographic is adhd and neurodiverse"

> "it shouldn't matter where a user installs this repo"

> "top thing in the readme, is tell your LLM to 'look at [this repo] and tell me what it is in my own words'"

---

## Concepts Coined / Named During Session

- **"Focus poison"** — the effect of consultative AI defaults on neurodivergent users (unsolicited suggestions, clarifying questions, scope expansion)
- **"Amnesiac freelancers"** — what AI agents behave like without orchestration
- **"Memory as cache"** — agent memory is a cache of canonical files, not an independent authority
- **"Executive instruction mode"** — high-level intent in, executed result out; agents interpret and execute without negotiation
- **"Convention-over-configuration"** — the system is enforced by agent compliance with text conventions, not by tooling or code
- **"The agent carries the cognitive load"** — the design principle behind one-prompt onboarding and neurodivergent-first design

---

## Architecture (What Shipped)

9 files, ~490 lines total:

| File | Purpose |
|------|---------|
| README.md | Human-facing landing page, problem framing, one-prompt onboarding |
| 01-instruction-hierarchy.txt | Precedence chain for agent instructions |
| 02-file-conventions.txt | What files exist, where they go, what goes in them |
| 03-session-protocols.txt | Start/during/end session behavior |
| 04-self-maintenance.txt | Agents update their own instruction files |
| 05-queue-coordination.txt | Async work passing between agents |
| 06-memory-alignment.txt | Memory drift prevention |
| 07-executive-instruction-mode.txt | How agents interpret instructions |
| 08-multi-machine.txt | Scaling across machines |
| 09-communication-profiling.txt | Agent learns the operator's style on onboarding |

---

## Timeline

| Time | Event |
|------|-------|
| Session start | Concept stated, repo created as private on GitHub (ELI7VH) |
| +2 min | Registered to executive-functions scheduled task queue |
| +3 min | Cloned, read all source material (AGENTS.md, AGENT_STACK.md, lucian-utils/AGENTS.md) |
| +8 min | README.md + 8 chapter files scaffolded in markdown |
| +10 min | Format pivot: chapters converted from .md to .txt, markdown syntax stripped |
| +12 min | Chapter 09 (Communication Profiling) added — agent-led onboarding analysis |
| +14 min | README rewritten: neurodivergent-first framing, problem explanation for newcomers |
| +16 min | Start Here simplified to single prompt with repo URL |
| +18 min | Repo transferred to lucian-labs org, URLs updated |
| +20 min | User testing collection discussed (agent-captured moments approach) |
| +22 min | Creation log compiled |

---

## Blog Hooks

**Headline options:**
- "I Built an Operating System for AI Agents — and It's Just Text Files"
- "Executive Functions: Teaching AI Agents to Stop Forgetting Everything"
- "Why Your AI Tools Need a Nervous System (and How to Give Them One)"
- "The ADHD-First Approach to AI Agent Management"

**Narrative arc:**
The session itself demonstrates the product. Elijah gave high-level executive instructions ("create a public repo for this," "make it neurodivergent-first," "the start here should literally say...") and the agent executed without asking clarifying questions, expanding scope, or proposing alternatives. The repo was created, scaffolded, rewritten, reformatted, reorganized, and published in a single continuous session. The process *was* the product.

**Key tension:**
The system has no enforcement mechanism. It works because LLMs are compliant readers — they follow instructions in text files. The entire architecture is a bet on convention over code. If agents stop reading their instruction files, the system breaks. But so does every other approach — the question is just where you put the trust.

**The one-liner:**
Clone it anywhere, paste one prompt into any AI tool, and the agent sets itself up. That's the whole install process. Everything else is the agent's job.
