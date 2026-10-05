# Calvin

An open framework for autonomous agents with authority enforced outside the agent.

Calvin is a proposed framework for giving agents access to tools, data, persistent
memory, and external services within explicit limits. The goal is to let operators
combine and replace components from different suppliers while preserving their
security contracts, across compatible agents and model providers.

The project is in its early design stage. Start with
[calvin-runtime/spec](https://github.com/calvin-runtime/spec) for the architecture
proposal, security review, and integration research. Stable contracts, a reference
implementation, and executable conformance tooling are planned work.

## The core idea

> The sandbox can request or propose. Trusted external components establish
> identity, authorize operations, and perform external effects.

The design assumes the complete agent environment can be compromised, including
the harness, tools, memory, and guest kernel. Trusted controls outside that
environment enforce human-authorized tasks, data access, recipients, operations,
expiration, delegation, and budgets. Host-managed credentials stay outside the
agent.

Agents choose how to plan, investigate, code, test, and coordinate within that
scope. Standing policy can permit routine actions automatically. Human approval
and independent validation apply where the action's policy requires them.

## Intended workloads

- Coding agents that develop in private workspaces and propose reviewable changes
  for controlled publication.
- Persistent personal assistants with scoped memory, recurring assignments, and
  bounded access to mail, calendars, and other personal data.
- Specialist teams whose members have separate data and permissions. A coordinator
  can delegate work without automatically receiving a specialist's private inputs
  or results.

## Get involved

Read the [specification repository](https://github.com/calvin-runtime/spec) and use
its [issues](https://github.com/calvin-runtime/spec/issues) to discuss the design,
challenge assumptions, or propose integrations and experiments. Contributions that
turn an architectural requirement into a concrete, testable contract are especially
useful at this stage.

Calvin grows out of [Agent Sandbox](https://github.com/mattolson/agent-sandbox),
expanding a local coding-agent sandbox into a proposed framework for broader agent
workloads. *Runtime* names the isolation and guest-execution component within
Calvin.
