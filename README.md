# Repository structure

Directory names use lowercase with hyphens between words. Standard entry filenames remain `README.md`, `AGENTS.md`, and `CLAUDE.md`.

| Location | Purpose |
|---|---|
| `README.md` | Repository structure and navigation: the agreed categories, what belongs in each one, and where to find or update that information. |
| `AGENTS.md` | Entry instructions for any AI agent: what to read first, how to find the relevant policies, SOPs, and skills, and the common rules for carrying out work. Detailed role responsibilities belong in `agent-team/`. |
| `CLAUDE.md` | Entry file for Claude. It should contain only “Refer to AGENTS.md.” so both tools use the same maintained instructions. |
| `context/` | Business and department background: what the organisation and department do, their objectives, the systems they use, and their key relationships and responsibilities. This gives readers the background needed to understand the policies and work. |
| `policies/` | Policies: the rules that govern decisions and actions, why those rules are required, who has authority to approve actions, and which controls must be followed. Step-by-step workflows belong in processes; detailed task instructions belong in skills. |
| `processes/` | Standard operating procedures (SOPs): what needs to be done, why it is done, who is responsible, and the sequence of steps and handoffs. Detailed instructions for performing individual tasks belong in skills. |
| `skills/` | Work instructions: how to perform a specific task, including the inputs and tools needed, detailed steps, expected output, and checks that confirm it was completed correctly. Supporting templates, examples, and scripts stay with the skill that uses them. |
| `agent-team/` | Agent roles and responsibilities: what each agent is accountable for, the work it can undertake within its authority, what it receives and delivers, and how it coordinates with other agents or hands work to a person. Includes the orchestrator and any supporting roles. |
