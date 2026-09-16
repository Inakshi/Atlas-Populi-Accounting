# Consultancy invoice check

## Purpose

Monthly process for verifying the consultancy invoices submitted by independent contractors
(data labellers and shift managers), recording the outcome in the invoice tracker, and filing the
approved invoices.

It converts a manual review into a repeatable control sequence with one defined outcome per
contractor per month, an explicit reason recorded against every rejection, and a reconciliation
between what was approved and what was filed.

> **Scope note.** This document describes the *process only*. It deliberately contains no
> contractor names, bank details, amounts, employee numbers, email addresses, or file identifiers.
> Those live in the internal working copy and must never be committed to this repository or
> published anywhere else. Where an example is needed, the values below are fabricated.

---

## 1. What the process does

Each month a group of independent contractors (data labellers and shift managers) email an invoice
for their work. For each one:

1. Determine the invoice month and the period it covers (§2).
2. Find the invoice in the mailbox.
3. Check it against Finance's own calculation of what that person should be paid.
4. Record the outcome in the tracker, and where something is wrong, record exactly what.
5. File the approved invoices in the document store.

**Finance's calculation is never modified by this process — it is read-only.**
**Contractors are never contacted as part of this process.** Any follow-up is done by the
finance owner personally.

---

## 2. Working out the month

> **The pay period runs from the 25th of the previous month to the 24th of the invoice month.**

The **invoice month** is the month the period *ends* in. That name is used consistently for the
fee computation file, the tracker tab, the folder and the filed document.

```
Invoice month = M

  Period starts:   25th of the month before M
  Period ends:     24th of M
  Invoices arrive: from about the 25th of M through the first ~10 days of the month after M
```

The dates are always the 25th and the 24th. They do not shift for month length, weekends or public
holidays. February is no different; there is no leap-year complication.

### 2.1 Year rollover

January is the exception to watch. A January invoice covers **25 December of the previous year →
24 January**, so the start date falls in a different year from the invoice month. January also
belongs to the new year's tracker file, while December belongs to the old one, and the two are
processed only weeks apart.

```
given invoice month M and year Y:

    end_date   = 24 / M / Y
    start_date = 25 / (M - 1) / Y

    if M == January:
        start_date = 25 / December / (Y - 1)
```

### 2.2 Confirm, don't assume

Compute the period so you know what to expect, **but the fee computation file is the authority** —
its overview tab states the period for the month. If the computed period and the stated period
disagree, **stop and escalate**. Do not proceed on either version.

### 2.3 Which month is being processed

Normally it is the month that has just ended on the 24th. Running in early October means the
September cycle. If it is ambiguous, or the previous month still has unfinished rows, ask rather
than guess.

---

## 3. The three outcomes

Every contractor ends each month with exactly one result:

| Result | Meaning | Received | Date Received | Notes |
|---|---|---|---|---|
| **Yes** | Invoice arrived and everything is correct | `Yes` | date the email arrived | blank |
| **No** | No invoice arrived at all | `No` | blank | **blank — never a note** |
| **N/A** | Invoice arrived but something is wrong | `N/A` | date the email arrived | **what is wrong** |

These are not the obvious readings, so they are worth restating:

- **`No` is about arrival, not correctness.** It means nothing came. A `No` row never carries a note,
  because there is nothing to explain.
- **`N/A` is the "there is a problem" answer.** The invoice did arrive, so it still gets a date, and
  the note **must** say what is wrong.
- **`Yes` requires all checks to pass.** Never mark `Yes` on a partial match.

If anything does not match, the answer is `N/A` plus a note. That is the correct and useful
outcome, not a failure of the process.

### 3.1 Standing exemptions

A small number of contractors are not expected to invoice at all. They are marked `No` every month
with no note, and are never chased or reported as missing. Because `No` counts toward the Pending
figure, a fully completed month will show a Pending count equal to the number of these exempt
contractors — not zero.

---

## 4. Where the inputs and outputs live

Everything is named after the invoice month. Work out the month first, then locate each item **by
name**. Do not rely on stored file identifiers — a new fee computation file is created every month
and a new tracker file every calendar year.

| Item | How to find it |
|---|---|
| Invoices | A dedicated mailbox label, searched by label name |
| Finance's numbers | `Fee Computation for Independent Contractors for Month of <Month> <Year>` |
| Tracker | `Consultancy Invoices Tracker <Year>`, one tab per invoice month |
| Filed invoices | `<Month> <Year>` / `Consultancy Invoices - <Month> <Year>` / `<Name> - <Month> <Year>.pdf` |

**Tracker tab names use the full month name** — `August 2026`, never `Aug 2026`.

Tracker columns:

| Column | Heading | Contents |
|---|---|---|
| A | Employee Number | pre-filled |
| B | Name | pre-filled |
| C | `Recieved` *(the sheet's own spelling)* | dropdown: `Yes` / `No` / `N/A` |
| D | `Date Received` | date the invoice email arrived |
| E | `Notes` | what is wrong, whenever C is `N/A` |
| F, G | Yes / N/A / Total / Pending counters | formulas — never type into these |

Header is row 1; contractors start at row 2. `Pending = Total − (Yes + N/A)`.

If the month's fee computation file does not exist yet, the numbers are not ready — stop and say so
rather than checking against the previous month's figures.

---

## 5. Reading the fee computation file

### 5.1 It contains more than one table

The contractors tab holds **several stacked tables**, not one. The first covers monthly-fee
contractors. Further down, past the New Recruits / Resignees / Addendums summaries, there is a
second block for **hourly (zero-hour) consultants** with its own identical header row.

Two column headings differ in the hourly block:

| Monthly block | Hourly block |
|---|---|
| `Shift Rate` | `Rate Per Hour` |
| `No. of Extra Shifts` | `No. of Hours (Extra Shifts)` |

Everything else, including the net pay and bank columns, sits in the same position and is read the
same way.

**If a contractor is not in the first table, search the whole tab before concluding they are
missing.** Matching on employee number is the reliable way; names are spelled inconsistently
across sources.

### 5.2 The figure that matters

**The invoice must match the final net pay column — the one after tax is deducted**
(`Net Pay = Gross Pay − WHT Amount`).

It is easy to pick the wrong column. Do not use the total salary, the gross pay, or the pre-tax net
pay. Comparing against the wrong column will reject correct invoices.

### 5.3 Role titles in the hourly block

In the hourly block the role title can sit in the contract-type column while the designation column
holds a more general one. An invoice matching **either** is acceptable — do not fail a designation
check on that basis.

---

## 6. The checks

| # | Check | Compared against |
|---|---|---|
| 1 | Period | the period for the invoice month (§2) |
| 2 | Amount | the final net pay column (§5.2) |
| 3 | Name | the contractor's name |
| 4 | Designation | the designation column |
| 5 | Bank details — account name, account number, bank, branch | the four bank columns, **all four** |
| 6 | Signature | must be present |

### 6.1 Differences that are acceptable

- Full legal name on the invoice versus the short name in the records.
- A missing shift qualifier — e.g. the role without its "(Night shift)" suffix.
- Spelling variants of the same role.
- A bank's common abbreviation versus its full registered name.
- A branch name with or without the word "Branch", or a minor spelling variant.
- A leading zero on an account number.
- Either the contract-type or designation string matching, in the hourly block (§5.3).

### 6.2 Differences that are not acceptable

- Any difference in the amount, however small.
- Wrong period dates — including the right shape with the wrong month.
- An account number differing by even one digit.
- A different bank or a genuinely different branch.
- A missing signature.
- A different person's name, or a genuinely different role.

### 6.3 The date printed on the invoice is not a check

Contractors frequently write the document date in the wrong format or with the wrong month. **This
is not a defect and must never be flagged.** Never fail an invoice over its printed date and never
write a note about it. What is recorded in `Date Received` is the date the *email* arrived, which is
unrelated to what the document says.

### 6.4 Checking the period carefully

This is the most frequently wrong field, because contractors copy the previous month's invoice and
forget to change the dates. Check **both ends and both months**, and both years — especially in
January. A common failure is the correct 25th–24th shape applied to the wrong month; read the
actual month names rather than pattern-matching the format.

### 6.5 Checking the signature properly

The signature is an **image or a vector drawing, not text**. Extracting the text alone will show the
word "Signature" — the template's caption — whether or not anyone actually signed.

**The rendered page must be inspected**, or the presence of a drawing or embedded image beside the
caption confirmed. Note that some signatures are vector paths carrying **no embedded image at all**,
so an image-only test will produce false negatives. An invoice with the caption and nothing beside
it is unsigned.

---

## 7. Dates and time zone

The tracker records the date the email arrived **in local time (UTC+5:30)**. Most mail tooling
reports timestamps in **UTC**, so the value must be converted before it is written.

- Anything arriving between **18:30 and 24:00 UTC rolls over to the next local day.**
- This means an invoice for one month can legitimately carry a Date Received in the following
  month. That is correct: the tab is the invoice month, the date is when it arrived.

**Resends:** where a thread contains several messages, always use the **latest** — its date and its
attachment.

**Writing the date:** the tracker displays `DD/MM/YYYY`. To remove any ambiguity about how a typed
date will be parsed, **enter it in longhand** (e.g. `1 September 2026`) and let the sheet format it,
then read the cell back to confirm.

---

## 8. Recording a problem

When a check fails:

- `Recieved` = `N/A`
- `Date Received` = the date the invoice arrived — it did arrive, so it still gets a date
- `Notes` = a short, specific reason

**Every `N/A` must have a note.** An `N/A` with an empty note is useless: it forces the reader back
to the document, which defeats the purpose of the check. **No `No` row ever has a note.**

### 8.1 Wording the note

One line. State **what was found** and **what it should be**, so the reader can act without opening
the invoice. Fabricated examples of the form:

| Problem | Note |
|---|---|
| Wrong amount | `Amount Rs 12,345.00, should be Rs 12,345.67` |
| Wrong period | `Period 25/07-24/08, should be 25/06-24/07` |
| Period shape wrong | `Period 24/07-24/08, should be 25/07-24/08` |
| Account number mismatch | `Account no. does not match records` |
| Account number missing | `Account number not given on invoice` |
| Wrong bank or branch | `Bank does not match records` |
| Not signed | `Not signed` |
| Name mismatch | `Name on invoice does not match records` |
| Wrong designation | `Designation shown as <X>, records show <Y>` |
| More than one problem | join with `; ` |

Rules for the text:

- State actual figures and dates where they are the point of the note.
- Keep it to roughly 100 characters.
- Plain English; no invented codes or abbreviations.
- Describe the document, never the person.

> **Exception for bank details.** Do not write a full account number into the tracker note. Record
> that the bank details do not match and escalate the specifics directly — see §10.

### 8.2 After marking `N/A`

Chasing the contractor is **not part of this process and is not automated.** The finance owner
emails the contractor personally. Do not write, draft, or send that message, and do not contact the
contractor in any way.

The tasks when an invoice fails are exactly three:

1. Mark `N/A`, fill in the date, write the reason in the note.
2. **Do not file the document** (§9).
3. Include the failure in the report so the finance owner knows who to contact.

Then stop.

### 8.3 When a corrected invoice arrives

The contractor replies with a corrected invoice, usually on the original thread. Picking that up is
part of the process — do a **second pass** a few days after the first:

1. Re-check the mailbox for a newer message from everyone marked `N/A`.
2. Download the **new** attachment and **re-run every check from scratch.** Do not assume only the
   flagged item changed.
3. **If it now passes:** set `Yes`, update the date to the **new** email's date, **clear the note**,
   and **file the document now** — this is the first and only time it is filed for that month.
4. **If it is still wrong:** leave it as `N/A` and **replace** the note with what is wrong now. Do
   not stack old reasons. Still do not file it. Report it again.
5. **If nothing has arrived:** leave the row as is and say so. Do not chase.

---

## 9. Filing the approved invoices

**Only invoices marked `Yes` are filed.** A rejected invoice is never filed — it waits for the
corrected version. The document store therefore holds exactly one clean, correct invoice per
contractor per month and nothing else.

Create the month's subfolder if it does not exist; that is the one item this process may create
without asking.

**Reconcile at the end: the number of filed documents must equal the number of `Yes` rows.** This
is the check most likely to catch a quiet omission — for example a contractor added to the tracker
after the filing pass had already run.

If something is filed by mistake, report it rather than quietly deleting it.

---

## 10. Escalate rather than decide

Stop and raise with the finance owner when:

1. **Any bank detail differs from the records.** Mark `N/A`, note that the details do not match, and
   raise the specifics directly. **Never "correct" a bank detail, and never pay against an account
   number that differs from the records.** A changed account number is a fraud-relevant signal.
2. **Any outbound message is involved.** Nothing is sent or drafted to a contractor by this process.
3. **A structural change to a sheet is needed** beyond adding a joiner or removing a resignee.
4. **Anything would require editing the fee computation file.** It is read-only, always.
5. **The month's fee computation file or tracker tab does not exist yet.**
6. **The stated period disagrees with the computed period** (§2.2).
7. **A person appears in one source but not the other**, after searching every table (§5.1).
8. **Anything is unclear.** An unanswered question is cheap; a wrong `Yes` is not.

---

## 11. Order of work

1. Work out the invoice month and period; confirm against the fee computation file.
2. Locate this month's fee computation file, tracker tab and destination folder.
3. Handle leavers (remove) and joiners (add, formatted) — §12.
4. Collect the invoices from the mailbox label; latest message per thread.
5. Extract each document; run the checks; **inspect the signature**.
6. Fill the tracker: the outcome column, then dates, then notes.
7. File the approved documents; **reconcile the count against the `Yes` rows**.
8. Report — failures and missing invoices first, then the rest.
9. Second pass a few days later for corrected resends (§8.3).

---

## 12. Joiners and leavers

### 12.1 Leavers

The fee computation file lists contractors whose contracts ended during the period.

1. **Check the mailbox first** — some leavers still invoice for their final part-month.
2. If they invoiced, process it normally.
3. If they did not, **delete their row from this month's tab.** They have left; they are not
   "pending", and leaving the row makes the month look permanently incomplete.
4. **Do not carry them into later months.** Once someone leaves in month M they do not appear in
   M+1 onwards.

Delete the row itself, not just its contents — an empty row still counts toward the totals.

> Removing someone from the invoice tracker records only that no invoice is expected. It does not
> settle any final payment still owed to them; that is tracked separately.

### 12.2 Joiners

New contractors appear in the fee computation file before the tracker has a row. **Add the row** —
do not leave them off.

The new row must **match the existing rows exactly**, not be plain text:

1. Enter the employee number and name.
2. Copy a complete existing row, select the new row, and **paste formatting only**.
3. Repeat with **paste data validation only**, so the outcome column gets its dropdown — or extend
   the existing validation rule's range to cover the new rows, which preserves the exact colours.
4. Confirm the new row looks identical to its neighbours before entering any data.

A row of left-aligned plain text with no dropdown is not acceptable.

**Joiners legitimately bill a part period.** Someone who started mid-period invoices from their
start date to the 24th, not from the 25th. That is correct and must not be marked as a failure —
the fee computation prorates to match. Check the **amount**, which is the real test.

---

## 13. Implementation notes

Adapt these to whatever tooling is in use; the process above is what matters.

### 13.1 Extracting the attachment

Some mail connectors expose attachment *metadata* but provide no way to download the file. Where
that is the case, fetch the **raw MIME** of the message and extract the attachment directly:

```python
import json, base64, email, os

raw  = json.load(open(RAW_MESSAGE_PATH))['raw']      # base64url-encoded MIME
mime = base64.urlsafe_b64decode(raw + '=' * (-len(raw) % 4))
msg  = email.message_from_bytes(mime)

for part in msg.walk():
    filename = part.get_filename()
    if filename:
        with open(os.path.join(SCRATCH_DIR, filename), 'wb') as fh:
            fh.write(part.get_payload(decode=True))
```

Read the document for **text and image content both**:

```python
import fitz                                   # pip install pymupdf

doc  = fitz.open(PDF_PATH)
page = doc[0]

print(page.get_text())                        # the words
print(page.get_images(full=True))             # raster signatures appear here
print(len(page.get_drawings()))               # vector signatures appear here
page.get_pixmap(dpi=110).save('page1.png')    # render and inspect
```

Some contractors send `.docx` rather than PDF. Unzip the file and read `word/document.xml` for the
text; `word/media/` holds the signature image.

### 13.2 Writing to the tracker

Where no spreadsheet write API is available, the tracker has to be driven through the browser. The
following failures have all occurred in practice:

- **Blank lines do not skip a row.** Typing a run of values separated by newlines, with empty lines
  intended to leave rows untouched, silently shifts everything below upward. The result looks
  plausible and is wrong. **Only bulk-enter contiguous runs with no gaps** — delete unwanted rows
  *first* so the column is gapless, then enter it in one pass.
- **Keyboard navigation drops and lags.** Repeated arrow keys may register once, or three times.
  **Re-read the cell reference before every entry** rather than trusting the key count.
- **Screen coordinates drift** as the viewport rescales between screenshots, and clicking the cell
  reference box is unreliable. Click the target cell in the grid and verify before typing.
- **A mis-click can silently change a dropdown value** in a neighbouring row. Verify the cell
  reference before and the value after.
- **If a typed dropdown value is rejected**, open the dropdown and select the option instead.
- **Work alone in the sheet.** If anyone else — person or automation — is editing the same tab,
  stop. Concurrent writes misalign each other's rows.

### 13.3 Filing

Do not attempt to upload a document by inlining it as base64 text; a typical invoice is around
200,000 characters encoded. Save the attachment through the mail client's own "add to document
store" action, then rename and move it, confirming identity by matching the **byte size** against
the extracted copy.

---

## 14. Worked example — a pass

*All values below are fabricated.*

Period for the invoice month: **25 Jul → 24 Aug**. Confirmed against the fee computation file.

| Check | Invoice | Records | Result |
|---|---|---|---|
| Period | 25th July to 24th August | 25-07 → 24-08 | pass |
| Amount | Rs 12,345.67 | 12,345.67 | pass |
| Name | full legal name | short name | pass — same person |
| Designation | role without shift qualifier | role with qualifier | pass |
| Bank details | all four fields | all four fields | pass |
| Signature | present | — | pass |

Recorded:

| Recieved | Date Received | Notes |
|---|---|---|
| `Yes` | `01/09/2026` | *(blank)* |

Filed as `<Name> - <Month> <Year>.pdf`. Note the Date Received falls in the month *after* the
invoice month — the email arrived late in the evening UTC and rolled over locally.

## 15. Worked example — a failure and its recovery

*All values below are fabricated.*

An invoice arrives showing the period **25 Jul → 24 Aug** when the invoice month requires
**25 Jun → 24 Jul** — the right shape, the wrong month. Everything else is correct.

| Recieved | Date Received | Notes |
|---|---|---|
| `N/A` | `03/08/2026` | `Period 25/07-24/08, should be 25/06-24/07` |

The finance owner asks the contractor to amend and resend. The corrected invoice arrives on the
17th and passes every check. The row becomes:

| Recieved | Date Received | Notes |
|---|---|---|
| `Yes` | `17/08/2026` | *(cleared)* |

The document is filed at this point — not before. That is the full life cycle of an `N/A`.

---

## 16. What changes, and how often

| Item | Frequency | Action |
|---|---|---|
| Pay period dates | Every month | Derive them (§2); never hardcode |
| Fee computation file | New file monthly | Locate by name for the current month |
| Tracker tab | New tab monthly | Named `<Month> <Year>` in full |
| **Tracker file** | **New file every calendar year** | In January, check for the new year's file |
| Month folder | Every month | Usually already created |
| Invoice subfolder | Every month | Created by this process |
| Contractor list | A few changes most months | Joiners, leavers, role changes (§12) |
| Mailbox label | Does not change | — |
| The checks | Rarely | If Finance changes what to check, update this document |
| Invoice template | Rarely | A layout change may affect the signature guidance (§6.5) |

**Keep this document current.** Anything discovered that it does not cover — a new failure mode, a
changed convention, a special case — belongs here, and the finance owner should be told what
changed.

---

## 17. Checklist

- [ ] Invoice month and exact period dates established and confirmed
- [ ] This month's fee computation file located; period matches
- [ ] Correct year's tracker file and correct month's tab open
- [ ] Leavers checked against the mailbox; those with no invoice removed from the tab
- [ ] Joiners added, with formatting and dropdown matching existing rows
- [ ] All invoices collected; latest message used in every thread
- [ ] Every document extracted and the **signature visually confirmed**
- [ ] All checks run, reading the period's actual month names
- [ ] No invoice failed over the date printed on it — that is not a check
- [ ] `Yes` only where everything matched
- [ ] `N/A` wherever something did not — **with a note in every case**
- [ ] No `N/A` row left without a note; no `No` row given one
- [ ] `No` where nothing arrived; standing exemptions marked `No`
- [ ] All dates converted to local time and confirmed in the cell
- [ ] Month subfolder created
- [ ] Approved documents filed; **count reconciled against the `Yes` rows**
- [ ] Rejected invoices **not** filed
- [ ] Nothing emailed to anyone; no message drafted to a contractor
- [ ] Fee computation file untouched
- [ ] Reported, with failures and missing invoices listed first
