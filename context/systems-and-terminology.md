# Systems and terminology

**Status:** Draft for review  
**Prepared:** 16 September 2026  
**Scope:** The systems, records and terms needed to understand Atlas Populi Finance. This is an onboarding map, not an access-configuration guide or work instruction.

Read [Business background](business-background.md) and [Finance department](finance-department.md) alongside this document.

## Systems and records

| System or record | What it is used for | Distinction to understand |
|---|---|---|
| Xero | Supplier bills and payments, ledger records, attachments, bank matching and accounting reports. | A bill, a recorded payment and a reconciled statement line are different records or stages. |
| Jira | General Finance task and execution record for work scope, progress, comments, attachments, approvals, validation, outcomes and carried-forward items. See [General Finance Jira](general-finance-jira.md) for the current project structure and agent boundaries. | A work item's existence, assignment or status does not itself prove approval, a bank action or an accounting entry. Process-specific instructions remain in the applicable SOP or skill. |
| Bank portals and statements | Execution and evidence of bank transactions, including payments, receipts and transfers. | A bank movement establishes cash activity; its accounting classification needs supporting records. |
| Payment Voucher sheet / Payment Control Register | Monthly control record linking payment activity, supporting documents, references, posting and follow-up. | It is not a substitute for the general ledger, nor does each row necessarily represent a separate payment. |
| Batch Payment Tracker | Supporting records for grouped payments and preparation of bank-upload information. | Several payees or bills may be associated with a single payment batch. |
| Google Drive | Shared source documents and evidence used by Finance. See [General Finance Drive](general-finance-drive.md) for the current folder map and navigation boundaries. | Access to a source link must be checked; a link alone does not show the document was read. |
| Physical invoice files | Retention of VAT and other supplier invoices received in hard copy, as described in the AP SOP. | Physical and digital records may both be relevant to the same transaction. |
| Finance chat / Google Chat | Notification that payments or batches have been processed and communication of payment evidence. | It is a communication channel; the relevant formal records still need to be maintained. |
| Project register | Project identifiers, tracker links, managers and project status. | A project may exist before a cost code is required. |
| Project/sprint tracker | Approved project activities, resources, effort and costing support where relevant. | Not all projects require a sprint tracker; project-specific dates and confirmation matter. |
| Approved Cost Code tab and central cost-code tracker | Source-approved project/task codes and a central view importing those codes. | The source project/sprint tracker and the imported central view are different records. |
| Payroll/remuneration workbooks and sheets | Payroll or contractor inputs, changes and supporting calculations for the relevant entity and stream. | Historical file titles, rosters and forecast assumptions are not proof of current approved payroll. |
| Expense and cash-forecast workbooks | Recurring commitments, planning assumptions, expected spending and cash requirements. | Forecasts and payment-based analysis must be distinguished from accounting actuals. |
| This Git repository | Maintained business context, policies, SOPs, skills and agent responsibilities. Existing documents also contain historical reviews and examples. | The presence of documentation does not establish connector access, current approval or live financial status. |

The systems map draws on the local AP SOP and process guide, FP&A and payroll references, and the existing repository documents. It does not establish that every connector or application is configured for the current AI tool.

## Entity, currency and bank context

The [monthly-close checklist](../docs/10-monthly-close-agent-checklist.md) identifies the Xero entity as **Atlas Populi (Private) Limited**, with **LKR** as the base currency and a **31 March** financial year-end.

The [accounting operating model](../docs/01-accounting-operating-model.md) records the following account labels at the time of its review:

- Petty Cash Atlas Populi.
- LKR and USD accounts at Commercial Bank.
- LKR and USD accounts at Union Bank.

These are documented account descriptions, not a fresh confirmation of active accounts, balances or access. No bank account numbers or credentials are included.

The same operating-model document records Architecture Visualisation, General, Product Engineering and Software Development as Xero Department options. It records the older Cost Codes tracking category as archived, with detailed project/task coding maintained externally and carried in descriptions. These observations need live confirmation when a task relies on current configuration.

## Terminology

| Term | Meaning in this working context |
|---|---|
| Atlas Populi / AP | AP sometimes abbreviates Atlas Populi. It also commonly means accounts payable. Write “Atlas Populi” or “Accounts Payable” where the intended meaning would otherwise be unclear. |
| Atlas Labs / AL | The Australian parent described in the local business-context briefs; a separate entity from Atlas Populi. |
| Accounts Payable | Supplier obligations and the work supporting their recording and settlement. |
| Accounts Receivable | Amounts due to the relevant entity, with related billing and collection work. The entity raising the invoice must be clear. |
| Payment Voucher / PV | Payment-support and control record linking evidence, approvals and references. A voucher identifier is not a supplier invoice number. |
| BP / Batch reference | Reference conventions used by the payment-control workflow for individual or batch payments. Exact formats and treatment belong in the relevant work instructions. |
| Supplier invoice number | The supplier's identifier for an invoice. It identifies source evidence, not proof of payment. |
| Xero reference / object ID | A reference or system identifier linking a Xero record. A reference field and a system object ID are not interchangeable. |
| Bank reference / cheque number | An identifier associated with the cash movement or payment instrument. |
| Project/task cost code | An identifier attributing activity to approved project work. It is distinct from a general-ledger account and from Xero Department. |
| Xero Department / business unit | A reporting grouping. Labels used in Xero, payroll and voucher records may differ; their mapping should not be assumed. |
| General ledger / GL | The accounting record underlying balances and financial reporting. |
| Prepayment | An advance or prepaid-cost record whose subsequent use or expense recognition must be understood from the underlying arrangement. Specific classification and allocation rules belong in policy and work instructions. |
| Petty cash / float | Cash held for operational expenditure; replenishing the float and recording the underlying expense are different events. |
| Reconciliation | Comparing records at a defined cutoff and explaining differences, rather than assuming a matching amount proves the treatment is correct. |
| Actual, forecast and commitment | An observed result, an estimate of a future result, and an obligation or expected payment respectively. Each needs a clear basis and period. |
| FP&A | Financial Planning and Analysis: budgeting, forecasting, explanation of results and support for management decisions. |
| FTC / G&A / ArchViz | Labels used in the local payroll material: fixed-term contract, general and administrative, and architectural visualisation. Exact source labels should remain visible where relevant. |
| Payroll-related statutory terms | APIT, EPF and ETF appear in the local payroll material. Applicable calculations, eligibility and deadlines belong in the relevant reviewed payroll/tax instructions, not this background map. |

## How the records relate

The source invoice describes the charge. Jira records the request and supporting coordination or approval. The payment-control record links the operational payment support. Xero holds the accounting record. The bank statement evidences the cash movement.

These records do not always arise in that order. The local AP SOP includes advance payments and final invoices received later.

A voucher can support several bills, and a bill can have more than one payment. A batch can occupy several tracker rows. Those relationships explain why identifiers and totals need to be interpreted together.

For project work, the approved code originates in the source project/sprint tracker and is imported into the central tracker. The older local AP SOP calls the central sheet the master list; the more detailed repository project guide clarifies this source-versus-import relationship. This draft uses that distinction without changing either underlying procedure.

## Points to confirm during review

1. Which system and tracker links are the current canonical locations, particularly for payroll and forecasts?
2. Which named owners maintain those records and their access?
3. Are the account and Department descriptions above still current?
4. What is the agreed mapping between Department, business unit, payroll department and project cost code?
5. Which finance applications are actually in use, versus proposed in local build plans?

The reviewed local folders contain Finance Portal and automation plans. This draft does not treat those plans as proof of a live replacement for Jira, Sheets, bank portals or Xero.

## Sources and evidence limits

Repository sources:

- [Accounting operating model](../docs/01-accounting-operating-model.md).
- [Payment vouchers and Xero bills](../docs/02-payment-vouchers-and-xero-bills.md).
- [Projects, cost codes and effort](../docs/05-projects-cost-codes-and-effort.md).
- [Source register](../docs/08-source-register.md), for the existing training and tracker references. Linked external sources were not all reopened for this draft.
- [Monthly-close checklist](../docs/10-monthly-close-agent-checklist.md).

Local source references, relative to the author's AI Projects folder:

- `Atlas/AP Finance/Finance Portal/AP_Current_Process_Guide.md` — May 2026; systems and big-picture explanation.
- `Atlas/AP Finance/Finance Portal/AP_Current_Workflow.md` — 2 June 2026; systems, records and role descriptions.
- `Atlas/AP Finance/AP_Expenses_FP&A_Master_Handover.md` — prepared 4 July 2026; record distinctions and forecasting context.
- `Atlas/Payroll/Payroll_Forecast_Master_Knowledge.md` — selected terminology and stream descriptions.

This is a synthesis of documentation, not a new live-system audit. Current transactions, balances, personal payroll details and credentials are intentionally absent.
