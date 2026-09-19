# SOP / Accounts Payable / Payment Voucher Process End-to-End

**Accountable owners:** Head of Finance and Finance Executive

## Purpose, outcome, and scope

This SOP governs the Atlas Populi payment-voucher process from an approved Jira request through human payment execution, entry in the Payment Voucher Sheet, and verified recording in Xero. It applies to individual online payments, cheque payments, partial payments, and advance payments. Batch payments are outside the current scope and must follow a separately approved process.

The outcome is a traceable chain between the approved request, the real payment and its evidence, the Payment Voucher Sheet, and the corresponding Xero records. Each system establishes a different part of that chain:

| System or record | What it establishes |
|---|---|
| Jira | The request, supporting documents, approvals, payment evidence, human directions, agent handoffs, and completion record. |
| Bank evidence or cheque | Whether and how the human-executed payment was processed. A cheque issue does not prove that it cleared the bank. |
| Payment Voucher Sheet | The operational register of payment lines, voucher references, invoice follow-up, filing, and Xero status. |
| Xero accounting system | The payable record and the accounting entry for the payment. |

Use the identifiers as follows:

| Identifier | Required use |
|---|---|
| Jira task number | Primary link from the payment evidence and Payment Voucher Sheet to the request, approvals, and support. Quote it in the bank narration for an individual online payment where the bank permits this. |
| Payment-voucher number (BP/PV number) | Assigned in the Payment Voucher Sheet for an individual online or cheque payment. Use it as the Xero payment reference and write it on a physically filed invoice. |
| Supplier invoice number | Use as the Xero bill reference when an official invoice exists, preserving leading zeros. |
| Cheque number | Links a cheque payment to its payment instrument and Payment Voucher Sheet entry. |

One payment may cover several invoices, and one invoice may be paid in several instalments. Verify the full relationship using the identifiers, payee, payment date, amount, payment evidence, and active Xero allocation. No identifier or register row proves completion by itself.

This SOP does not govern supplier selection, purchasing, batch payments, changes to approval authority, detailed bank-interface instructions, or bank reconciliation. Reconciliation begins after the records governed by this SOP are ready for review.

## Trigger and prerequisites

Every payment must begin with a Jira task created by Finance, Procurement, or another initiating department. Before a human executes the payment, the task must contain or link to:

- the supplier or payee and verified payment details;
- the invoice, quote, pro-forma invoice, receipt, or other available support;
- the amount, agreeing with the support;
- the applicable cost code;
- HOD, manager, or lead approval recorded in a Jira comment; and
- CEO approval recorded in a Jira comment.

The Head of Finance checks these prerequisites and returns an incomplete or conflicting request to the initiating department. A Jira status, attachment, or request to pay does not by itself prove approval or payment.

Agents do not initiate, approve, or execute real bank or cheque payments under this SOP. The agent workflow begins only after an authorised human has executed or issued the payment and the required payment evidence is available.

| Role | Responsibility |
|---|---|
| Initiating department | Creates the Jira request and supplies the required information, evidence, cost code, and approvals. |
| Head of Finance and other authorised human payment roles | Validate the request, execute or issue the real payment within their authority, and provide payment evidence. |
| PV/Xero preparation agent | Creates the annual register when required, makes the provisional Payment Voucher Sheet entry, prepares the Xero payable record, attaches evidence, and submits it for review. |
| Xero reviewing agent | Independently reviews the prepared record, returns errors for rework or approves the record, records the payment in Xero, and verifies the saved result. This must be a different agent from the preparation agent for the same item. |
| Responsible human | The Head of Finance or Finance Executive acting on the Jira task. Gives Xero-recording direction when the treatment is unclear and approves any destructive or posted-record correction. |

The people and agents performing the process need authorised access to the Jira task and evidence, the approved restricted Google Drive locations, the Payment Voucher Sheet, payment evidence, and the Atlas Populi Xero organisation. Before recurring work, check the current Jira task, the most recent comparable completed task, carried-forward items, incomplete intervening runs, and the relevant live system state.

### Payment Voucher Sheet location and annual setup

The Payment Voucher Sheet is stored in [General Finance (Restricted) / 1. Corporate: Atlas Populi / 1. Payment Vouchers](https://drive.google.com/drive/folders/1KeNf94_JdO7tGq_Gs0wF5dlDF2ya62ve). Atlas Populi's financial year runs from 1 April to 31 March.

Before the first payment entry of a new financial year, the PV/Xero preparation agent must create the annual register in the corresponding `FY<YYYY/YY>` folder, name it `Payment vouchers: FY <YYYY/YY>`, create monthly tabs from April through March, and verify the standard register fields. During payment processing, do not create an improvised replacement file or tab. If the expected register is missing, duplicated, renamed, or structurally different, stop and correct or restore the controlled annual register before continuing.

## Process steps and decisions

### 1. Confirm human payment execution and evidence

An authorised human performs the real payment:

- For an individual online payment, the Head of Finance executes the transfer from the approved Jira task, quotes the Jira task number in the bank narration where possible, and adds the payment receipt to Jira and Finance chat.
- For a cheque payment, the assigned human finance preparer writes the cheque, the Head of Finance reviews it, and the CEO signs it before issue. Retain the cheque number and issue evidence.

The PV/Xero preparation agent must not continue until the payee, payment date, amount, payment method, identifier, and evidence of execution agree with the approved Jira task. If the payment outcome is uncertain, apply the stopping rule under Exceptions and escalation.

### 2. Create the provisional Payment Voucher Sheet entry

The PV/Xero preparation agent selects the annual register from the payment date's financial year and the tab from the payment month. Confirm the Atlas Populi entity, financial-year title, monthly tab, and expected fields before entering anything.

Record the applicable filing status, payment-voucher number, Jira task number, payee, payment details, cost code, invoice value, actual amount paid, currency and exchange-rate information, business unit, payment method, cheque number, Xero status, and notes.

Apply these register rules:

1. Assign the next monthly BP/PV number in payment order using `BP<sequence>/<month>/<year>`. If a missed payment must be inserted after later numbers were assigned, add a letter suffix to the preceding sequence using `BP<sequence><letter>/<month>/<year>`. Never replace or reuse an assigned number.
2. Use one row per distinct invoice or payment line. When one cash movement spans several rows, record the total amount paid on the first row and leave the Amount Paid field blank on the remaining related rows.
3. Keep invoice value and actual amount paid separate.
4. Add `INV` when no invoice has been issued or a final invoice is outstanding. Add `VAT` and the required blue highlight for a VAT-invoice row.
5. Leave the `Xero` field blank at this stage. Mark it `Yes` only after the payable record is in Xero and the required invoice or human-approved alternative support is attached. Do not introduce a `No` value.

### 3. Prepare the Xero payable record

The PV/Xero preparation agent first searches the Atlas Populi Xero organisation for the supplier invoice, existing draft or repeating bill, prepayment, and active payment. Use the supported existing record. Do not create a duplicate because an item is absent from an ordinary bill search.

Select and document the treatment using the following rules:

| Condition | Required treatment |
|---|---|
| Official one-off invoice | Use the supplier, invoice number, invoice date, due date, value, and service details from the source, subject to any documented supplier exception. |
| Recurring supplier or service | Review previously approved or paid Xero records for the same supplier and service. Use the established service-period, invoice-date, and due-date treatment. The invoice date is usually the first day of the service month, but apply a different date when the consistent approved history supports it. Use the current source due date when the established treatment shows that the source governs; otherwise follow the consistent approved due-date convention. If the history does not establish either date or conflicts with the current evidence, stop and obtain human direction in Jira. |
| No invoice issued | Retain the quote, pro-forma invoice, or other available support and keep `INV` in the Payment Voucher Sheet. Obtain human direction in Jira on the Xero record type, reference, date, accounting treatment, and evidence requirement before creating or completing the Xero record. This direction concerns the accounting record; it is not authority for the already human-executed payment. |
| Partial or advance payment | Use an existing supported bill or prepayment treatment where the current evidence and approved history establish it. If the record type or allocation is unclear, stop and obtain human direction in Jira. Record only the supported amount and active allocation. |
| VAT invoice | Where the approved source and established treatment require separate VAT, record the expense base against the supported expense or direct-cost account and the separately identified VAT against **314 — VAT Input**. Use the current authorised Xero tax treatment, include `VAT` in the description, and do not calculate VAT again when the source already separates it. |

For a recurring bill, also:

1. Confirm that no active bill already covers the same service period.
2. Use `<invoice number> <service month> <year>` as the reference for one recurring service.
3. For several services from the same supplier, use `<connection or service identifier>_<invoice number>_<service month> <year>`.
4. Make the reference and description agree on the service period.
5. Complete an existing repeating-bill draft instead of creating a duplicate.

For every prepared payable record, verify the supplier or supported payee, reference, invoice and due dates, service period, description, Jira cost code, general-ledger account, tax treatment, amount, allocation, source attachment, and Jira reference. The cost code and general-ledger account are separate classifications; apply the [chart-of-accounts and coding reference](../../policies/chart-of-accounts-and-coding-reference.md).

Attach the required digital support and save the prepared record without approving it. Mark the Payment Voucher Sheet's `Xero` field `Yes` only when the payable record is in Xero and the required invoice or human-approved alternative support is attached; otherwise leave it blank and retain `INV`. Hand the item to the Xero reviewing agent through Jira, recording the prepared Xero record link and checks completed. The preparation agent must not approve the record or record its Xero payment.

### 4. Review, approve, and record the Xero payment

The Xero reviewing agent independently compares the prepared record with the Jira request and approvals, payment evidence, Payment Voucher Sheet entry, source support, duplicate search, coding, dates, reference, service period, amount, allocation, attachment, and paying account.

If an ordinary draft error is found, the reviewing agent records the finding in Jira and returns the item to the preparation agent. The preparation agent corrects the draft and resubmits it; the reviewing agent then repeats the independent check. The reviewing agent must not silently correct the preparation agent's draft.

If the record is correct, the reviewing agent approves it and records the accounting payment against the correct active payable record using the actual payment date, paying account, amount, and BP/PV number as the Xero payment reference. For a partial payment, record only the supported active allocation. Exclude deleted payment attempts from active totals.

The reviewing agent then reopens or retrieves the saved Xero records and verifies the payable record, attachment, approval status, payment, paying account, date, amount, reference, and active allocation. A successful tool response alone is not completion. Recording a payment in Xero does not authorise or execute a real bank payment.

The reviewing agent records the verified outcome and Xero links in Jira and hands the item back to the PV/Xero preparation agent.

### 5. Finalize the register, evidence, and handover

After receiving the verified reviewer handback, the PV/Xero preparation agent:

1. Rechecks that the Xero payable record and payment agree with the Payment Voucher Sheet entry and payment evidence.
2. Confirms that the Payment Voucher Sheet's `Xero` field correctly reflects whether the payable record and required support are present in Xero. If the field remains blank because evidence is outstanding, do not change it merely because review and payment recording are complete.
3. Retains `INV` until the final invoice is attached in Xero, or until the responsible human confirms in Jira that no invoice will be issued and approves the retained support and accounting treatment.
4. For a physical invoice, writes the BP/PV number on it, files it by month, and updates the register's `Filed` or legacy `Filled` field. Electronically received non-VAT invoices do not require a physical copy unless another approved requirement applies.
5. Records the completion outcome in Jira, including the payment method and outcome, this SOP's repository path and Git commit, evidence links, Payment Voucher Sheet entry, Xero records, preparation and review evidence, human directions, and outstanding items.

Each outstanding item must have an owner, target date, linked Jira task, and stated effect on completion.

If a final invoice arrives after the initial Xero recording, the PV/Xero preparation agent resumes at step 3 to attach it and make any human-directed update. Any change to the Xero reference, date, amount, tax treatment, record type, or allocation must be independently reviewed under step 4. After verification, return to this step to update the Payment Voucher Sheet and Jira. Apply the same return path after an approved correction whenever the correction changes a dependent register or Jira record.

## Exceptions and escalation

| Condition | Required response |
|---|---|
| Jira information, support, amount, cost code, payment details, or approvals are missing or conflicting | Stop. Return the Jira task to the initiating department. Do not infer missing authority or evidence. |
| Real payment outcome is uncertain | Stop. Check the bank or cheque evidence and Jira before any human retries the payment. An agent must never initiate or repeat the payment. |
| No invoice has been issued | Continue only to the point where human Xero-recording direction is required in step 3. Retain the available support and `INV`; do not assume the accounting treatment or that the support is final. |
| Recurring history is absent, inconsistent, or conflicts with current evidence | Stop Xero preparation and obtain human direction in Jira. Do not turn an unexplained historical outlier into a rule. |
| Reviewer finds an ordinary draft error | Return the item to the preparation agent for correction and resubmission. Preserve separation of duties. |
| An incorrect, duplicate, approved, or paid Xero record requires deletion, voiding, reversal, or reallocation | The reviewing agent verifies the issue and reports the affected records, evidence, proposed correction, and expected effect to the responsible human. Proceed only after explicit approval is recorded in Jira. Perform only the approved correction, read back the live result, and report the verified outcome. |
| A Xero save or payment-recording outcome is uncertain | Retrieve the live Xero record and active payments before retrying. Do not repeat a write to obtain a clearer response. |
| Jira, the Payment Voucher Sheet, payment evidence, or Xero is unavailable | Stop the dependent work, record completed checks and unverified results, and report the blocker through an approved channel. Verify current live state before resuming. |

An exception becomes reusable guidance only after an accountable owner reviews it and the approved documentation change is merged.

## Completion and handover

The process is complete only when:

- the Jira task contains the request, applicable support, approvals, and human-executed payment evidence;
- the Payment Voucher Sheet entry is complete without double-counting;
- the preparation agent has prepared the supported Xero payable record and attached the required evidence;
- a separate reviewing agent has approved the payable record, recorded the Xero payment, and verified the saved records;
- the preparation agent has completed the final register check after reviewer handback, with the `Xero` field reflecting whether the payable record and required support are present; and
- the Jira completion record contains the procedure version, evidence links, preparation and review evidence, human directions, and any outstanding items.

Where an invoice remains outstanding, the payment may already have been executed and recorded, but the invoice follow-up remains open until the final invoice is attached or the responsible human approves the alternative support and treatment. Keep the payment Jira task open, or move the follow-up to a linked Jira task with an owner and target date before closing the payment task. Record the resolution in Jira before removing `INV`. Month-end cannot close while an `INV` item remains unresolved.

The completed records are inputs to month-end review by a Finance team member other than the preparation agent, followed by bank reconciliation. Completion of this SOP does not prove that the bank statement was imported, the payment was reconciled, or the accounting period was closed.

For interrupted work, Jira must identify completed checks, unverified results, pending actions, and what the next agent must verify before continuing. The next agent must be able to resume without access to the previous agent's conversation or hidden reasoning.

## Related policies and skills

- [Chart of accounts and coding reference](../../policies/chart-of-accounts-and-coding-reference.md) — governs account selection and restricted-account use.
- [Systems and terminology](../../context/systems-and-terminology.md) — defines the systems, records, and identifiers used in this process.
- [Projects, cost codes and effort](../../docs/05-projects-cost-codes-and-effort.md) — identifies the approved source and maintenance process for project and task cost codes.
- [Bank and petty-cash reconciliation](../../docs/03-bank-and-petty-cash-reconciliation.md) — begins after the payment and Xero records are ready for matching.

Supporting skills should be created for annual Payment Voucher Sheet setup and entry, Xero payable preparation, and Xero review and payment recording. Those skills must implement this SOP without changing its authority or decision boundaries.
