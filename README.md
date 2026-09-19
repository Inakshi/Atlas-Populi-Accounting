# Atlas Populi Accounting

## Purpose and scope

This repository brings together the operating knowledge of the Finance department of Atlas Populi (Private) Limited. It contains the business and department context, policies, standard operating procedures (SOPs), work instructions, and agent roles needed to perform finance work consistently.

It is designed for use by both people and AI agents. Keeping these instructions in one maintained repository allows the department to use different AI tools while retaining the same business rules, procedures, and responsibilities.

Its initial scope covers supplier invoices and payments, bank reconciliation, prepayments, and project and cost-code allocation. The structure can expand as further finance activities are documented.

## Where to start

The onboarding instructions below describe the agreed setup. Start with `AGENTS.md`; `CLAUDE.md` directs Claude to the same maintained instructions.

Before creating or updating a policy, SOP, or skill, read the [Documentation Framework](documentation-framework.md). It defines the required structures, drafting rules, information boundaries, review checks, and approval route.

**For people:** Use the repository structure below to find the information relevant to your work. Start with `context/` when unfamiliar with the business or department, then consult the relevant policies, SOPs, and work instructions.

**For AI agents:** Start with `AGENTS.md` and follow its onboarding instructions. Before beginning work, read the business and department context in `context/` to understand the organisation, its objectives, systems, and responsibilities. Then read the policies, SOPs, work instructions, and agent role relevant to your task. `CLAUDE.md` directs Claude to the same entry point.

Each delegated agent also needs the core business and department context. Do not assume it inherits everything the orchestrator knows.

## Intended repository structure

Directory names use lowercase with hyphens between words. Standard entry filenames remain `README.md`, `AGENTS.md`, and `CLAUDE.md`.

| Location | Purpose |
|---|---|
| `README.md` | Repository purpose, scope, onboarding, and navigation: what the repository covers, where to start, and where to find or update each type of information. |
| `documentation-framework.md` | Company-wide framework for writing and maintaining policies, SOPs, and skills. |
| `AGENTS.md` | Entry and onboarding instructions for any AI agent: read the core business and department context before beginning work, then find the relevant policies, SOPs, and skills and follow the common rules for carrying out work. Detailed role responsibilities belong in `agent-team/`. |
| `CLAUDE.md` | Entry file for Claude. It should contain only “Refer to AGENTS.md.” so both tools use the same maintained instructions. |
| `context/` | Business and department background: what the organisation and department do, their objectives, the systems they use, and their key relationships and responsibilities. This gives readers the background needed to understand the policies and work. |
| `policies/` | Policies: the rules that govern decisions and actions, why those rules are required, who has authority to approve actions, and which controls must be followed. Step-by-step workflows belong in processes; detailed task instructions belong in skills. |
| `processes/` | Standard operating procedures (SOPs): what needs to be done, why it is done, who is responsible, and the sequence of steps and handoffs. Detailed instructions for performing individual tasks belong in skills. |
| `skills/` | Work instructions: how to perform a specific task, including the inputs and tools needed, detailed steps, expected output, and checks that confirm it was completed correctly. Supporting templates, examples, and scripts stay with the skill that uses them. |
| `agent-team/` | Agent roles and responsibilities: what each agent is accountable for, the work it can undertake within its authority, what it receives and delivers, and how it coordinates with other agents or hands work to a person. Includes the orchestrator and any supporting roles. |
