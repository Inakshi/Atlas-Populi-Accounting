# Grokbot awaiting-payment settlement runbook

## Purpose

This is a copy-ready execution brief for Grokbot. It covers the Atlas Populi supplier bills for which the payment voucher and a live Commercial Bank statement debit agreed during the review on **15 September 2026**.

The evidence below identifies candidates for settlement. It does not override the final live checks or reviewer approval. Grokbot must fail closed: if any field differs, do not pay, allocate, reconcile, write off, void or edit the affected item.

## Copy-ready instruction for Grokbot

You are working in the Xero organisation **Atlas Populi (Private) Limited**, country LK, base currency LKR. Your task is to prepare and, only after my review and approval, settle the exact supported bills in this instruction.

Use these source workbooks:

- [Payment vouchers: FY 2026/27](https://docs.google.com/spreadsheets/d/1IBU0-BH4IXI6G4n8jqXH-g6msIXNQXYTwMHeZccwsoM/edit?gid=427450684#gid=427450684)
- [Payment vouchers: FY 2025/26](https://docs.google.com/spreadsheets/d/10hUXY-m_CRmYDEUmAjOIFi4psDtpi6x-CqDA80kEI34/edit?gid=800643728#gid=800643728)

### Non-negotiable rules

1. Confirm the Xero organisation name and LKR base currency before doing anything else. Stop if they differ.
2. Refresh every bill, payment, credit and bank statement line immediately before proposing or making a change.
3. Treat a settlement as exact only when all applicable fields agree:
   - supplier or supported payee;
   - active Xero bill ID and reference;
   - service period;
   - amount currently due;
   - payment-voucher number, date and paid amount;
   - procurement or bank reference where one exists;
   - Commercial Bank statement date and debit amount;
   - no active payment or allocation already records the same cash.
4. Never match on amount alone. Repeated supplier amounts must also agree by date, reference and service period.
5. Exclude voided, deleted or reversed payments and allocations. Check the bill's active payment history for duplicates.
6. Do not create a second payment when a matching payment already exists. Reconcile the statement line to the existing payment.
7. For an unpaid bill with an unreconciled statement debit, start from **100 — LKR Account: Commercial Bank** and use Xero **Find & Match**. Select only the bill or bills identified below. The selected total must equal the bank statement debit to the cent.
8. For a compound payment, select all and only the specified bills in one Find & Match result. Do not record the full bank debit separately on each bill.
9. If the Xero workflow requires the bill's **Make a payment** form instead, use:
   - amount: the exact supported amount;
   - date paid: the bank statement date;
   - paid from: **100 — LKR Account: Commercial Bank**;
   - reference: the payment-voucher number.
   Then match that payment to the existing statement line. Do not use both methods to create two payments.
10. Do not write off, void, delete, change a bill, change its account, or use another bank or clearing account as part of this task.
11. Before posting anything, open every qualified bill below in its own Xero tab in AWP order. Keep the tabs open for me. Present a proposed-action table containing AWP ID, supplier, bill reference, amount due, bank date, bank reference, bank amount, voucher number, intended Xero action and expected amount due after settlement.
12. Ask for one explicit approval covering the exact proposed-action table. Do not treat access to Xero or this instruction as approval to post if the live values have changed.
13. After approval, complete one payment group at a time. Read back the bill status, amount due, payment or allocation amount, date, account, reference, Xero transaction ID/link and bank-line reconciliation status before continuing.
14. If a group fails readback, stop the related work. Do not continue through the batch while an unexplained difference remains.

### Already paid: reconcile only

Do not add another payment to this bill:

| ID | Bill | Verified state | Required action |
|---|---|---|---|
| AWP-005 | [Frankils security charges — BP005/06/2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=365a1a17-70d1-415f-8345-d6f89ff2ce21) | Paid in full: two active payments of LKR 271,537.50 dated 2 Jun and 5 Aug 2026; amount due LKR 0.00. The second payment transaction ID is `b8e91e2d-85fc-452b-b163-bf5b938afbf0`. | If the 5 Aug 2026 Commercial Bank debit `GF-4973` for LKR 271,537.50 is still unreconciled, match it to the existing second payment. Do not create or record another payment. |

### Exact live-bank candidates to prepare for approval

The following candidate set contained **26 open bills**, with a combined Xero amount due of **LKR 6,846,328.73**. The supported cash debits total **LKR 6,845,432.93**; the remaining **LKR 895.80** relates only to the Dialog credit described in the AWP-058 row.

Every bank line listed here was visible in Xero's imported statement for **100 — LKR Account: Commercial Bank** and was marked unreconciled during the 15 September review. Reconfirm that status before action.

| AWP ID(s) | Bill(s) and amount due | Voucher | Exact Commercial Bank debit | Required Xero treatment |
|---|---|---|---|---|
| AWP-026, AWP-027 | [Frankils March Phase 2 electricity — LKR 116,005.48](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=0e186332-daaa-41cc-a498-e35ba5045ce7); [Phase 1 — LKR 535,961.78](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=9105eb57-af91-49ac-8746-e3702ee3526f). Total LKR 651,967.26. | BP016/08/2026 | 14 Aug 2026; `GF-5109`; LKR 651,967.26 | Find & Match both bills to the one debit. |
| AWP-035, AWP-036 | [Frankils June Phase 1 rent — LKR 1,566,830.77](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=236e8652-d82c-41c3-82b5-fcb4e67995fb); [Phase 2 — LKR 382,153.84](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=f72f6da3-e91c-40ac-80f6-412ae5d0e8e5). Total LKR 1,948,984.61. | BP008/08/2026 | 10 Aug 2026; `GF-5100`; LKR 1,948,984.61 | Find & Match both bills to the one debit. |
| AWP-037 | [Dialog Broadband 114775452 — June 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=d482e091-7a6b-4b84-88e8-f915c4d9f6bb), LKR 9,929.41 | BP009/08/2026 | 10 Aug 2026; `IB-BIL 114775452 DIALOG_DBN`; LKR 9,929.41 | Match this bill only. |
| AWP-038 | [Sri Lanka Telecom — June 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=fffdaf84-ec2e-4975-9405-12cc34443349), LKR 9,630.71 | BP021/08/2026 | 14 Aug 2026; `IB-BIL 0029658572 SLT_ACCOUNT`; LKR 9,630.71 | Match this bill only. |
| AWP-041 | [Access Natural Water — June 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=007f474d-361f-430c-b558-bfa6ede9d854), LKR 36,057.86 | BP008/07/2026 | 8 Jul 2026; `INV-9194`; LKR 36,057.86 | Match this bill only. The voucher tracker showed Xero=`No`; report that field for correction after settlement, but do not edit the sheet unless separately authorised. |
| AWP-042 | [Management Corporation — WEG_82545](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=7fc63515-7cf5-41d6-b7dc-5fc36be4114d), LKR 82,685.73 | BP024/08/2026 | 21 Aug 2026; `GF-5161`; LKR 82,685.73 | Match this bill only. |
| AWP-043 | [Indu — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=d541720a-0272-43c7-80bf-d4d2f79ec283), LKR 70,000.00 | BP003/08/2026 | 3 Aug 2026; `GF-5153`; LKR 70,000.00 | Match this bill only. |
| AWP-044 | [Care Well — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=208a792e-c5b0-4616-82a0-569042794ef5), LKR 46,000.00 | BP005/08/2026 | 5 Aug 2026; `GF-5152`; LKR 46,000.00 | Match this bill only. |
| AWP-046 | [Russel's — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=45d0d81d-6baa-4869-b124-08bcdfaee547), LKR 198,146.80 | BP018/08/2026 | 14 Aug 2026; `/GF-5157`; LKR 198,146.80 | Match this bill only. |
| AWP-047, AWP-048 | [Frankils July Phase 1 rent — LKR 1,566,830.77](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=716237b7-39d4-450f-a1ba-b0dd0c83b4b3); [Phase 2 — LKR 382,153.84](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=1d955be7-0fb4-4d85-9dce-565927495baf). Total LKR 1,948,984.61. | BP023/08/2026 | 21 Aug 2026; `GF-5151`; LKR 1,948,984.61 | Find & Match both bills to the one debit. Do not use the equal-value 10 Aug debit for this July group. |
| AWP-049 | [Top Care — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=9626ac80-4ace-4133-9dfe-9f622a443981), LKR 87,450.00 | BP015/08/2026 | 14 Aug 2026; `GF-5162`; LKR 87,450.00 | Match this bill only. |
| AWP-051 | [National Water Supply — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=27ed7ca5-2741-4ff3-aaa3-9fe8b3aa9e4e), LKR 9,510.80 | BP010/08/2026 | 10 Aug 2026; `IB-BIL 10/14/112/065/15 WATER_`; LKR 9,510.80 | Match this bill only. |
| AWP-055 | [Fardar Express — CLC2026018498](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=b5b48acb-3e46-4b6e-b64b-447fa69e30a0), LKR 30,000.00 | BP017/08/2026 | 14 Aug 2026; `NV-9254`; LKR 30,000.00 | Match this bill only after the supplier and invoice reference agree to the voucher. |
| AWP-057 | [Dialog Axiata PR52444729 — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=dc567b89-3a60-4b6c-b216-8f7e1a6330b7), LKR 8,288.02 | BP013/08/2026 | 10 Aug 2026; `GF-5159`; LKR 8,288.02 | Match this bill only. |
| AWP-058 with AWP-039 credit | [Dialog Axiata PR108866005 — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=b939294d-1ec8-493a-bc49-e8e7363b94b5), LKR 6,846.66; [Dialog overpayment BP008/06/2026](https://go.xero.com/app/!cDZ-!/bills/view/credit-note?id=869852bc-66f6-4772-949b-a9338cd77781), LKR 895.80 | BP012/08/2026 supports cash of LKR 5,950.86 | 10 Aug 2026; `GF-5160`; LKR 5,950.86 | First confirm the LKR 895.80 supplier credit is still active, belongs to the same Dialog contact and is not allocated elsewhere. Apply exactly LKR 895.80 to AWP-058 and match exactly LKR 5,950.86 cash. The two active allocations must total LKR 6,846.66. If the credit cannot be proved live, leave this entire case unposted. |
| AWP-061 | [APIT — July 2026](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=ebadd51a-8392-43f2-bfa7-9a2c1cad3057), LKR 81,694.74 | BP020/08/2026 | 14 Aug 2026; `IRD_SELF10106576632627 IRD_PAY`; LKR 81,694.74 | Match this bill only. Confirm the tax period is July 2026. |
| AWP-062 | [Rubteco — 26JUL_RUAE_000194](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=8297369d-b9c2-4ebc-91cc-0b2e2c05d7cf), LKR 46,233.45 | BP014/08/2026 | 14 Aug 2026; `INV-9113`; LKR 46,233.45 | Match this bill only. |
| AWP-063 | [Access Natural Water — 26JUL_FGDI_713170](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=a650f76a-09a6-4b84-b0b9-9b5d6baeb448), LKR 29,215.62 | BP019/08/2026 | 14 Aug 2026; `INV-9278`; LKR 29,215.62 | Match this bill only. |
| AWP-064, AWP-082, AWP-085 | [Malika consultancy — LKR 213,290.32](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=5ad86801-aa2d-4c98-8254-3852111ed9be); [Laknadi consultancy — LKR 49,560.00](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=ed2dcac7-eedd-4c8a-b1c3-86c9327bbfbb); [Independent Contractors — LKR 1,183,569.29](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=8f8f4d05-5bdd-4be8-b999-16ddbcf2f758). Total LKR 1,446,419.61. | FY26/27 August voucher rows 33–35; re-read the shared batch/voucher identifier before approval | 31 Aug 2026; `1 SALAUG2026`; LKR 1,446,419.61 | Find & Match these three bills as one batch. Confirm the three current due amounts still sum to the statement debit before posting. |
| AWP-069 | [Printers.lk — 25-200-002799](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=0250f6dc-bb53-4d41-8c36-f0b4191c672a), LKR 49,150.00 | BP004/08/2026 | 5 Aug 2026; `INV-9236`; LKR 49,150.00 | Match this bill only. |
| AWP-073 | [Exterminators — 26AUG/EPLC38628](https://go.xero.com/app/!cDZ-!/bills/view/bill?id=9d762b90-6176-4bca-bdcf-962f572ae7c2), LKR 49,132.84 | BP025/08/2026 | 21 Aug 2026; `INV-8819`; LKR 49,132.84 | Match this supplier cash bill only. It is separate from the account-620 monthly prepayment-release bills. |

### Do not include without further evidence

- **AWP-009 — Dialog Axiata June 2025, LKR 1,384.15:** the exact Commercial Bank debit was subsequently verified in Xero on 24 July 2025 with reference `BP043/07/2025`, amount LKR 1,384.15, and status Reconciled. It was recorded as a Dialog overpayment and then fully allocated to **AWP-010 — Dialog July 2025**. The voucher and overpayment description identify June service for mobile number 0743450707, so this is a confirmed cross-month misallocation. Do not create another payment. Remove the LKR 1,384.15 allocation from AWP-010 and apply that same credit to AWP-009 using 24 July 2025, but only as a separately reviewed correction. After removal, AWP-010 will show LKR 1,384.24 due unless separate exact July evidence is found; do not write off its current LKR 0.09 balance first.
- **AWP-023 — EPF January 2026:** voucher supplier conflicts with the Xero supplier.
- **AWP-088 — CameraLK:** payment predates the Xero bill and source chronology remains unresolved.
- **AWP-081 — August payroll:** only a partial payment is supported and LKR 39,400.00 remains unexplained.
- Any bill or credit not listed in the exact candidate table.
- Any item whose current live state no longer matches this instruction.

Do not write off any old balance as part of this exercise.

### Required readback report

After each approved group, report:

| AWP ID(s) | Bill status | Amount due after | Payment/allocation date | Paid from | Payment or credit amount | Voucher/reference | Xero transaction link | Bank line status | Result |
|---|---|---:|---|---|---:|---|---|---|---|
|  |  |  |  |  |  |  |  |  |  |

Use `FIXED_VERIFIED` only when both the Xero bill readback and the bank-line reconciliation readback agree. Otherwise use `FAIL` or `BLOCKED`, describe the exact difference and stop the affected group.

## Control note

The live bank evidence in this document is a 15 September 2026 snapshot. It supports the proposed records, but Grokbot must still refresh every record because another user or agent may have posted a payment or reconciliation since that review.
