# Payment vouchers and Xero bills

## Preparing the voucher

Confirm the following before the voucher is treated as ready:

- Supplier matches the source invoice or approved request.
- Invoice number is copied exactly, including leading zeros.
- Invoice and due dates follow the source and the supplier's established treatment.
- Description identifies the service or goods, service period, and task cost code where applicable.
- Invoice value and the actual amount paid are not confused.
- GL account, tax treatment and Department are independently checked.
- Supporting invoice/receipt and Jira or procurement link are retained.

The PV tracker separately records invoice value, LKR payment, USD amount, exchange rate, business unit, cheque number, payment method, Xero link and notes. When several rows belong to one voucher or batch, record the cash amount once according to the existing tracker design.

## One-off and recurring bills

For one-off bills, use the supplier invoice date and due date unless a documented exception applies.

For recurring bills:

- Check the same supplier/service history first.
- The recent recurring pattern generally dates the bill on the first day of the service month and uses month-end as the due date.
- Include the supplier invoice number and service month/year in the reference.
- For suppliers with multiple services or connections, include the connection/service identifier.
- Make the reference and description agree on the service month.

Historical exceptions should be recorded and investigated. They should not automatically override a clear recent convention.

## When no formal invoice exists

Use the PV number as the Xero reference and retain the approved source evidence, such as a receipt or request. Update the PV tracker so the support can be traced from the Xero record.

## VAT line treatment observed

The sampled workflow separates the expense and VAT Input amounts:

- Expense line: the appropriate expense/direct-cost account, using the configured **Tax on Purchases (0%)** tax type.
- VAT line: account **314 — VAT Input**, using **Tax Exempt (0%)**.

The zero-percent labels describe the configured Xero tax types on these manually separated lines. They do not mean the underlying supplier invoice had no VAT, and they are not a substitute for a tax-policy check. Do not calculate VAT again when the VAT amount has already been separated from the supplier invoice.

The PV sheet marks VAT invoices in blue and uses the note **VAT Invoice**. Filing instructions require VAT invoices and cheque payments to be filed with PV sheets. Soft copies are attached to Jira and Xero.

## Payments and status

Before recording or matching a payment:

- Confirm date, payee, reference, voucher and amount.
- Confirm whether the Xero object is a bill, prepayment, transfer or direct receipt.
- For partial payments, reconcile only the active allocation being paid.
- Exclude deleted payment attempts.
- Do not create a second bill because a prepayment is absent from an ordinary bill search.

## Supplier consistency rule

For each vendor, prefer the historically consistent account, date convention, reference format and description. Raise a question when:

- two recent active records use conflicting treatments;
- the current source document conflicts with the established pattern;
- a proposed change would alter the GL classification;
- a historical outlier has no documented explanation; or
- the source evidence cannot establish the correct service period.
