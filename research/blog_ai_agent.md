# Research Notes: What Is an AI Agent? (for Naver blog post)

- Date: 2026-10-24
- Purpose: Source material for the Naver blog post "AI 에이전트란?" (draft in `blog/ai_agent/`)

## 1. Definition

- IBM: an AI agent is "a system that autonomously performs tasks by designing workflows with available tools." Beyond language processing, agents make decisions, solve problems, interact with external environments and take actions. Agents "require goals and predefined rules defined by humans."
- Anthropic ("Building effective agents"): uses *agentic systems* as an umbrella term.
  - **Workflows**: LLMs and tools orchestrated through predefined code paths.
  - **Agents**: "LLMs dynamically direct their own processes" and tool usage, keeping control over how they accomplish a task.
- Common plain-language framing (Korean blogs, WikiDocs): a regular AI "answers when asked"; an agent "handles the job on its own" (plan → choose tools → execute → check result → retry).

## 2. How an agent works (IBM)

1. **Goal initialization and planning** – humans set goals and rules; the agent decomposes the goal into subtasks.
2. **Reasoning with tools** – fills information gaps with external datasets, web search, APIs, even other agents; re-evaluates and corrects its plan.
3. **Learning and reflection** – uses feedback from humans/other agents and stores what it learns.

Common four-part simplification of components: **LLM "brain" (reasoning/planning)**, **perception**, **tools**, **memory (short- and long-term)**, run in a perceive → plan → act loop until the goal is reached. This split is a simplification, not a standard.

## 3. Chatbot vs. workflow vs. agent

| | Chatbot | AI workflow | AI agent |
|---|---|---|---|
| Core behavior | Answers questions | Follows predefined steps | Decides next step toward a goal |
| Flexibility | Low | Low–medium | High |
| Predictability | High | High | Lower (needs verification) |
| Best for | Q&A, drafting | Repetitive, well-defined tasks | Open-ended, multi-step tasks |

Anthropic advice: start with the simplest solution; use workflows where predictability matters, agents for open-ended problems where the number of steps can't be predicted. Agents trade latency and cost for performance, and errors can compound.

## 4. Types of agents (IBM, simplest → most advanced)

1. Simple reflex (thermostat on a timer)
2. Model-based reflex (robot vacuum remembering cleaned areas)
3. Goal-based (navigation finding a route)
4. Utility-based (choosing the route that best balances time, cost, fuel)
5. Learning agents (personalized recommendations)

## 5. Adoption

- Gartner (press release, 2025-08-26): 40% of enterprise applications will feature task-specific AI agents by the end of 2026, up from less than 5% in 2025. Gartner's evolution path: embedded assistants → task-specific agents (2026) → multi-agent ecosystems (2029). Best case: agentic AI could drive ~30% of enterprise application software revenue by 2035 (over $450B).
- Market-size figures from vendor blogs vary widely; not used in the post.

## 6. Risks and limitations (IBM)

- Multi-agent dependencies and shared weaknesses of the same foundation model
- Infinite feedback loops (repeatedly calling the same tool)
- Computational cost and time
- Data privacy / security, given "experimental and often unpredictable behavior"
- Practical tip from Korean blogs: check permissions (read-only vs. modify/send/delete) and keep a human review step.

## 7. Naver top-post format analysis (search "AI 에이전트란", 2026-10-24)

Posts reviewed: diu_lab/224450263688, zomama/224447999477, lifeasset365/224449574222.

- Hero image + 2–3 line intro that restates the question
- Table of contents in a quotation block
- Numbered section titles (1., 2., 3. …), one image per section
- Comparison table or bullet list in a quotation block
- Concrete examples / analogies (recipe vs. chef, assistant vs. employee)
- "Wrap-up" section, then FAQ (Q/A)
- Length: ~2,000–3,300 characters, 4–14 images

## Sources

- IBM, "What are AI agents?" – https://www.ibm.com/think/topics/ai-agents
- IBM, "What are the components of AI agents?" – https://www.ibm.com/think/topics/components-of-ai-agents
- Anthropic, "Building effective agents" – https://www.anthropic.com/engineering/building-effective-agents
- Gartner press release (2025-08-26) – https://www.gartner.com/en/newsroom/press-releases/2025-08-26-gartner-predicts-40-percent-of-enterprise-apps-will-feature-task-specific-ai-agents-by-2026-up-from-less-than-5-percent-in-2025
- WikiDocs, "AI 에이전트 완전 이해" – https://wikidocs.net/338279
- Glean, "7 core components of an AI agent architecture" – https://www.glean.com/blog/7-core-components-of-an-ai-agent-architecture-explained
