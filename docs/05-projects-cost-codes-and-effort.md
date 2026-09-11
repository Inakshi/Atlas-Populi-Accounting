# Projects, cost codes and effort

## Project setup

1. Obtain the project request through the IT service desk, including project name/code, client, stakeholders and required applications/trackers.
2. If the service desk is unavailable, a direct-message fallback may be used, but it must contain the same essential information.
3. Check for project-number collisions before assignment.
4. Create the project folder and required tracker using the established naming convention.
5. Update the central project register with the tracker link, manager and status.
6. Notify the relevant finance reviewers after setup is complete.

A project can exist before a cost code is needed. Not every project requires a sprint tracker; the requirement depends on whether effort/invoicing needs to be tracked.

## Approved cost-code source

The source of truth is the project's/sprint tracker's **0. Approved Cost Code** tab. Record:

- entered by;
- scoping-document reference;
- code;
- description;
- status; and
- requester.

The central cost-code tracker should import the source code, description and status using IMPORTRANGE. Authorise the connection where appropriate and verify that values appear. Do not manually maintain a second version of the same code.

## Project 203 example

The training detected that project number 202 was already used. The resulting live project is 203, and its source tracker contains:

- **DG203_000_01**
- **Purchase of 3D Assets**
- **Active**

At review, the source code existed but the central tab **203-Greg Miller-1488 Dragon Glen** returned a #REF! connection error. The code is valid at source but is not reliably flowing into the central view.

## Roles

- Finance maintains the tracker structure and validates formulas and costing logic.
- The project manager supplies and finalises activities, resources, hours and sprint dates.
- Finance/reviewer checks detailed effort before invoicing or monthly reporting.
- A status such as “Ready for Invoicing” does not prove that an invoice was raised.

## Effort validation

Check:

- role-rate lookups against the rate card;
- working days and allocated fractions;
- source detail rows included in each subtotal;
- merged-cell/range boundaries;
- exact values before display rounding; and
- PM confirmation of completeness.

### Horcery Backend example

Q2 sprint 1, 8–21 May:

- Bug fixes: 95 + 55 + 125 = 275.
- Stall sharing: 95 + 55 + 92.5 = 242.5.
- Exact total: 517.5, displayed as 518.

Q2 sprint 2, 22 May–4 June:

- 142.5 + 55 + 277.5 + 375 = 850.

Preserve the exact 517.5 for downstream calculations. A two-week/ten-working-day sprint is a common Horcery pattern, not a universal rule; use PM-approved dates and effort detail.

The training does not establish how to allocate a sprint crossing month-end between monthly invoicing and VAT Schedule 7. That remains an open policy question.
