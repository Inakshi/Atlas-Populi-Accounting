# Verified examples and exceptions

Review date: 11 September 2026. These are sampled controls and exceptions, not a complete audit.

## Verified transaction examples

### Franks rent

The March payment comprises two bills:

- Phase 1: Rs1,566,830.77.
- Phase 2: Rs382,153.84.
- Combined: Rs1,948,984.61, matching PV BP003.

The April rent has the same combined amount but a different payment date. Amount alone cannot identify the correct match.

### Cubicoan SINV-03001

- Expense: Rs53,410 to account 459 — Industrial Components.
- VAT Input: Rs9,613.80 to account 314.
- Bill total: Rs63,023.80.
- Active payments: Rs31,511.90 on 22 April and Rs31,511.90 on 7 May.
- A deleted Rs63,023.80 payment remains in history and must be excluded.

The live bill date is 19 May, later than both payment dates. This chronology needs source-invoice verification before it is called an error.

### May payroll

The Xero record is one bill with four Department lines and four active payments:

- Rs471,120
- Rs1,606,420.48
- Rs1,614,300
- Rs1,248,860

Total: Rs4,940,700.48, matching PV BP034. The training transcript's reference to “four bills” is imprecise.

### Multi-row voucher examples

- BP009: Rs61,832 + Rs18,290 = Rs80,122; the paid amount appears once.
- BP020: Rs2,200 + Rs2,200 = Rs4,400; the paid amount appears once.

### Dialog connection 297190077

Recent established pattern:

| Service month | Bill date | Due date | Description month | Total LKR |
|---|---:|---:|---|---:|
| March 2026 | 31 March | 14 April | March | 282,197.96 |
| April 2026 | 1 April | 30 April | April | 282,197.96 |
| May 2026 | 1 May | 31 May | May | 282,197.96 |
| June 2026 | 1 June | 30 June | June after correction | 282,197.96 |
| July 2026 | 1 July | 31 July | July | 282,199.56 |
| August 2026 | 1 August | 31 August | August | 282,199.56 |

The June bill originally described July, while a separate July bill already existed. The user confirmed June was correct. Both line descriptions were corrected to June on 11 September 2026 and read back from Xero. Date, due date, reference, amount, accounts, tax treatment and Department were unchanged. The attachment remains named **Atlas - 297190077 - July.pdf** and still needs source-document verification.

March remains a date/due-date outlier relative to April onward. Confirm whether the first-of-month convention was introduced from April before changing historical records.

## Tracker and system exceptions

### May 2026 PV dashboard formulas

- E2 sums K76:K124 even though the inspected entries occupy rows 7:75; result is 0.
- G2 calculates MAX(K76:K222); result is 0 for the visible population.
- F2 refers to missing sheet **April 2025** and returns #REF!.

The dashboard should not be used as evidence of May totals until the intended ranges and prior-period comparison are confirmed and repaired.

### Cost-code imports

- Project 203 source code is valid and Active, but its central IMPORTRANGE is disconnected.
- The central Database query returns #REF! rows and combines a limited named set of tabs.
- The PV CostCodes sheet contains a broken import and fixed import ranges.

Do not assume every active project code is available downstream. A complete dependency audit is still required before formulas are rewritten.

### Project register

The latest named tab observed was FY25/26 even though it includes the project used in June 2026 training. Some ownership cells are blank. Confirm the current register and its maintenance owner before treating the tab as complete.

### Bank dashboard snapshot

At the 11 September 2026 snapshot:

- LKR Commercial showed 60 items to reconcile.
- USD Union showed 10 items.
- LKR Union showed 10 items.
- USD Commercial was marked reconciled, with a displayed statement date of 26 April.
- The latest displayed LKR Commercial/Union and USD Union statement date was 31 August.

These counts are a snapshot, not proof of errors or lateness.

### Petty-cash snapshot

Xero displayed Rs185,126.11 and a statement balance of negative Rs12,363,851.74 dated 23 June. The dates/cutoffs are not aligned, so the difference does not prove missing cash. It confirms that an opening-balance bridge and common-cutoff reconciliation are needed before certifying the account.
