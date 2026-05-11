<!--
  GitHub Profile README for: AgentLayer (org)
  Place this file at: .github/profile/README.md  (in repo: AgentLayer1/.github)
  Ordering mirrors agentlayer.one (home, platform, /dev)
-->

<div align="center">

<br/>

# AgentLayer

### The platform agents run on.

<p>
  <samp>Industries built for agents. Forward-deployed engineering.</samp>
</p>

<br/>

<a href="https://agentlayer.one"><img alt="agentlayer.one" src="https://img.shields.io/badge/website-agentlayer.one-0a0a0b?style=for-the-badge&labelColor=2a2a2a" /></a>
<a href="https://studio.agentlayer.one"><img alt="studio (live)" src="https://img.shields.io/badge/studio-live%20demo-c6f432?style=for-the-badge&labelColor=2a2a2a" /></a>
<a href="https://agentlayer.one/dev"><img alt="developers" src="https://img.shields.io/badge/developers-%40agentlayer%2F%2A-2a2a2a?style=for-the-badge&labelColor=2a2a2a" /></a>
<a href="mailto:contact@agentlayer.one"><img alt="contact" src="https://img.shields.io/badge/contact-contact%40agentlayer.one-2a2a2a?style=for-the-badge&labelColor=2a2a2a" /></a>

<br/>
<br/>

</div>

> Frontier models are already smart. The interesting problem is making agents safe, auditable, and useful inside organizations that have rules, regulators, and customers.

---

## 🧭 About

**AgentLayer** is a platform company building the enterprise AI Agent Orchestration Platform for industries that were never built for the agentic world. One product, one engagement model, one recurring monthly contract. Forward-deployed engineering is in the price.

---

## ⚙️ The Engine

The foundational layer. Six platform-core capabilities, productized as the engine every deployment runs on.

| Capability | What it does |
|---|---|
| 🧠 **Orchestration** | Agent loop, tool dispatch, multi-step planning, lifecycle and state handoff |
| 🔐 **Identity & Access** | Principal-vs-agent action delegation, KYA (Know-Your-Agent), credential scoping |
| 📜 **Compliance & Audit** | Append-only action logs, attribution, replay, citations on retrieval, regulator-aware |
| 🔁 **Workflow** | Stateful multi-step workflows, human-in-the-loop checkpoints, approval routing |
| 🔭 **Observability** | Heartbeat health, task lineage, session state, agent-action traceability |
| 🛡️ **Governance** | Policy framework, sovereignty controls, jurisdictional grounding |

---

## 🧩 Agentic Primitives

The enabling layer. The **`@agentlayer/*`** packages are open-source primitives extracted from production. Each one is a focused pattern proven against real regulated-industry workloads, then absorbed into the engine that powers every AgentLayer deployment. Engineering teams can engage these primitives directly. No contract, no signup, just code.

| Package | Pattern | Status |
|---|---|---|
| **`@agentlayer/orchestration`** | Agent loop, tool dispatch, planning, lifecycle, state handoff | 🛠️ In preparation |
| **`@agentlayer/identity`** | Principal-vs-agent delegation, KYA, scoped credentials | 🛠️ In preparation |
| **`@agentlayer/audit`** | Append-only logs, attribution, replay, citations | 🛠️ In preparation |
| **`@agentlayer/observability`** | Heartbeat health, task lineage, session state, traceability | 🛠️ In preparation |
| **`@agentlayer/agent-kevin`** | Canonical internal-team-agents reference. Knowledge pipeline, task orchestration, autonomous heartbeat, plugin dispatch | 🟢 In production. OSS Q3–Q4 2026 |
| **`@agentlayer/studio`** | The operator surface. Activity feed, agents, tasks, timeline, audit, approvals | 🟡 Live prototype. Closed commercial |

<div align="center"><sub>Closed patterns stay proprietary. Open primitives compose.</sub></div>

---

## 🚀 Deployment Patterns

Every customer engagement deploys across one or more of these orthogonal surfaces. All supervised through **AgentLayer Studio**.

<table>
<tr>
<td width="33%" valign="top">

### 🧑‍💻 Internal-team agents
Engineering, ops, finance, back-office teams operating at AI multiples. The `@agentlayer/agent-kevin` pattern, configured for the customer's organization.

</td>
<td width="33%" valign="top">

### 📞 Customer-facing agents
Support, onboarding, account management. Audit-trailed, human-in-the-loop on consequential decisions.

</td>
<td width="33%" valign="top">

### 🤝 Agent-as-customer
Autonomous agents transacting with the business. AgentPay is the leading instance, on a regulated payments rail.

</td>
</tr>
</table>

---

## 🏭 Industry Modules

The application layer. Each module is a deployable, industry-tuned configuration on the same engine. Customer-facing brand, structurally the same platform.

| Module | Brand | Industry | Status |
|---|---|---|---|
| `agent-fintech` | 💸 **AgentPay** | Payments, financial operations, fintech | 🟡 In progress |
| `agent-gov` | 🏛️ **AgentGov** | Government, public-sector, RFP response | Engagement open |
| `agent-edu` | 🎓 **AgentEdu** | Education ops, registrar, admissions, student services | Engagement open |
| `agent-health` | 🩺 **AgentHealth** | Healthcare operations, clinician-augmenting | Engagement open |
| `agent-legal` | ⚖️ **AgentLegal** | Legal work, citation-disciplined, lawyer-augmenting | Engagement open |
| `agent-stay` | 🏨 **AgentStay** | Hospitality operations, operator-augmenting | Engagement open |

---

## 🎛️ AgentLayer Studio

> **The operator surface of the platform. Live today.**
> [studio.agentlayer.one](https://studio.agentlayer.one)

One screen showing every agent in the organization. What they're doing, what's queued for human review, what's complete, how they hand work to one another. The control plane for non-engineers: operators, executives, ops leads, supervisors.

<sub>Activity feed · Agents · Kanban + List · Timeline · Audit trail · Approvals queue · Notifications · Light and dark themes · Multi-tenant context · Real-time streaming</sub>

Studio is shipped under the same Enterprise Platform Contract. The way the AWS Console is part of AWS.

---

## ⚒️ Stack

```ts
type AgentLayerStack = {
  models:     ['Claude (Anthropic) · default', 'GPT, Gemini · fallback'];
  runtime:    ['Bun + TypeScript', 'LangGraph', 'Anthropic Agent SDK'];
  agents:     ['Tool use', 'Planners + routers', 'Sub-agent orchestration', 'Memory: short/episodic/semantic'];
  retrieval:  ['Hybrid (BM25 + dense)', 'pgvector', 're-ranking', 'citation-aware'];
  evals:      ['Golden sets', 'LLM-as-judge', 'trace diffing', 'cost + latency budgets'];
  data:       ['PostgreSQL', 'Redis'];
  cloud:      ['AWS', 'Kubernetes', 'multi-region'];
  frontend:   ['Next.js 16', 'React 19', 'Tailwind CSS 4', '@agentlayer/ui'];
  payments:   ['x402', 'ERC-8183', 'ERC-8004', 'EIP-7702', 'Polygon · Arbitrum'];
};
```

---

## 🧱 Engineering Principles

- **Orchestration over framework.** Patterns that compose with the language and tooling teams already use. No lock-in.
- **Audit trail by default.** Every agent action attributable, replayable, reviewable.
- **Observability first.** Heartbeat health, task lineage, session state. All surfaced.
- **Human-in-the-loop is a feature.** Designed-in approval points, not bolted-on guardrails. A core capability, not a fallback.
- **Autonomy is earned, not assumed.** Agents prove themselves through evals before they earn longer leashes.

---

## 🛰️ Connect

<table>
<tr>
<td>🔗 <strong>Website</strong></td>
<td><a href="https://agentlayer.one">agentlayer.one</a></td>
</tr>
<tr>
<td>🎛️ <strong>Studio (live)</strong></td>
<td><a href="https://studio.agentlayer.one">studio.agentlayer.one</a></td>
</tr>
<tr>
<td>🛠️ <strong>Developers</strong></td>
<td><a href="https://agentlayer.one/dev">agentlayer.one/dev</a></td>
</tr>
<tr>
<td>🏢 <strong>Engage</strong></td>
<td><a href="https://agentlayer.one/engage">agentlayer.one/engage</a></td>
</tr>
<tr>
<td>💬 <strong>Contact</strong></td>
<td><a href="mailto:contact@agentlayer.one">contact@agentlayer.one</a></td>
</tr>
</table>

---

<div align="center">

<sub>Design agents. Govern agents. Trust agents.</sub>

<br/>
<br/>

<sub>© AgentLayer</sub>

</div>
