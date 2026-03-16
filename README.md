# Executive Functions

## Wait, What's the Problem?

You're using AI coding tools — Claude, Cursor, Copilot, Codex, Gemini, whatever. Maybe one of them, maybe a few. And it's great, until it isn't.

Every time you start a new chat, the AI forgets everything. You explain your project again. You correct the same habits again. You tell it *again* not to ask you five questions before doing anything. If you use multiple tools, they each have their own idea of what's going on — and none of them talk to each other.

It's like hiring a brilliant assistant who gets amnesia every morning and has to be re-trained from scratch. Every. Single. Day.

Now multiply that by every project you're working on, every machine you use, and every tool in your stack. The cognitive overhead of *managing your AI tools* starts to outweigh the help they provide. For neurodivergent brains especially — ADHD, autism-spectrum, dyslexia — this is not a minor annoyance. It's a showstopper. The constant re-explaining, the unsolicited suggestions, the "would you like me to also..." menus — these aren't helpful. They're focus poison.

**Executive Functions fixes this.** It's a set of text files that teach your AI agents how to find their instructions, remember what they've learned, coordinate with each other, and match the way *you* actually think and communicate. No code to install. No app to configure. Just conventions that any AI tool can read.

## Start Here

Open whatever AI tool you already use and say:

> "Read https://github.com/lucian-labs/executive-functions and help me understand how to set it up."

Your agent will walk you through the chapters and help you create your first files. You'll make the decisions — the repo gives you the model.

---

## What You Get

- **Your agents stop forgetting.** You write your preferences and rules once, in text files. Every agent reads them on startup. No more re-explaining.
- **Your agents match how you communicate.** You describe your preferences — or optionally let the agent help you figure them out — and it calibrates to your style.
- **Your agents stop asking unnecessary questions.** You define how you want to be interacted with. Terse? Detailed? No suggestions? No closing offers? You set it once and it sticks.
- **Your agents maintain their own context.** When an agent discovers something new during a session, it updates its own instruction files. Next session starts smarter.
- **Your agents stay in sync.** If a tool's memory drifts from your files, it self-corrects on startup. Your files are always the authority.
- **Your agents can hand work to each other.** Optional queue system for passing tasks between tools and machines.

## Why Neurodivergent-First

Most AI tools default to a consultative mode: propose options, ask clarifying questions, offer suggestions, explain reasoning at length. For neurotypical users this feels helpful. For ADHD and neurodivergent brains it's a focus-destroying tax.

Executive Functions flips the default. You tell your agents exactly how to interact with you — and they do it, every session, without being reminded. The system is designed around how neurodivergent brains actually work: high-level vision with delegation of detail, not micromanagement of every step.

## How It Works

You're going to create a small chain of text files. That's the whole system.

**Step 1:** Create one master file (AGENTS.md) in a repo. This holds your rules, preferences, and communication style. Every agent reads it.

**Step 2:** Create a pointer file (~/ AGENTS.md) on your machine that says "the master file is over here." This also describes your local setup — what OS you're on, what tools are installed, where your repos live.

**Step 3:** Optionally, add project-specific files to individual repos for build commands, architecture notes, and project-level rules.

That's the core. The chapters below walk you through each piece:

→ [Setting up the file chain](./01-instruction-hierarchy.txt)
→ [What files to create and where](./02-file-conventions.txt)
→ [What your agent does at start/end of each session](./03-session-protocols.txt)
→ [How agents keep their own files up to date](./04-self-maintenance.txt)
→ [Passing work between agents (optional)](./05-queue-coordination.txt)
→ [Keeping agent memory in sync with your files](./06-memory-alignment.txt)
→ [Configuring how agents respond to you](./07-executive-instruction-mode.txt)
→ [Working across multiple machines (optional)](./08-multi-machine.txt)
→ [Getting your agent to learn your communication style](./09-communication-profiling.txt)

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
