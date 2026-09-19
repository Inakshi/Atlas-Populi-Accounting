# Agent Instructions

## Documentation

Read the [Documentation Framework](documentation-framework.md) before creating or updating documentation in this repository. Apply its fixed document structures, drafting rules, review criteria, repository confidentiality, and operational-continuity requirements. Resolve known flaws and drafting questions with the responsible owner before pushing a complete policy, process/SOP, or skill for review.

For this finance repository, use the area names in the [finance department context](https://github.com/Inakshi/Atlas-Populi-Accounting/blob/main/context/finance-department.md). Xero is the accounting system of record; Jira holds execution records and links to evidence in approved restricted stores.

Every new or updated policy, process/SOP, or skill, including changes to the documentation framework, must go through a PR targeting `main`. Never commit or push directly to `main`. Complete the applicable author checks, walkthrough, and skill validation, obtain review and explicit approval of the final content, and address findings before merge. An agent's self-check does not replace PR approval. Unmerged documents do not authorise changes to operating practice.

Maintain skill source files at `skills/<area-folder>/<skill-name>/SKILL.md`. Find the relevant skill through the SOP link or its metadata, then read its instructions and necessary references before use. This source location does not by itself enable native automatic discovery. Follow the framework's discovery guidance when configuring a supported client, and keep one canonical copy of each skill.

The repository holds durable business context, policies, processes/SOPs, skills, and agent responsibilities. Actual financial records, confidential case details, credentials, and execution logs must remain outside Git and the repository working directory. Record reusable edge-case handling without the underlying case details. Obtain process-owner review before treating a new handling approach as approved guidance.

## Recurring Work and Handover

Before starting recurring work, review the current Jira task, the most recent completed task for the same entity and process, and any open items carried forward. Check for intervening incomplete runs. Read the applicable context, policy, process/SOP, and skills, and verify relevant live state in the system of record. Prior task status or model output alone is not proof of completion.

Record progress, evidence references, exceptions, reviews, approvals, and the final outcome in the appropriately restricted Jira task. Preserve supporting financial evidence in approved restricted systems. Use the process-specific completion record, identify the procedure version used, and give each carried-forward item an owner, target date, and linked task. Verify uncertain action outcomes before retrying; do not duplicate financial writes.

Update the repository only when enduring context, policy, process/SOP, skill, or agent responsibilities change. Do not create a `progress.md` or equivalent repository log for recurring finance execution. If required access or evidence is missing, stop dependent work and report the specific blocker; if Jira is unavailable, report it to the requester through an approved channel. Never substitute an assumed result for verification.

These documentation and handover rules do not authorise financial writes. Preserve the applicable entity checks, exact approval scope, and live readback requirements.

## Communication

Explain the work and relevant decisions in detail as needed. End with a concise summary in simple English using these bullets:

- What was done
- Decisions
- Action Items
