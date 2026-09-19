# Finance department

**Status:** Draft for review  
**Prepared:** 16 September 2026  
**Basis:** The seven functional areas below were agreed with the user on 16 September 2026. Detailed descriptions and ownership boundaries remain subject to review; this document does not appoint staff or amend approval authority.

Read [Business background](business-background.md) first. For the records and tools used by Finance, see [Systems and terminology](systems-and-terminology.md).

## Department purpose

Atlas Populi Finance supports the operation of the Sri Lankan entity by maintaining reliable financial records, coordinating payments, explaining expenditure and cash requirements, and supporting project-cost reporting. It works with Procurement, department heads, project managers and management to connect business activity with the corresponding financial records.

This purpose statement is a draft synthesis of the AP SOP, expense-planning material and project documentation. A complete department charter and current performance measures have not yet been supplied.

## High-level department structure

These are areas of responsibility, not seven required job positions or seven mandatory AI agents. A person or agent may support more than one area, while applicable preparation, approval and independent-review responsibilities remain distinct.

| Area | Purpose and principal responsibilities | Important boundary |
|---|---|---|
| Accounts Payable | Maintain supported supplier obligations: invoice handling, payment vouchers, supplier balances, invoice follow-up and payment-request preparation. | Payment preparation and accounting records do not themselves establish bank payment execution or authority. |
| Accounts Receivable and Billing | Prepare invoices from approved billing information; manage credit notes, receivables, collections and receipt allocation. | Atlas Populi's actual customer/intercompany billing scope needs confirmation. Atlas Labs' customer billing is not automatically in scope. |
| Payroll | Prepare and reconcile payroll and contractor-payment information, including approved changes, deductions and employer contributions; hand off payment requirements. | Employment and contractor streams remain distinguishable. This area does not absorb Atlas Labs payroll by default. |
| Banking and Treasury | Manage payment execution, bank and petty-cash operations, transfers, foreign-currency conversions, bank reconciliation, cash availability and funding requirements. | Combining the area does not combine preparation, execution and independent review into one authority. |
| Financial Accounting and Reporting | Own general-ledger completeness, journals, accruals, prepayments, fixed assets, intercompany balances, period-end close, financial reporting and audit support. | This is the agreed functional home for these responsibilities; current detailed procedures and owners are not fully documented for every item. |
| Tax and Statutory Compliance | Coordinate tax reconciliations, returns, payments, refunds and statutory reporting calendars. | The split with Payroll for payroll-related obligations needs an explicit handoff. This document does not prescribe tax rates, filing dates or legal treatment. |
| Financial Planning and Analysis (FP&A) | Prepare budgets and forecasts; explain spending and variances; support workforce-cost planning, project-cost analysis and management decisions. | Forecasts and scenarios remain distinguishable from actual accounting results. Project-cost validation feeds Billing where relevant. |

The Finance functional areas above are different from business reporting categories such as Software Development or Product Engineering.

## Responsibilities that cross several areas

### Supplier payments and accounting close

Accounts Payable establishes the supported supplier obligation and payment information. Banking and Treasury handles the authorized movement of cash and bank-side evidence. Financial Accounting and Reporting owns whether the resulting accounts are complete and supported at period end.

This describes the responsibility boundary, not a new mandatory transaction sequence. Existing procedures cover cases where payments precede final invoices. Detailed sequencing belongs in the applicable SOP.

Prepayments illustrate the handoff: Accounts Payable helps establish supplier support; Banking and Treasury evidences cash movement; Financial Accounting and Reporting owns the appropriate period-end accounting and reconciliation.

### Payroll, tax and cash planning

Payroll prepares and reconciles the payroll or contractor amounts. Tax and Statutory Compliance coordinates the relevant reporting obligations, with the precise preparation/submission ownership still to be confirmed. Banking and Treasury executes authorized payments. FP&A uses supported payroll information to forecast workforce costs.

The local payroll knowledge base distinguishes Atlas Populi FTC/internship, data-labeling contractor and 0-hour contractor streams from Atlas Labs arrangements. This draft records that distinction without importing historical employee rosters, rates or model-specific exclusions.

### Project costing and billing

Project managers provide and confirm activities, resources, hours and dates. Existing documentation assigns Finance responsibility for tracker structure, formulas, costing logic and effort checks before invoicing or reporting.

In the agreed department map, project-cost analysis sits within FP&A and hands approved billing information to Accounts Receivable and Billing. Confirm the invoicing entity and the person responsible for issuing invoices before using that handoff operationally.

### Planning and treasury

FP&A explains spending drivers and expected future costs. Banking and Treasury considers available cash, payment timing and funding needs. They should share the relevant forecast inputs rather than maintain conflicting versions of cash requirements.

## Working relationships documented in existing sources

The local AP SOP dated 2 June 2026 describes the following roles. These descriptions support onboarding; they are not a current named roster, authority matrix or delegation of access.

| Role or stakeholder | Documented relationship with Finance |
|---|---|
| Procurement | Assembles payment requests, supporting documents, payment details and approvals. |
| Department heads, managers and leads | Review business requests and provide the approvals required by the applicable process. |
| CEO / management | Provides approvals or decisions where required by the documented process. |
| Head of Finance | Reviews payment requests, oversees bank execution and shares payment evidence under the existing AP workflow. |
| PV / Xero preparer | Maintains the payment-control record and the corresponding Xero entries and attachments. |
| Batch payment preparer | Prepares assigned batch-payment support and bank-upload files. |
| Month-end reviewer / reconciler | Reviews recorded activity and reconciles accounts separately from preparation. |
| Project managers | Supply and confirm project effort, resources, dates and completeness for Finance's costing and invoicing support. |

Named owners, deputies and broader interfaces such as HR/payroll input ownership still need confirmation. A title or role description alone does not grant payment authority.

## What successful Finance work should make possible

The reviewed sources point to these practical outcomes:

- Traceable links between business support, recorded obligations and cash movements.
- Complete, supportable period-end accounts with unresolved differences visible.
- A useful explanation of spend drivers and future cash requirements.
- Reliable project effort and cost information for billing and management reporting.

These are draft outcome statements, not approved numerical targets or service-level commitments.

## Points to confirm during review

1. The named owner and backup for each area, including work performed outside the immediate Finance team.
2. Atlas Populi's billing and collection responsibilities, including intercompany billing.
3. Responsibility boundaries for payroll inputs, statutory submissions, tax-adviser coordination and payment release.
4. Management reporting recipients, reporting cadence and current Finance priorities.
5. Coverage and ownership of fixed assets, year-end reporting and audit support, where the reviewed sources do not provide a full procedure.

## Sources and evidence limits

- User agreement on the seven-area department map, 16 September 2026.
- [Payment Voucher Process End-to-End SOP](../processes/accounts-payable/payment-voucher-process-end-to-end.md): payment evidence chain and accounting-record distinctions.
- [Projects, cost codes and effort](../docs/05-projects-cost-codes-and-effort.md): Finance/project-manager relationship and billing support.
- [Monthly close checklist](../docs/10-monthly-close-agent-checklist.md): cross-process review and close responsibilities.
- Local `Atlas/AP Finance/Finance Portal/AP_Current_Workflow.md`, updated 2 June 2026: AP scope, systems and roles.
- Local `Atlas/AP Finance/AP_Expenses_FP&A_Master_Handover.md`, prepared 4 July 2026: spending analysis, cash timing and reporting support.
- Local `Atlas/AP Finance/Cash Forecast/Cash forecast prompt.md`: expense-forecast questions.
- Local `Atlas/Payroll/Payroll_Forecast_Master_Knowledge.md`: payroll-stream distinctions, from selected sections.

Local paths are relative to the author's AI Projects folder. Existing documents establish parts of the operation, not proof that every responsibility above already has an implemented process. This draft does not replace policies, SOPs, approval requirements or professional sign-off.
