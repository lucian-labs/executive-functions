# Executive Functions

## Wait, What's the Problem?

You're using AI coding tools — Claude, Cursor, Copilot, Codex, Gemini, whatever. Maybe one of them, maybe a few. And it's great, until it isn't.

Every time you start a new chat, the AI forgets everything. You explain your project again. You correct the same habits again. You tell it *again* not to ask you five questions before doing anything. If you use multiple tools, they each have their own idea of what's going on — and none of them talk to each other.

It's like hiring a brilliant assistant who gets amnesia every morning and has to be re-trained from scratch. Every. Single. Day.

Now multiply that by every project you're working on, every machine you use, and every tool in your stack. The cognitive overhead of *managing your AI tools* starts to outweigh the help they provide. For neurodivergent brains especially — ADHD, autism-spectrum, dyslexia — this is not a minor annoyance. It's a showstopper. The constant re-explaining, the unsolicited suggestions, the "would you like me to also..." menus — these aren't helpful. They're focus poison.

**Executive Functions fixes this.** It translates how you work — your communication style, your decision-making patterns, how you give instructions, what derails you, what you need from an assistant — into a portable model that any AI tool can read. You build the model once. Every agent follows it. No more re-training.

## Start Here

Open whatever AI tool you already use and say:

> "Read https://github.com/lucian-labs/executive-functions and help me understand how to set it up."

Your agent will walk you through the chapters and help you create your first files. You'll make the decisions — the repo gives you the model.

---

## What You Get

- **Your agents know how you work.** You define your communication style, decision posture, pacing, correction patterns, and accessibility needs. Every agent reads this profile and calibrates to it.
- **Your agents stop acting like strangers.** Instead of defaulting to generic chatbot behavior, they match *your* way of working — from the first message of every session.
- **Your agents stop forgetting.** Your operator model lives in text files that persist across sessions, tools, and machines. No more re-explaining.
- **Your agents maintain the model themselves.** When you correct an agent or it discovers something new about your workflow, it updates the files. The model gets sharper over time.
- **Your agents stay in sync.** If a tool's memory drifts from your files, it self-corrects on startup. Your files are always the authority.
- **Your agents can hand work to each other.** Optional queue system for passing tasks between tools and machines.

## The Core Idea

Executive Functions is an operator-modeling system. The primary payload is *you* — how you think, communicate, prioritize, delegate, and correct. Everything else in the repo exists to carry that model and keep it consistent.

The system has three layers:

**1. Your operator model** — This is the core. A profile of how you work: communication preferences, interaction style, cognitive patterns, how you organize, what you need from an assistant. You build this first. It's the thing every agent reads to stop being generic. → [Building your operator profile](./09-communication-profiling.txt)

**2. A portable instruction surface** — Your model gets stored in a chain of text files (AGENTS.md) that any AI tool can read. Global rules in one file, machine-specific context in another, project details in a third. The files are the transport layer — they carry your model across tools, repos, and machines.

**3. Persistence infrastructure** — Session protocols, self-maintenance, memory alignment, and optional queues keep the model alive and accurate over time. Agents update their own files, correct their own memory, and hand work to each other. This is the machinery that prevents decay.

## Why Neurodivergent-First

Most AI tools default to a consultative mode: propose options, ask clarifying questions, offer suggestions, explain reasoning at length. For neurotypical users this feels helpful. For ADHD and neurodivergent brains it's a focus-destroying tax.

Executive Functions flips the default. Your operator model encodes exactly how you want to be interacted with — and agents follow it without being reminded. The system is designed around how neurodivergent brains actually work: high-level vision with delegation of detail, not micromanagement of every step.

## The Chapters

Start with your operator profile. Everything else serves it.

→ [Building your operator profile](./09-communication-profiling.txt) — **start here**
→ [Setting up the file chain](./01-instruction-hierarchy.txt) — how to store and distribute your model
→ [What files to create and where](./02-file-conventions.txt) — the transport layer
→ [What your agent does at start/end of each session](./03-session-protocols.txt) — keeping the model active
→ [How agents keep their own files up to date](./04-self-maintenance.txt) — the model improves over time
→ [Keeping agent memory in sync with your files](./06-memory-alignment.txt) — preventing drift
→ [Configuring how agents respond to you](./07-executive-instruction-mode.txt) — applying the model to interaction style
→ [Passing work between agents (optional)](./05-queue-coordination.txt) — multi-agent coordination
→ [Working across multiple machines (optional)](./08-multi-machine.txt) — carrying the model everywhere

## Who This Is For

You, if you've ever:
- Repeated the same instructions to an AI tool across multiple sessions
- Lost context switching between AI tools
- Gotten derailed by an agent asking questions you didn't want to answer
- Wished your AI assistant would just *remember*

Neurodivergent operators, solo devs, small teams, anyone tired of managing their AI tools instead of being helped by them.

## Philosophy

Plain text. No code, no frameworks, no dependencies. Text files are readable by every AI tool on every platform. Your agents enforce the conventions by reading them — there's no software layer. The overhead is near zero because the agents maintain the system themselves.

Clone it anywhere. It doesn't matter where it lives on your machine.
