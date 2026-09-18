# General Finance Jira

**Accountable owner:** Finance  
**Scope:** Current organisation and use of the General Finance Jira project, including the boundaries an authorised agent must follow when creating, progressing and handing over Finance work.

## Purpose and scope

The [General Finance Jira project](https://atlas-labs.atlassian.net/jira/software/projects/GF/boards/66) is Finance's task and execution record for work managed in the `GF` project. It gives the Finance team and authorised agents a continuing record of what work was requested, which legal entity it relates to, its period, current status, supporting evidence, approvals, reviewer and outcome.

The project includes work relating to Atlas Populi, Atlas Labs and Horcery. Their work may be managed in the same Jira project, but the entities remain separate. An agent must confirm the legal entity before creating, interpreting or updating a work item.

This document explains the General Finance Jira structure and the common rules for using it. It does not define how payments, bank reconciliations, payroll, tax, audit or other Finance processes are performed. Those instructions belong in the applicable SOP or skill. The Restricted Finance Jira project is outside this document's scope.

## Jira and the other Finance systems

Jira is the authoritative task record for the scope, progress, decisions, exceptions, comments, attachments, approvals, validation, outcome and carried-forward work for a Finance activity.

Jira is not the accounting ledger or proof of a bank action. Xero remains the accounting system of record, bank portals and statements evidence cash movements, and Google Drive may contain working files or supporting documents. A Drive file is not required for every Jira task, and Drive does not replace the Jira task record.

Attachments and approvals needed to understand or review the task must be retained in Jira. Where evidence is maintained in another approved restricted system, the Jira task must identify or link to it clearly enough for the authorised reviewer to retrieve it. Confidential operational details and evidence must remain in Jira or another approved restricted system and must not be copied into GitHub.

## Agent authority and boundaries

When an agent is assigned Finance work, it may create and maintain the General Finance Jira work item needed to record that assigned work. This authority is limited to the assigned activity and does not extend to unrelated work items, other Jira projects or additional operational actions.

Before starting the activity, the agent must:

1. Confirm the legal entity.
2. Identify the correct period-specific Epic.
3. Check the current Jira state, the most recent completed comparable work for the same entity and process, and any unfinished or carried-forward work.
4. Ask which human will perform the required validation and receive the work item at the Validation stage.
5. Confirm that the task itself provides authority for the intended operational work. Creating a Jira record does not authorise a bank, Xero, Drive or other external action.

The agent may create the work item, update its description and applicable fields, add comments and authorised evidence, move it through the statuses supported by verified progress, and assign it to the identified human validator when it reaches Validation.

This context document does not authorise an agent to delete or archive work items, comments or attachments; change project configuration, workflows, work types or sprint settings; or change work outside the assigned scope. Any such action requires specific authority.

After creating or updating a work item, the agent must reopen or reread it and verify the parent Epic, legal entity, period, sprint, status, assignee, recorded update and evidence.

## Legal entity identification

The legal entity must be unambiguous from the Epic and child work item together. The agent must not infer the entity solely from the absence of an entity prefix, a familiar supplier, a filename, the assignee or the previous month's task.

When an Epic is entity-specific, its child items must remain under that Epic. When an Epic contains work for more than one entity, each child item's summary or description must identify its legal entity clearly.

If the available Epic and work-item information do not establish one legal entity, the agent must stop and ask before proceeding.

## Epics and work-item structure

### Epics

An Epic groups one Finance process or work group for a specific period. Recurring monthly Epics must include the month and year in their title.

Use the naming pattern:

- `<Process or work group>: <Month YYYY>` where the entity is otherwise made explicit.
- `<Entity> <process or work group>: <Month YYYY>` where the entity prefix is needed to distinguish parallel work.

The Epic is the parent record for its child work items. Its child list provides the operational breakdown and shows which parts are To Do, In Progress, in Validation or Done.

Before creating a child item, the agent must search for the applicable Epic and check that its process, period and entity match the task. It must not attach work to the nearest or most recent Epic merely for convenience. If the correct Epic does not exist, the agent must ask whether it should create a new Epic.

An Epic's status alone does not prove that its process is complete. The agent must check the status and outcome of every relevant child item and any carried-forward work.

### Work types

| Work type | Use in General Finance |
|---|---|
| `Epic` | A period-specific Finance process or work group containing related child items. |
| `Payments` | An individual payment activity. Its required fields, approvals, payment details and evidence are governed by the applicable payment SOP or skill. |
| `Task` | An individual non-payment Finance activity, such as a reconciliation, payroll, tax, reporting or other process step. Its required information depends on the applicable process. |
| `Subtask` | A smaller action that must be tracked separately beneath a work item when the parent alone is not sufficient. |
| `Story` | Not used as a standard Finance work type. An agent must not select it merely because it is available. |
| `Bug` | Not used as a standard Finance process work type. Use it only when the task specifically concerns a system defect and the intended treatment is confirmed. |

## Choosing the fields and evidence

There is no single field set for every Finance task. The agent must use the applicable SOP or skill and compare the most recent completed equivalent work item for the same entity and process to identify the expected structure.

Historical work provides a consistency reference, not authority to copy old values, approvals, dates, assignees, attachments or conclusions. The agent must confirm all current-period information and must not treat a previous task's completion as proof that the current work is complete.

Every new work item must contain enough information for another authorised person to understand:

- the work to be completed;
- the legal entity;
- the applicable period;
- the parent Epic;
- the work type;
- the current weekly sprint;
- the person performing the work;
- the human who will validate it;
- the task-specific inputs, instructions and links;
- the evidence and approvals required by the applicable process; and
- the current outcome, exception or next action.

Use task-specific fields when the process requires them. For example, a payment item may require a cost code and payment support, while a reconciliation, payroll or tax task requires different inputs and evidence. Do not add irrelevant fields merely to imitate a different process.

## Weekly sprints

General Finance uses weekly sprints to organise active work. A work item must be placed in the weekly sprint in which the work is being performed.

If the work is unfinished at the end of the week, move it into the next weekly sprint. Retain the original process period in the Epic and work-item title; the sprint records when the work is actively being handled, not the accounting or operational period to which it relates.

Moving an item to a new sprint does not change its status, resolve its blockers or prove that it was reviewed. The work-item comment must explain any material delay, blocker or carried-forward action needed by the next operator.

## Status workflow

| Status | Meaning | Required handling |
|---|---|---|
| `To Do` | The work item has been created but active work has not started. | Confirm the entity, correct Epic, period, sprint, task inputs and human validator before starting. |
| `In Progress` | Work has actually started and remains with the preparer or agent. | Keep the task current through comments and evidence. Record blockers or unresolved questions rather than implying completion. |
| `Validation` | The preparer or agent has completed its work and the item is waiting for the identified human to review, approve or complete the required validation. | Add a completion comment, attach or link the evidence, assign the item to the human validator, and state exactly what validation is required. A payment awaiting bank review or approval remains in Validation. |
| `Done` | The required work and human validation have been completed. | Move the item to Done only after the required review or approval is complete and the task record contains the final outcome. |

The normal sequence is `To Do` → `In Progress` → `Validation` → `Done`. A task must not move directly to Done merely because the agent finished its preparation, a file was produced, a payment was initiated, or a tool returned success.

## Creating and completing an agent-managed task

1. **Inspect current and prior Jira state.** Check for an existing task for the same entity, process and period; review the most recent completed equivalent; identify unfinished older work and confirm that no duplicate task will be created.
2. **Confirm the entity and validator.** Establish the legal entity and ask which human should receive the item for Validation.
3. **Select the Epic and work type.** Use the matching process-and-period Epic and choose `Payments`, `Task` or another specifically justified work type. Ask before creating a missing Epic.
4. **Create the item in To Do.** Use a clear summary consistent with comparable tasks. Add the parent Epic, current weekly sprint, assignee, task-specific information, evidence links and attachments required to begin.
5. **Move to In Progress when work starts.** Do not use In Progress for work that has not actually begun.
6. **Perform the authorised work.** Follow the applicable SOP or skill. Keep financial writes and other external actions within their separate approval boundaries.
7. **Record the result.** Add a comment stating exactly what was completed, the result, the evidence or attachment location, checks performed, and any exception or outstanding action. Avoid vague updates such as `completed` without supporting detail.
8. **Hand over for Validation.** Move the item to Validation, assign it to the human identified at the start, and state what the human needs to review or approve.
9. **Confirm final completion.** Treat the work as Done only after the required human validation is complete. Verify the final status, comments, evidence and outcome.

## Recurring work and continuity

Before beginning a recurring activity, the agent must review:

- the current-period Epic and work item;
- the most recent completed work item for the same legal entity and process;
- any open child items from earlier periods;
- unfinished work carried through weekly sprints;
- comments, evidence and validation outcomes that affect the current period; and
- the relevant live state in the operational system of record.

The agent must use those records to avoid duplicate work and to preserve continuity. It must not assume that an earlier task marked Done proves the underlying current-period bank, Xero, Drive or other system state.

For incomplete or blocked work, the Jira record must state what has been completed, what remains unverified, the blocker, the required next action, the owner or validator, and the effect on completion. An unfinished task remains visible and must be moved to the next active sprint rather than recreated without checking the existing item.

## Jira check

Before finishing an agent-managed Jira update, confirm:

1. The work item is in the General Finance project.
2. One legal entity is confirmed and is unambiguous from the Epic and work item together.
3. The correct process-and-period Epic is selected.
4. The work type matches the activity.
5. The month and year are present in the recurring monthly Epic title.
6. The item is in the current weekly sprint, or unfinished work has been carried to the next sprint.
7. The status reflects the verified stage of work.
8. Task-specific fields, attachments, approvals and evidence are present or clearly linked.
9. The comments state what was done, the result, exceptions and next action.
10. The correct human validator was identified at the start and receives the item in Validation.
11. The item is not marked Done before the required human validation is complete.
12. The saved Jira state has been reread and verified.

If any required point is unresolved, the agent must leave the item at the appropriate non-final status and ask for direction.

## Related documents

- [Systems and terminology](systems-and-terminology.md) — how Jira relates to Xero, Drive, bank evidence and other Finance records.
- [General Finance Drive](general-finance-drive.md) — where Finance working documents and supporting files are organised.
- [Finance department](finance-department.md) — Finance areas and responsibility boundaries.
- [Documentation Framework](../documentation-framework.md) — where durable context, policies, SOPs and skills belong.