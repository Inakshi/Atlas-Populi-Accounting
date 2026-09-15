# Monthly supplier control register

## Purpose

This register tells the monthly-close agent which supplier patterns must be checked and what the expected treatment is. It contains stable expectations only. Current bills, payments, allocations and balances must be retrieved from Xero during each close.

Do not manually copy live Xero balances into this register. That would create a second ledger and increase the risk of stale totals.

Last verified: **15 September 2026**.

## How the agent must use this register

1. Load this register before reviewing supplier bills or account 620.
2. Select every row marked **Active** whose service period includes the close month, plus every **Ongoing** row.
3. Record the resulting number as `expected_active_supplier_count`.
4. Produce exactly one monthly check result for each selected row.
5. Record the number produced as `completed_active_supplier_count`.
6. If the two counts differ, stop and report **Close not certified**.
7. Search current and recent Xero activity for recurring suppliers or prepayment cycles absent from this register. Report candidates as exceptions; do not invent a supplier rule without checking its source and history.
8. At the end of the close, review the status and coverage of every register row.
9. Move a fixed cycle from **Active** to **Completed** only after its service period has ended, all expected releases are present and its supplier-cycle balance is fully reconciled.
10. If an Ongoing supplier is no longer used, mark it **Retired** only when source evidence or finance confirmation establishes that the relationship or service has ended. One missing monthly bill is not enough evidence.
11. Add a renewal or replacement contract as a new **Active** row with its own source and rules. Do not extend or overwrite the completed source row.
12. Record all register changes in the close output and recalculate the expected active-supplier count for the next close.

An **Active** row has expected activity during its stated service period. An **Ongoing** row has no fixed end date. A **Completed** row is a fully reconciled historical cycle and is excluded from the active count. A **Retired** row is an ended ongoing supplier relationship supported by evidence or finance confirmation. The discovery scan must still identify a new contract or cycle for a Completed or Retired supplier.

## Active monthly checks

| Status | Supplier and source | Process | Service coverage | Expected base or total | Monthly expectation | Expense account | Key supplier rule |
|---|---|---|---|---:|---:|---|---|
| Active | [B PLUS — 3314](https://go.xero.com/AccountsPayable/View.aspx?InvoiceID=b0a9a082-f0fe-4b16-bea8-f0823eaa0ea1) | Equal monthly prepayment release | November 2025–October 2026 | Rs615,325.88 posted to 620 | Rs51,277.16; final October Rs51,277.12 | 500 — Software Subscriptions | Bill on first of service month, month-end due date, release from 620; keep separate subscription renewals separate. |
| Active | [Employers' Federation of Ceylon — 26JUL_TTTT_706331](https://go.xero.com/AccountsPayable/View.aspx?InvoiceID=0bc749db-38c6-410e-9378-0dd51f07c00d) | Equal monthly prepayment release | April 2026–March 2027 | Rs238,500 posted to 620 | Rs19,875 | 412 — Administration Expenses | Exclude separate SSCL and VAT lines from the release; use the corrected recurring schedule and service-month-end clearing from 620. |
| Active | [Fairfirst Insurance — CRFFC2300000310300001](https://go.xero.com/AccountsPayable/View.aspx?InvoiceID=6e14941d-f830-4a98-87f9-30c84a5dacb7) | Equal monthly prepayment release | February 2026–January 2027 | Rs60,539.90 posted to 620 | Rs5,044.99 standard; expected final January Rs5,045.01 if the first eleven months remain Rs5,044.99 | 410 — Insurance | Release only the insurance base; exclude the separate Rs10,897.18 VAT line and close the two-cent rounding difference in the final month. |
| Ongoing | Digital Mobility Solutions Lanka / PickMe | Actual-usage prepayment | Ongoing | Pull current top-ups and available supplier prepayment from Xero | Actual supported monthly usage | 430 | Do not create equal recurring bills. Match the reference and usage description to the service month; date the bill on the first of that month and use month-end as the due date, even when the supplier issues the invoice in the following month. Identify the exact available Xero prepayment object before applying it. |
| Ongoing | Dialog Broadband Services — connection 297190077 | Recurring monthly supplier bill | Ongoing | Per supported supplier invoice | Variable; compare with source and recent history | Verify against current-cycle history | Bill date normally first of service month and due at month-end; reference, description, connection and attachment must identify the same service month. Do not copy the unexplained March 2026 date outlier. |

The active count as at 15 September 2026 is **5**. The agent must recalculate it from the status and service coverage for every future close.

## Completed cycles retained for reference

| Status | Supplier and completed source | Completed coverage | Completed base | Historical monthly treatment | Future-cycle rule |
|---|---|---|---:|---:|---|
| Completed | [Exterminators PLC — 26AUG/EPLC38628](https://go.xero.com/AccountsPayable/View.aspx?InvoiceID=9d762b90-6176-4bca-bdcf-962f572ae7c2) | June–August 2026 | Rs41,638 | Rs13,879.33, Rs13,879.33 and final Rs13,879.34 to 420 | The cycle is fully released. If a new annual or periodic invoice appears, verify the new base, VAT separation and coverage and add a separate Active row. |
| Completed | [Cemex Biostar — CMX/2025/08/0081](https://go.xero.com/AccountsPayable/View.aspx?InvoiceID=56980254-9ca4-4a14-aa2c-66b9de858bbf) | May–August 2026 | Rs46,458.57 | Rs11,614.64 for May–July and final Rs11,614.65 to 500 | The cycle is fully released. Do not create more months unless a new supported cycle exists. |
| Completed | Secretaries Colombo — 1352 | June 2025–May 2026 | Rs96,000 | Rs8,000 to 412 | The cycle is fully released. Add a supported renewal as a new row and use 412 unless finance expressly approves a prospective reclassification to 433. |
| Completed | Secretaries Colombo — 1161 | June 2024–May 2025 | Rs96,000 | Rs8,000 to 412 | Historical cycle only; do not recreate or reactivate it. |

## Required monthly result

The close package must contain this table with one row for every supplier selected from the active checks:

| Close month | Supplier/source | Expected activity | Actual Xero activity | Amount variance | Status | Evidence/link | Required action |
|---|---|---|---|---:|---|---|---|
|  |  |  |  |  |  |  |  |

Then record:

```yaml
expected_active_supplier_count:
completed_active_supplier_count:
unregistered_supplier_candidates:
supplier_register_completeness: PASS_OR_FAIL
supplier_register_changes:
next_close_expected_active_supplier_count:
```

`supplier_register_completeness` is `PASS` only when the expected and completed counts match, every unregistered candidate has been classified or raised as an exception, all completed or ended cycles have the correct status, and the next close's active count has been recalculated.

## Register maintenance

Update this register during every monthly close when evidence establishes a new, completed, retired or changed supplier cycle. Record the source invoice or contract, service coverage, amount posted to account 620 where relevant, expected monthly method, expense account, supplier-specific rule and status change.

Do not replace a prior row silently. Move a fully reconciled fixed cycle to **Completed** and add a new source as a separate row so the historical basis remains visible. Mark an Ongoing supplier **Retired** only with evidence or finance confirmation; do not infer retirement from inactivity alone.
