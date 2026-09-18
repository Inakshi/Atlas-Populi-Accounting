# Documentation Framework

Writing and maintaining policies, SOPs, and skills.

## Objective

Use this framework across departments to create and maintain documentation that people and AI agents can follow consistently. Each document must make the purpose, responsibilities, decision boundaries, and evidence of success clear. Document the agreed, improved way of working; resolve known flaws and open design questions with the responsible owner before pushing a complete candidate for PR review.

Choose the document type and location, use its required structure, apply the drafting and information rules, then complete review and publication. Process-specific instructions and controls belong in the relevant document.

## Document Types, Names, and Locations

| Type and purpose | Markdown title (`#`) | Path from repository root |
|---|---|---|
| **Policy:** rules, principles, and decision authority. | `Policy / <Policy name>` | `policies/<policy-name>.md` |
| **Process/SOP:** the business workflow from trigger to verified outcome. These are one document type. | `SOP / <Area> / <Process name>` | `processes/<area-folder>/<process-name>.md` |
| **Skill:** how to perform one reusable task or tool operation. | `Skill / <Area> / <Skill name>` | `skills/<area-folder>/<skill-name>/SKILL.md` |

Use the exact area names in the repository's authoritative company or department context; maintain no separate list here. The repository's `AGENTS.md` must identify that context and the designated systems of record. If these are unspecified, confirm them with the responsible owner rather than inventing them. Derive area folders by removing parenthetical abbreviations, trimming spaces, converting to lowercase, and replacing spaces with hyphens. For example, `Customer Support` becomes `customer-support`.

Use short, descriptive lowercase names with hyphens for files and folders, except the required filename `SKILL.md`. Keep names stable; Git records versions, so omit dates, version numbers, `final`, and `latest`. For a cross-area SOP or skill, confirm one owning area and describe other areas' roles in the SOP. Link to the authoritative document instead of duplicating it.

## Required Structures

Use the applicable headings below in the stated order. Retain a heading that does not apply and briefly explain why. Use subheadings only when helpful.

Start with the title and accountable owner; add an effective date only when implementation timing requires it. Git history records versions, and the PR records approval. Do not add a document status field or separate change log. For skills, YAML metadata precedes this document header.

### Policy

| Heading | Required content |
|---|---|
| Purpose and scope | Why the policy exists, its intended outcome, who and what it covers, and exclusions. |
| Principles and rules | Explicit requirements, their conditions and boundaries, and the reasons for significant rules. |
| Responsibilities and authority | Who must follow the policy and who can decide or approve under it. |
| Exceptions | Permitted departures, approval authority, and required records. State if none are permitted. |
| Review and ownership | The maintaining role and review triggers. Include an interval only if agreed. |
| Related documents | Relevant policies, SOPs, skills, and authoritative references, with their purpose where needed. |

### Process/SOP

Keep business logic and responsibilities in the SOP; link to skills at the steps that need detailed tool instructions. Add a flowchart or responsibility matrix only when it materially improves understanding.

| Heading | Required content |
|---|---|
| Purpose, outcome, and scope | Why the process exists, what it delivers and to whom, its start and end, and exclusions. |
| Trigger and prerequisites | Trigger, inputs, systems, access, authority, and authoritative sources. For recurring work, identify the current task, relevant prior outcomes, carried-forward items, and incomplete runs to check against live state. |
| Process steps and decisions | Ordered actions, responsible roles, decision conditions, checks, dependencies, expected results, and handoffs. State the scope and duration of approvals where required. |
| Exceptions and escalation | General exception conditions, recovery, stopping points, decision authority, and how to resume. Explain how to verify uncertain outcomes before retrying to avoid duplicate actions. For unavailable access or missing, conflicting, or changed evidence, identify blocked work, any independent work that can continue, and a reporting route, including when the task system is unavailable. |
| Completion and handover | Evidence of completion, required review and approval, record destinations, and outstanding work. Specify which unresolved conditions block completion and who can accept exceptions. Apply the completion-record requirements below. |
| Related policies and skills | Governing policies, supporting skills, applicable agent instructions, and other necessary references. |

For recurring work, define a compact completion record: scope and outcome, procedure version used, evidence references, review and approval, and outstanding items with an owner, target date, linked task, and effect on completion. Distinguish preparation, review, and approval states with evidence for each. For blocked or interrupted work, record completed checks, unverified results, pending actions, and what is needed to resume. The next operator must be able to continue without the previous agent's conversation or hidden reasoning. Keep the process-specific fields and checklist in the SOP.

### Skill

Use the [Agent Skills format](https://agentskills.io/specification): begin `SKILL.md` with YAML metadata between `---` lines containing:

- **`name`:** a unique task name matching the skill folder; 1–64 lowercase letters, digits, or hyphens, with no leading, trailing, or consecutive hyphens. This differs from the display title.
- **`description`:** what the skill does and when to select it, in 1–1,024 characters. Include useful trigger terms and exclusions only where they prevent likely mismatches.

Follow the metadata and document header with these headings. They are this repository's convention; the external specification does not prescribe body headings.

| Heading | Required content |
|---|---|
| When to use | Intended task and result, with meaningful boundaries. |
| Inputs and prerequisites | Inputs, tools, access, dependencies, governing policy/SOP links, and action when prerequisites are missing. |
| Method | Direct instructions, tool or script usage, decision conditions, and necessary fallbacks. |
| Checks and output | Observable success checks, required output, and its permitted destination. |
| Exceptions and stopping conditions | Expected failures, safe recovery, escalation, and checks before retrying an uncertain action. |
| References and resources | Supporting files and authoritative references, stating when to read or execute each. |

Keep the entry file focused on task-specific knowledge, essential constraints, and directions to supporting material. Add `references/` for substantial conditional detail, `scripts/` for reusable executable helpers, and `assets/` for output templates only when needed. Link these directly from `SKILL.md`; an instruction-only skill needs no extra folders. Use portable paths and explicit dependencies, without relying on prior conversations or the author's machine. This follows [Anthropic's authoring guidance](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices).

**Discovery:** `AGENTS.md` must direct agents to the canonical skills location in the naming table and require reading the selected skill and necessary references. Storage there does not enable native automatic discovery. When configuring it, local [Codex](https://learn.chatgpt.com/docs/build-skills) uses `.agents/skills/<skill-name>/` and [Claude Code](https://code.claude.com/docs/en/skills#choose-where-skills-load) uses `.claude/skills/<skill-name>/`. Both support folder symlinks to the canonical skill. Keep one source copy and verify discovery in each intended client; other environments require their supported loading method.

## Drafting and Writing Rules

1. **Establish the facts.** Identify the purpose, scope, owner, and document type. Read authoritative sources and consult the people who own or perform the work. Distinguish observed practice, approved requirements, and proposed improvements. Ask focused questions and offer practical alternatives where a decision is needed; never invent responsibilities, limits, approvals, or controls. Keep discovery notes, rejected options, and case-specific decision records in the appropriate restricted system.
2. **Write like a knowledgeable colleague.** Use professional, direct, measured language, familiar terms, and active sentences. Explain significant reasons and tradeoffs. Use prose for explanations, numbered steps for sequences, and tables for comparisons. Omit generic background that does not help the reader act or decide.
3. **Make instructions testable.** Specify who acts, under what conditions, what they do, what they check, the acceptable result, and what happens if it fails. Replace vague directions such as “ensure accuracy” with concrete checks. Prescribe exact sequences when correctness depends on them; allow judgment within explicit boundaries elsewhere.
4. **State authority precisely.** Use **must** for requirements, **may** for permitted choices, and **should** for recommendations. Documentation must preserve approval boundaries; a skill or agent cannot grant itself authority or expand the requested task. Task status, model output, missing evidence, or a successful tool response alone does not prove completion or approval.
5. **Give each requirement one authoritative home.** Before adding content, check the existing document and relevant references for the same requirement. Update its existing section or place it under the appropriate required heading; do not append a new section for each request or discovery. Keep an instruction with its conditions and exceptions. Link to shared rules or methods at the point of use, with a brief reminder where needed to prevent error; do not copy their full explanation. Add a subsection or supporting file only when it serves a distinct purpose. Resolve conflicts with the responsible owner, and consolidate related wording without losing controls or decision boundaries.

## Information Boundaries

### Sources of truth

| Source | Authoritative content |
|---|---|
| Git repository | Durable business context, policies, SOPs, skills, and agent responsibilities. |
| Designated operational systems of record | Business records and their live state. |
| Designated task system | Each run's scope, progress, decisions, exceptions, reviews, approvals, completion, and carried-forward work. |
| Approved restricted evidence stores or originating systems | Supporting records and approval evidence, linked from the task system. |

SOPs must identify the actual sources and access required for their work. Confirm appropriate access restrictions in the task system before recording confidential details; link to evidence rather than copying it. A link is useful only if the authorised operator can access its evidence. Execution records belong outside Git: do not introduce `progress.md` or equivalent recurring-work logs.

### Confidentiality and reusable learning

The repository must not contain actual operational records, confidential information, or credentials. This includes financial records, personal or employment data, customer or supplier records, commercial terms, security details, and identifiable case histories. The rule applies even to a private repository and covers all files, skill resources, temporary or ignored material, logs, screenshots, commit messages, issues, and PRs.

Document business concepts, calculation methods, and process rules only where suitable for the repository's audience. For confidential limits, tolerances, rates, or other parameters, explain how authorised users obtain the current value from the restricted source. Operational approval does not authorise disclosure. Examples must be wholly fictional, clearly labelled, and independent of real cases.

For an edge case, document the general condition, why normal handling fails, required checks, handling method, decision authority, and completion evidence in the relevant SOP or skill. Omit real names, amounts, dates, identifiers, and any combination that could reconstruct the case. If the lesson cannot be separated from confidential facts, keep it restricted. Confirm the method with the responsible owner: one successful case does not establish an approved procedure. Apply the review and publication requirements below.

Check confidentiality **before writing** into the repository or its collaboration tools and again before committing or publishing. Do not copy records in and redact them afterwards. If a disclosure occurs, stop publication and notify the repository owner so removal from files, history, and affected locations can be assessed; deleting the current text alone is insufficient.

## Review and Publication

### Author checks

Before pushing a document for review, read the complete revised document and directly affected references, not only the changed passages. Confirm:

- **Structure:** Correct title, path, owner, headings, and clear scope.
- **Coherence:** Each requirement has a clear home; related conditions are together, repeated explanations are removed, and links take the reader directly to the needed guidance. Required controls remain explicit.
- **Support:** Authoritative sources or confirmed owner decisions support the guidance; no known flaws, placeholders, unresolved questions, or conflicting instructions remain.
- **Usability:** An unfamiliar operator can identify the actor, action, decision, authority, exception path, and verifiable result without assumed context. References are accessible and consistent.
- **Continuity:** Applicable completion, evidence, approval, retry, and handover requirements are explicit.
- **Confidentiality:** All proposed content meets the information boundaries above.

Validate the applicable document type:

| Type | Required validation |
|---|---|
| Policy | Walk through one ordinary application and one relevant boundary or exception. |
| Process/SOP | Walk through one normal path and one relevant exception from trigger to outcome. |
| Skill | Check metadata, folder naming, links, and dependencies. Test a representative request, a failure or missing-input case, and a similar request that should not select the skill. Verify outputs, new or changed scripts, and discovery in every client for which it is claimed. |

Use general or wholly fictional scenarios. Policy and SOP walkthroughs are document-only. Skill execution tests require a safe environment and must not perform unauthorised operational actions. Fix ambiguity and failures; report what was actually tested and any unverified compatibility. A walkthrough alone does not establish executable or cross-client reliability. Skill evaluation follows [OpenAI](https://learn.chatgpt.com/docs/build-skills#best-practices) and [Anthropic](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices#evaluation-and-iteration) guidance.

### Approval and merge

Every new or updated policy, SOP, skill, this framework, and related skill resources or discovery configuration must go through a PR targeting `main`. Never commit or push directly to `main`, including for small wording changes.

After the author checks, push the working branch and open a PR explaining the change, its purpose, and validation results. No separate walkthrough report is required. Obtain explicit approval from the responsible owner or an authorised designated reviewer. Address findings and obtain renewed approval if the content changes after approval; an agent's self-check does not replace review.

Merge only the reviewed, approved final content. The version on `main` is the operating reference; an unmerged document does not authorise a change in practice.
