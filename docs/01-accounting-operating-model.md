# Accounting operating model

## End-to-end record chain

The core payment chain is:

1. Obtain the supplier invoice, receipt, approved request, or other source evidence.
2. Retain the Jira/procurement reference and prepare the payment voucher.
3. Record the Xero bill or the appropriate prepayment, using the supplier's established convention.
4. Record the payment with the correct date, paying account and voucher/reference.
5. Import the relevant bank or petty-cash statement.
6. Match the statement line to the active Xero transaction or transactions.
7. Review unmatched items, deleted/voided history, and the overall account balance at a common cutoff.

Project coding follows a parallel chain:

1. Approved project request.
2. Project register and, when required, a sprint tracker.
3. Approved cost code in the source project/sprint tracker.
4. Import into the central cost-code tracker.
5. Use the code in voucher, bill and costing descriptions.
6. Validate detailed effort before invoicing or reporting.

## Identifiers and what they prove

| Identifier | Purpose | It does not prove |
|---|---|---|
| Supplier invoice number | Identifies supplier evidence | That the invoice was paid or correctly coded |
| Payment voucher number | Links approved payment support and tracker entry | That every row represents a separate cash movement |
| Bank reference or cheque number | Links the real cash movement | That the suggested Xero match is correct |
| Project/task cost code | Attributes the activity to approved project work | The Xero Department or GL classification |
| Xero Department | Reporting dimension in Xero | The detailed project/task code |

A single voucher may cover several bills. One bill may have several payments. A batch may span several tracker rows. Always reconcile the active amounts rather than counting rows.

## Core controls

### Evidence

- Match the supplier, period, invoice number, amount and support.
- Preserve leading zeros in supplier invoice numbers.
- Attach source evidence to Xero and retain the Jira/procurement link where required.
- If no formal invoice exists, use the PV reference and retain the best available approved receipt/request.

### Consistency

- Start with the supplier's historical dates, reference format, account, tax treatment and Department.
- Investigate genuine outliers before changing the current record.
- An old inconsistency is a question, not a template for future entries.

### Review and readback

- The training calls for independent review before reconciliation/payment completion.
- Recording a Xero payment records an event; it does not itself authorise a real-world payment.
- After a write, reopen or retrieve the saved record and verify the fields that were intended to change.
- Keep voided and deleted records visible for audit history but exclude them from active totals.

## Xero structure observed

Active bank/cash accounts observed:

- 02 — Petty Cash Atlas Populi
- 100 — LKR Account: Commercial Bank
- 101 — LKR Account: Union Bank
- 102 — USD Account: Union Bank
- 103 — USD Account: Commercial Bank

Active Department options observed:

- Architecture Visualisation
- General
- Product Engineering
- Software Development

The old Xero tracking category named **Cost Codes** is archived. Detailed project/task codes are maintained in the external project and cost-code trackers and carried in descriptions. Department and project/task code must therefore be checked separately.
