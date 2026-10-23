<div align="center">

<img src="./assets/zenera-hero-dark.svg#gh-dark-mode-only" alt="Zenera — Build intelligent AI agents" width="100%" />
<img src="./assets/zenera-hero-light.svg#gh-light-mode-only" alt="Zenera — Build intelligent AI agents" width="100%" />

### Self-improving multi-agent systems for real work.

Zenera builds **agentic AI** that designs, evaluates, and fine-tunes itself.
Describe the work, connect the knowledge and tools, and define what success
looks like. A **meta-agent** turns that intent into a team of specialized
agents, and a **recursive self-improvement loop** makes them better with every
run, backed by evals, execution traces, and human oversight.

The goal is not another general-purpose chatbot, but agent systems that fit a
domain, coordinate around a task, and improve through evidence.

**People define the purpose and boundaries. Agents help build, evaluate, and
refine the systems that do the work.**

`Agentic AI` · `Multi-Agent Orchestration` · `Meta-Agents` · `Recursive Self-Improvement` ·
`Agent Fine-Tuning` · `Context Engineering` · `Agentic RAG` · `Long-Term Memory` ·
`LLM-as-a-Judge` · `Eval-Driven Development` · `Prompt Optimization` · `Human-in-the-Loop`

[**About Zenera**](https://zenera.ai) · [**LinkedIn**](https://www.linkedin.com/company/zenera-ai) · [**YouTube**](https://www.youtube.com/@Zenera_AI)

</div>

---

## What Zenera does

Zenera is building a platform that turns a description of the work into a
working, continuously improving agent system. Each part of the platform
handles one piece of that lifecycle:

| Capability | What it means |
| :--- | :--- |
| **Agent Factory (meta-agent)** | Describe the job in plain language. A meta-agent generates the roles, prompts, skills, tool integrations, and orchestration strategy. |
| **Multi-agent orchestration** | Routing, handoffs, supervisor/worker patterns, and parallel execution, used only where they actually pay off. |
| **Context engineering & agentic RAG** | Retrieval over documents and API schemas, query planning, and context selection, so each agent gets the right context rather than simply more of it. |
| **Durable agent memory** | Long-term memory with explicit policies for what to store, reuse, and discard. |
| **Self-improvement engine** | Trace-driven optimization: failures and wasted steps become concrete, testable changes to prompts, skills, and memory. |
| **Agent fine-tuning** | Harness-level tuning against datasets and rubrics. Better behavior without retraining the model. |
| **Evals & observability** | LLM-as-a-judge rubrics, regression suites, and full trajectory inspection: tool calls, retrieval, tokens, latency, and cost. |
| **Governance & control** | Permissions, approval gates, and human-in-the-loop review wherever the work requires it. |

## What we focus on

- **Specialized agents and multi-agent systems.** Give each agent a clear
  responsibility, the right tools, and explicit boundaries. Use routing,
  handoffs, and parallel work where they help, rather than making every task
  a multi-agent problem.
- **Context engineering.** Bring together instructions, domain knowledge,
  retrieval-augmented generation (RAG), API schemas, tools, and durable memory.
  The challenge is providing the right context, not simply more context.
- **Meta-agents and agent engineering.** Let an agent turn intent into roles,
  prompts, skills, integrations, and an execution strategy, then help maintain
  that system as requirements change.
- **Evaluation-driven self-improvement.** Turn real tasks, execution traces,
  and feedback into testable changes. Measure correctness alongside token
  usage, latency, and unnecessary work.
- **Observable, human-directed autonomy.** Keep goals and constraints explicit,
  make decisions inspectable, and preserve review and approval where the work
  requires them.

## Recursive self-improvement, with receipts

<div align="center">

<img src="./assets/workflow-dark.svg#gh-dark-mode-only" alt="Iterative workflow: Specify → Generate → Run and inspect → Improve → return to the specification" width="100%" />
<img src="./assets/workflow-light.svg#gh-light-mode-only" alt="Iterative workflow: Specify → Generate → Run and inspect → Improve → return to the specification" width="100%" />

</div>

A useful agent system is not finished when it produces its first answer.
Our approach treats every run as evidence about how the system can improve:

1. **Specify** the job, source material, permissions, and success criteria.
2. **Generate.** A meta-agent assembles the specialists, instructions, skills,
   tools, and memory policies.
3. **Run and evaluate** representative tasks with **trajectory-level
   evaluation**: inspect what was retrieved, which tools ran, and what it
   cost, not just the final answer.
4. **Improve and re-test** through **reflective optimization** against
   explicit rubrics. Re-run earlier cases to catch regressions, and feed
   unresolved requirements back into the specification.

This is **recursive agent engineering**: agents help build, evaluate, and
refine other agents. The goal stays human-defined, and every improvement must
be demonstrated by evals rather than assumed.

### Agent fine-tuning: optimize the system, not just the prompt

In ZeneraNeo, **agent fine-tuning** means optimizing the harness around a
model: prompts, instructions, skills, and memory policies. It does **not**
update model weights, so it works with any model and any provider, and every
change stays readable and reversible.

The tuning loop:

- runs **dataset cases** against **rubrics**, scored by an LLM judge;
- **diagnoses failures and wasted work** from execution traces;
- **applies targeted changes** and runs the cases again;
- performs **memory ablation**, comparing runs with and without memory to
  check that stored knowledge helps rather than adds noise.

Read more about [specialized agent engineering](https://github.com/andreyryabov/ZeneraNeo/blob/main/docs/specialized-agents.md)
and [fine-tuning with datasets and rubrics](https://github.com/andreyryabov/ZeneraNeo/blob/main/docs/finetuning.md).

## Where it fits

Specialized, self-improving agents are most useful where work is repeatable,
knowledge-heavy, and needs to be checked:

- **Knowledge assistants** that answer from internal documentation and cite
  their sources.
- **Operations automation** across business APIs, with confirmation before any
  write action.
- **Research and analysis agents** that gather, compare, and summarize
  information under explicit quality rubrics.
- **Domain copilots** for support, sales, and internal teams, tuned on real
  cases from that domain.

## Exploring in the open

We explore this approach through **ZeneraNeo**, an open-source experimental
project for building specialized agent systems from a specification and the
knowledge a task depends on. It helps developers design, run, inspect, and
improve agents for real workflows.

ZeneraNeo is an experimental side project, **not the official Zenera AI
Platform**. It is a place to share ideas, test approaches, and learn in the open.

### ZeneraNeo packages

Core tools for creating and running agent projects:

<p align="center">
  <a href="https://www.npmjs.com/package/@zenera/cli">
    <picture>
      <source
        media="(prefers-color-scheme: dark)"
        srcset="./assets/card-cli-dark.svg"
      />
      <source
        media="(prefers-color-scheme: light)"
        srcset="./assets/card-cli-light.svg"
      />
      <img
        src="./assets/card-cli-light.svg"
        alt="Zenera CLI — Build and operate agent projects"
        width="49%"
      />
    </picture>
  </a>
  <a href="https://www.npmjs.com/package/@zenera/neo">
    <picture>
      <source
        media="(prefers-color-scheme: dark)"
        srcset="./assets/card-neo-dark.svg"
      />
      <source
        media="(prefers-color-scheme: light)"
        srcset="./assets/card-neo-light.svg"
      />
      <img
        src="./assets/card-neo-light.svg"
        alt="Zenera Neo — TypeScript runtime for agent systems"
        width="49%"
      />
    </picture>
  </a>
  <a href="https://www.npmjs.com/package/@zenera/rag">
    <picture>
      <source
        media="(prefers-color-scheme: dark)"
        srcset="./assets/card-rag-dark.svg"
      />
      <source
        media="(prefers-color-scheme: light)"
        srcset="./assets/card-rag-light.svg"
      />
      <img
        src="./assets/card-rag-light.svg"
        alt="Zenera RAG — Knowledge retrieval for documents and APIs"
        width="49%"
      />
    </picture>
  </a>
  <a href="https://www.npmjs.com/package/@zenera/faker">
    <picture>
      <source
        media="(prefers-color-scheme: dark)"
        srcset="./assets/card-faker-dark.svg"
      />
      <source
        media="(prefers-color-scheme: light)"
        srcset="./assets/card-faker-light.svg"
      />
      <img
        src="./assets/card-faker-light.svg"
        alt="Zenera Faker — Mock integrations and generated APIs"
        width="49%"
      />
    </picture>
  </a>
</p>

## Examples

| Example | What it does |
| :--- | :--- |
| [Documentation RAG](https://github.com/andreyryabov/ZeneraNeo/tree/main/examples/projects/01-docs-rag) | Answers questions about Hugging Face Transformers documentation and cites the source passages. |
| [API Integration](https://github.com/andreyryabov/ZeneraNeo/tree/main/examples/projects/02-api-integration) | Coordinates a meeting using mock mail and calendar APIs, with confirmation required before writes. |

Explore [ZeneraNeo on GitHub](https://github.com/zenera-ai/ZeneraNeo) and browse
the [worked examples](https://github.com/andreyryabov/ZeneraNeo/tree/main/examples)
to see the project in action.

## Our vocabulary

The field moves fast and its terms get stretched. Here is what we mean by ours:

- **Agentic AI:** systems that plan, use tools, and take multi-step actions
  toward a goal, rather than answering a single prompt.
- **Meta-agent:** an agent whose job is to design, configure, and maintain
  other agents.
- **Recursive agent engineering:** agents helping build, evaluate, and improve
  other agents, under human-defined goals.
- **Self-improvement:** measurable gains on evals from changes proposed by the
  system itself, verified before they are kept.
- **Agent fine-tuning:** optimizing prompts, skills, and memory policies
  against datasets and rubrics, without changing model weights.
- **Context engineering:** deciding what information an agent sees, when, and
  in what form.
- **Eval-driven development:** treating rubrics and regression suites as the
  definition of "better".

## Related ideas and research

These are useful perspectives on the wider field, not claims that ZeneraNeo
implements these particular methods:

- [Building effective agents](https://www.anthropic.com/research/building-effective-agents):
  composable agent workflows, orchestration, and evaluator-optimizer loops.
- [Context engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents):
  managing the information an agent needs across a long-running task.
- [Reflexion](https://arxiv.org/abs/2303.11366):
  using feedback and reflective memory without updating model weights.
- [GEPA](https://arxiv.org/abs/2507.19457):
  reflective prompt evolution guided by execution trajectories and evaluation.

---

<div align="center">

### Follow Zenera

**[Website](https://zenera.ai)** · **[ZeneraNeo on GitHub](https://github.com/zenera-ai/ZeneraNeo)** · **[LinkedIn](https://www.linkedin.com/company/zenera-ai)** · **[YouTube](https://www.youtube.com/@Zenera_AI)**

<sub>Specialize around the work. Improve through evidence. Keep people in control.</sub>

</div>
