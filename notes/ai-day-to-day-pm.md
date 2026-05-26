# Building a PM Operating System with AI

The shift for me was realizing AI is not a chatbot, it is an operating system for the product role. The biggest unlock came from **Garry Tan's gstack**. He is the President of Y Combinator, and his open-source toolkit has tens of thousands of GitHub stars. I installed it inside Claude Code and pulled key elements from it into my **CLAUDE.md** (a markdown file that loads automatically into every Claude session on my machine, so the operating system is universal across every project I touch). gstack also ships skills (slash commands) I can invoke when I want a specific process followed. The framework that ties it all together is a simple sprint:

**Think. Plan. Build. Eval. Ship. Reflect.**

## Think (user and use case discovery)

External research (market, competitors, customer signals) runs through ChatGPT Deep Search or Google Deep Search. Perplexity used to be my default but the others have caught up and I don't need three subscriptions. For internal context (docs, feedback, tickets, call transcripts) I use MCP connectors so the AI can read them directly. No manual copy-paste.

## Plan (stories and journey)

I convert research into personas, jobs-to-be-done, user stories, edge cases, and acceptance criteria using Claude. ChatPRD caps at three options and then paywalls, so Claude wins on cost and depth. For user journeys I moved from Whimsical to Mermaid. Flow diagrams, decision trees, and system flows from plain text. Version-controllable, no extra tool to pay for.

## Build (requirements and prototype)

Functional requirements live in Notion, surfaced into Claude through the Notion MCP. Prototypes used to mean Figma Make MCP, but Claude's built-in design panel covers most of what I need now. One less twenty-dollar subscription. For non-functional requirements (latency, reliability, privacy, scalability, concurrency, cost, observability, failover) I lean on Claude to force me to name them upfront instead of discovering them in production.

## Eval (review and test, merged)

Two halves, both essential.

**Quantitative**: golden test cases on every PR, probabilistic regression under varied conditions, replay testing on recorded inputs, fault injection for graceful recovery.

**Qualitative**: LLM-as-judge against a rubric for tone and accuracy, scenario-based simulations for multi-turn flows, human in the loop for things only humans catch (tone misses, looping behavior, awkward recovery).

Three layers, weekly cadence, cheap to start.

## Ship and Reflect

Execution runs through Asana, Linear, or Jira via MCP. AI flags blockers, drafts bug reports, notifies owners, and ties everything back to the PRD so the loop closes. Reflection is the step most people skip. I connect Claude to my observability stack through an MCP, then compare what I expected to happen against what actually happened. The delta becomes the input for the next Think cycle.

## Simple framing

AI is the operating layer across discovery, journey, requirements, prototype, evaluation, execution, and feedback. Tools change. The sprint doesn't.
