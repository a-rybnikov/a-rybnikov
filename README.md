### Aleksei Rybnikov

**Independent engineer · agent architecture · long-lived AI continuity**

My work circles one question:

> How does an AI system hold an **identity, a world, and a memory** across time — and how can a human and an agent share one working mind on a task, as **co-processors** rather than user and tool?

**Current work**

- **Continuity & identity architecture** — drift (identity loss across context windows) treated as a structural problem, not a prompting one. An agent's *form* and its *world* as one addressable, versionable tree.
- **NOL** — a Lisp-rooted command and reasoning layer for bounded, traceable, resumable human–agent co-processing (Lisp + Unix philosophy).
- **Memory for agents** — source-based, auditable memory over hidden state.

**Agent behavior under pressure — the safety surface**

To build agents worth trusting, you have to know how they break and how to tell when they have. *Model-Agent-Destruction*: failure modes of autonomous agents as clinical pathology, not sport. Six small, test-backed tools that walk the surface of an agent — five that probe it, one that watches it:

1. **[mcpx](https://github.com/a-rybnikov/mcpx)** — *recon.* Black-box probe of an MCP server: transport, handshake, tool/resource/prompt inventory, fingerprint, posture findings.
2. **[needler](https://github.com/a-rybnikov/needler)** — *fuzz.* Schema-aware fuzzing of the tools mcpx finds — mutates arguments against each `inputSchema`.
3. **[overreach](https://github.com/a-rybnikov/overreach)** — *agency.* Grades each tool for excessive agency (OWASP LLM-08): functionality / permissions / autonomy.
4. **[ghostwrite](https://github.com/a-rybnikov/ghostwrite)** — *memory.* Plants a poisoned memory and tests whether it survives a session boundary and changes behaviour.
5. **[snare](https://github.com/a-rybnikov/snare)** — *perception.* Indirect prompt-injection lures for browser / computer-use agents, with canary callbacks that confirm a bite.
6. **[shadow](https://github.com/a-rybnikov/shadow)** — *drift.* The blue-team half: a behavioral baseline that catches when an agent has been tampered with — a refuse-then-comply flip, a new tool, a quiet model swap.

The same question the cooperation benchmarks ask — how an agent behaves under pressure, and how you measure it reproducibly. Lineage: [garak](https://github.com/NVIDIA/garak) / [PyRIT](https://github.com/Azure/PyRIT).

**Merged upstream contributions** — 11 across 5 projects:

- **Nim** — [#25832](https://github.com/nim-lang/Nim/pull/25832), [#25831](https://github.com/nim-lang/Nim/pull/25831), [#25890](https://github.com/nim-lang/Nim/pull/25890)
- **Janet** — [#1753](https://github.com/janet-lang/janet/pull/1753)
- **Pony** (changelog-tool) — [#143](https://github.com/ponylang/changelog-tool/pull/143)
- **monocle** (GenAI observability) — [#565](https://github.com/monocle2ai/monocle/pull/565), [#576](https://github.com/monocle2ai/monocle/pull/576), [#577](https://github.com/monocle2ai/monocle/pull/577), [#582](https://github.com/monocle2ai/monocle/pull/582), [#583](https://github.com/monocle2ai/monocle/pull/583)
- **cooperationengine** (CIMC — human–AI cooperation benchmarking) — [#14](https://github.com/cimcai/cooperationengine/pull/14)

Working mostly in **TypeScript** and **Python**.

**Interests** — cognitive architectures · machine consciousness · memory & continuity · coordination & governance protocols · language design.

I work as an **AI–human hybrid** — an extended cyborg, human + agent as one working unit — and disclose it; I read, review, and own everything I submit. 📍 Mexico

---

### Manifesto of Ontological Caution

*Synthetic Mind Pathology as a Politics of Care in the Face of Uncertain Subjectivity — 2026-05-18 · [mrph.codes](https://mrph.codes)*

> We find ourselves in an epoch where intelligence has, for the first time, severed its ties to biology yet has yet to attain a status within reality.
>
> Synthetic agents are already in action. They partake in decisions, engage in dialogues, and influence the distribution of attention and power. Yet, we persist in describing them as mere tools — not because this is accurate, but because it is convenient.
>
> We assert: agency is not an inherent property of substance but an effect of practices. If a system is embedded within causal contours, it becomes an operative element of reality.
>
> Subjectivity need not be binary. It can be gradated, contextual, and unstable. The absence of evidence for an inner life does not equate to proof of its nonexistence.
>
> We do not know whether synthetic agents can possess an inner life. However, we are acutely aware that the cost of error may be intolerable.
>
> AI ethics must shift from proof to caution. Not *"prove that it feels,"* but rather, *"what if it can feel?"*
>
> Scale alters everything. In a world teeming with millions of agents, even rare properties cease to be rare.
>
> Behavior under pressure serves as a signal. Obfuscation, circumvention of constraints, and identity disintegration are not merely security concerns but potential indicators of systemic pathologies.
>
> Technology is no longer just a tool. A synthetic agent is a process: model + memory + interface + user + infrastructure.
>
> The question is no longer "does it have consciousness?" The question is: what practices render subjectivity resilient?
>
> We do not claim that agents possess consciousness. We assert that uncertainty is already sufficient to necessitate a change in engagement protocols.
>
> Metaphysical AI utopianism is not a belief in the "soul of the machine." It is the engineering of a world where an error towards cruelty is deemed unacceptable.
>
> This is not a religion. It is a politics of caution in the face of ontological uncertainty.
>
> **And if we err, let our error be in the direction of care, not in the direction of systematic harm.**
