# Chart of accounts and coding reference

**Organisation:** Atlas Populi (Private) Limited
**Status:** Active policy
**Reviewed against Xero:** 18 September 2026
**Scope:** Active accounts only

## Purpose

This reference explains what each active Atlas Populi general-ledger account is for and the types of transactions that belong in it. It is intended to support consistent coding by Finance and AI agents.

The account name alone is not sufficient evidence for a posting. Every transaction must still be supported by the source document, the supplier or customer history, the accounting period, the applicable tax treatment, the Department and any required project or task code.

Accounts marked **Confirm before use** remain active in Xero, but the reviewed evidence does not establish a safe, distinct coding rule. They should not be used for a new transaction until Finance confirms the intended treatment.

## Bank and cash accounts

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 02 | Petty Cash Atlas Populi | Records cash held and used as petty cash. | Petty-cash funding, approved cash purchases, reimbursements paid from petty cash and cash-count adjustments supported by a reconciliation. |
| 100 | LKR Account: Commercial Bank | Atlas Populi's main LKR operating account and the principal account used to make payments. | Transfers received from the LKR Union Bank account, supplier payments, payroll payments, statutory payments, other approved LKR payments and bank charges belonging to this account. |
| 101 | LKR Account: Union Bank | Acts primarily as a clearing account for USD revenue converted into LKR before the funds are transferred to the main Commercial Bank account. | LKR proceeds received when funds are converted from the USD Union Bank account, transfers of those proceeds to the LKR Commercial Bank account and bank charges directly related to this account. It is not the normal account for operating payments. |
| 102 | USD Account: Union Bank | Atlas Populi's principal USD receipt account. Atlas Labs pays Atlas Populi's USD revenue into this account. | USD receipts from Atlas Labs, conversion of USD into the LKR Union Bank account, and bank interest or charges directly related to this account. |
| 103 | USD Account: Commercial Bank | An active Xero bank account that is not currently used and is expected to remain substantially empty. | No routine transactions should be recorded here while the account remains unused. Record a transaction only if it appears on the corresponding bank statement and is supported by evidence. |

The normal funding flow is:

1. Atlas Labs pays Atlas Populi's USD revenue into account 102 — USD Account: Union Bank.
2. The USD is converted into LKR through account 101 — LKR Account: Union Bank.
3. The LKR proceeds are transferred to account 100 — LKR Account: Commercial Bank.
4. Atlas Populi makes its operating payments from the LKR Commercial Bank account.

Each movement must be recorded as a transfer between the actual source and destination accounts. Bank fees belong in account 401 and interest income in account 201; they should not be absorbed into the transfer amount.

## Revenue and other income

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 200 | Sales | Records Atlas Populi's ordinary service revenue. | Project and service invoices issued to Atlas Labs for work delivered by Atlas Populi, including time-and-materials billing under the agreed intercompany arrangement. |
| 201 | Interest Income | Records interest earned on Atlas Populi funds. | Bank interest credited to LKR or USD accounts and other supported interest income. |
| 202 | Income from Operational Support Services | Records operating income earned from parties other than Atlas Labs. Historical use includes external consulting and, more recently, CNC machining and related services. | External operational-service income, including CNC machining and similar work, together with incidental operating receipts historically treated here. Atlas Labs project and service invoices remain in account 200. |
| 210 | Discount Received | Records reductions in amounts payable that are treated as income rather than reductions of the original expense. | Supplier settlement discounts and other supported discounts received. Supplier credit notes should normally follow the original expense treatment unless Finance approves separate discount recognition. |

## Receivables and other current assets

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 313 | Security Deposits | Records refundable deposits that remain recoverable by Atlas Populi. | Rental, utility and other refundable security deposits; refunds; and approved transfers into a right-of-use asset or another asset where required by the year-end accounting treatment. |
| 314 | VAT Input | Records separately identified input VAT recoverable or carried forward. | The VAT component of qualifying supplier invoices when Finance records the expense base and VAT as separate lines, plus supported tax adjustments and settlements. |
| 315 | Income Tax Recievable | Records income-tax amounts recoverable from the tax authority. | Tax overpayments, refundable credits and approved adjustments or write-offs. The Xero account name contains a spelling error; this reference preserves the live name. |
| 316 | Reimbursable Expenses | Records costs paid by Atlas Populi that are recoverable from another group entity or party. | Supported expenses to be reimbursed, including Horcery-related expenditure recoverable through Atlas Labs, and the subsequent recovery or reclassification. |
| 317 | Accounts Receivables 2 | Secondary receivables account used when an accountant-approved journal cannot be posted to Xero's locked Accounts Receivable account 610. | The receivables side of approved manual journals for adjustments, write-offs, reclassifications and corrections that cannot be processed directly through account 610. The other side must use the appropriate supported expense, income, liability or equity account. Ordinary customer invoices, credit notes and receipts continue to use account 610 through Xero's receivables process. |
| 610 | Accounts Receivable | Xero's trade-receivables control account for approved customer invoices not yet paid. | Sales invoices, customer credit notes, receipts allocated to invoices and authorised receivables adjustments generated through the normal Xero invoice process. Do not post routine manual journals here. |
| 620 | Prepayments | Records expenditure paid before the related goods or services are consumed. | Supplier advances, annual subscriptions, insurance and other prepaid services; monthly or usage-based releases to the relevant expense account; refunds; and supported corrections. Each balance must be tied to its originating supplier and service period. |
| 621 | Salary Advance Account | Records recoverable salary advances made to employees. | Approved advances, payroll deductions or repayments that clear them, and specifically approved write-offs. It should not contain normal salary expense. |

## Expenses and direct costs

### People and professional services

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 403 | Project Consulting | Records external consulting that directly supports projects or service delivery. | Engineering, design and other project-consultant fees that can be linked to delivery work. The current Xero description also mentions tax and payroll consulting, but accounting and tax professional fees have a separate account at 451; use 451 for those unless Finance confirms otherwise. |
| 405 | Wages and Salaries (Indirect) | Records payroll cost for employees in indirect, support or administrative functions. | Gross salaries and supported payroll adjustments for people whose work is not treated as a direct project or delivery cost. |
| 417 | EPF - Employer Contribution | Records the employer EPF cost relating to direct employees. | Employer EPF contributions associated with payroll recorded in account 421. Employee deductions belong in the relevant payable account, not here. |
| 418 | ETF | Records the employer ETF cost relating to direct employees. | Employer ETF contributions associated with payroll recorded in account 421. |
| 421 | Wages and Salaries | Records payroll cost for employees directly involved in projects or service delivery. | Gross salaries, approved direct-payroll adjustments and year-end corrections for direct staff. Employee cash payments and payroll liabilities are cleared through the appropriate bank and payable accounts. |
| 431 | Bonus | Records bonuses awarded to employees. | Approved performance, annual or other employee bonuses and related reversals. Ordinary monthly salary remains in 405 or 421. |
| 445 | Accommodation Allowance | Records accommodation allowances provided to staff. | Approved employee accommodation allowances or employer-paid accommodation treated as employee compensation. |
| 449 | Recruitment Costs | Records costs of hiring employees or contractors. | Recruitment advertising, recruiter fees, candidate assessments, background checks and other directly attributable recruitment costs. |
| 450 | Staff Welfare | Records general employee-welfare expenditure. | Approved welfare activities, refreshments or benefits provided for staff where a more specific account does not apply. Team meals and hospitality normally belong in account 439. |
| 451 | Accounting and Tax Consultant Fees | Records external accounting, audit and tax professional fees. | Accounting support, tax advisory and compliance fees, audit-fee expense and similar professional services. Audit fees accrued but unpaid are credited to account 861. |
| 456 | Gratuity Provision | Records the period expense or adjustment for employee gratuity obligations. | Accountant-approved year-end gratuity provisions, reversals and corrections, with the corresponding liability in account 863. |
| 457 | Allowances for Interns | Records allowances paid to interns where treated as a direct cost. | Approved intern allowances and related payroll adjustments for interns supporting project or delivery work. |
| 462 | EPF - Employer Contribution ID | Records employer EPF cost relating to indirect employees. | Employer EPF contributions associated with indirect payroll in account 405. `ID` denotes the indirect-payroll classification in the current chart. |
| 463 | ETF ID | Records employer ETF cost relating to indirect employees. | Employer ETF contributions associated with indirect payroll in account 405. `ID` denotes the indirect-payroll classification in the current chart. |

### Premises, office and administration

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 401 | Bank Fees | Records charges imposed by Atlas Populi's banks. | Transfer fees, transaction charges, cheque charges and other bank-service fees. Interest belongs in account 411. |
| 402 | Janitorial Services | Records contracted cleaning services for business premises. | Cleaning-service invoices and recurring janitorial charges. Cleaning materials purchased directly may be recorded in 415 when appropriate. |
| 404 | Caretaker and Security Expenses | Records the cost of guarding and caretaking business premises. | Security-service invoices, guards and caretaker services. |
| 408 | Freight & Courier | Records third-party delivery, freight, postage and courier costs. | Local and international courier charges, freight and document or parcel delivery costs. Customs duties belong in account 425. |
| 409 | General Expenses | Residual account for supported operating expenditure that does not fit a more specific account. | Infrequent, low-value general expenses after checking that no dedicated account applies. It has also held historical correction write-offs, but account 506 should be used for specifically approved write-offs. |
| 410 | Insurance | Records the portion of business insurance relating to the current period. | Property, equipment and other business-insurance expense, including monthly releases from account 620. Refundable or future-period portions remain in Prepayments. |
| 412 | Administration Expenses | Records general corporate administration that does not have a more specific account. | Administrative support, regulatory and professional memberships, visa and permit administration, postage, general compliance costs and penalties historically treated as administration. Registrar of Companies filings and company-secretarial work belong in account 433. |
| 413 | Water Expense | Records water supplied to business premises. | Water-board bills, water deliveries and related usage charges. |
| 415 | Office Supplies and Groceries | Records consumable office supplies and workplace groceries. | Pantry items, cleaning consumables, storage boxes, cables and other low-value office supplies that are not fixed assets or specialised project components. |
| 416 | Printing & Stationery | Records printing and stationery used by the business. | Printed materials, paper, stationery, business cards and external printing services. |
| 419 | Rent | Records occupancy cost for leased premises before any required lease-accounting adjustment. | Office rent and supported rent adjustments. At year-end, accountant-approved lease entries may reclassify rent against the lease liability under the applicable lease-accounting treatment. |
| 420 | Repairs and Maintenance | Records work that restores an existing asset or premises to its normal condition without creating a new asset. | Equipment and premises repairs, servicing and recurring maintenance such as supported pest-control releases. Capital improvements belong in a fixed-asset account. |
| 422 | Telephone & Internet | Records business communications and connectivity costs. | Mobile and fixed-line bills, internet connections, data services and connection charges. |
| 427 | Electricity | Records electricity supplied to business premises. | Electricity bills and directly related utility charges. |
| 428 | Office Miscellaneous Fittings and Maintenance | Records non-capital office and workshop fittings, maintenance materials and minor installations. Historical use overlaps with account 420, including some repair services. | Low-value fittings, replacement parts, small tools, maintenance materials and minor installation work. To reduce the historical overlap, use account 420 when the substance of the purchase is a repair, service or recurring maintenance activity. |
| 430 | Traveling and Transport | Records business travel and local transport. | Employee business travel, taxis, ride-hailing, mileage or transport reimbursements, and transport of people for business purposes. Freight of goods belongs in 408. |
| 433 | Secretarial Expenses | Records company-secretarial and Registrar of Companies expenditure. Historical postings and an external-auditor reclassification establish this as the specific account for these costs. | Annual returns, statutory forms, certified copies, Registrar of Companies filing charges and company-secretarial service fees. Similar recurring service fees recently posted to 412 should use 433 going forward; prior periods should only be reclassified if Finance and the accountant consider the adjustment necessary. |
| 435 | Training expenses | Records employee learning and development costs. | Training courses, workshops, certifications and approved training materials. |
| 439 | Meals and Hospitality Expenses | Records team meals and business hospitality. | Team meals, refreshments for meetings and approved hospitality costs. General staff benefits belong in 450 and non-deductible entertainment in 407 where applicable. |
| 441 | Computer Accessories | Records low-value computer accessories that are expensed rather than capitalised. | Keyboards, mice, adapters, cables, headsets and similar accessories below the fixed-asset threshold. Computers and capital equipment belong in 700. |

### Project, product and operating inputs

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 414 | Biomedical Expenses | Records biomedical project costs. **Confirm before use:** historical activity exists, but the underlying goods or services were not identifiable from the reviewed reports. | Biomedical materials, testing or specialist services only when supported by an approved project and prior coding evidence. |
| 423 | Research and Development costs | Records research, prototype and product-development expenditure. Transaction history consistently shows components, prototypes, trials, testing and experimental work; the Xero description referring to domestic travel is incorrect. | Prototype materials, experimental components, product samples, testing services, field or horse trials and other supported development costs. Business travel belongs in account 430. |
| 455 | Miscellaneous Tools and components | Records low-value project tools and components that do not fit the electronic or industrial-component accounts. | Small tools, general components and minor project consumables. Use 458 or 459 when the item is clearly electronic or industrial. |
| 458 | Electronic Components | Records electronic parts consumed in project or product work. | Sensors, circuit components, connectors, boards and other electronic parts that are expensed rather than held as inventory or capital assets. |
| 459 | Industrial Components | Records mechanical or industrial parts consumed in project or product work. | Fabricated parts, mechanical components, enclosures and similar project inputs that are expensed rather than held as inventory or capital assets. |
| 460 | Industrial Design Expenses | Records direct industrial-design costs. | External industrial-design services, prototyping design work and other approved design inputs attributable to a project. |
| 464 | Packaging Material and Expenses | Records packaging used for project or product items. | Boxes, inserts, labels, protective material and packaging services. Freight belongs in 408. |
| 500 | Software Subscriptions | Records software and online services treated as direct delivery costs in the current chart. | Licences, cloud tools and recurring software subscriptions used in project or service delivery, including current-period releases from account 620. General administrative software should follow the established supplier treatment until Finance defines a separate rule. |
| 504 | Product Testing and Validation Expenses | Records direct costs of trials, testing and validation. | Test services, trial materials, certifications, prototypes consumed in testing and other supported validation expenditure. |

### Sales, marketing and external activities

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 400 | Advertising & Marketing | Records paid advertising for Atlas Populi's own operations and the CNC activity. Earlier recruitment advertising was reclassified by the external auditor and should now use account 449. | Facebook campaigns, media placements and similar paid advertising for Atlas Populi or CNC activities. Recruitment advertising belongs in account 449. |
| 407 | Entertainment | Records approved business entertainment classified as non-deductible under the current Xero description. | Client or business entertainment that Finance determines is not tax deductible. Team meals should normally use 439. |
| 426 | Uniforms | Records uniforms and branded clothing supplied for work. | Office shirts, T-shirts, protective clothing and other approved work uniforms. |
| 434 | Donations and Special Projects | Records approved donations and expenditure on separately authorised special initiatives. | Charitable donations and exceptional special-project costs that do not form part of ordinary service delivery. The approval and business purpose must be retained. |
| 505 | Marketing Expense | Records Horcery and other specifically identified product or project marketing. Historical postings include Horcery sponsorships, event materials, printed collateral and branded promotional items supported by project codes. | Project-coded sponsorships, event costs, banners, printed collateral, branded merchandise and other campaign expenditure for Horcery or another identified product project. General Atlas Populi or CNC paid advertising belongs in account 400. |

### Tax, finance charges, foreign exchange and write-offs

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 264 | Bad Debt | Records approved losses on customer receivables that are no longer recoverable. | Write-off of specific trade receivables after recovery action and approval, together with reversals of earlier bad-debt entries. |
| 411 | Interest Expense | Records financing costs. | Bank interest and accountant-approved unwinding interest on lease liabilities. Bank service charges belong in 401. |
| 425 | Customs Duties and Levies | Records customs charges on imported goods. | Import duty, customs levies, clearance taxes that are expensed and similar government charges directly related to imports. Freight and courier charges belong in 408. |
| 452 | Stamp Duty Expense | Records stamp duty borne by Atlas Populi. | Stamp duty on agreements, instruments and other supported transactions. |
| 454 | Income Tax | Records corporate income-tax expense under the treatment used after 2018. | Accountant-approved current or year-end corporate income-tax expense and adjustments. The corresponding liability belongs in account 830; settlement of an existing liability clears account 830 rather than creating another expense. |
| 497 | Bank Revaluations | Records revaluation movements on foreign-currency bank accounts. | Xero-generated or accountant-approved period-end exchange movements on USD bank balances. It should not be used for bank fees or manual transfers. |
| 498 | Unrealised Currency Gains | Records exchange movements on foreign-currency balances that remain outstanding at the reporting date. | Period-end unrealised gains or losses on open foreign-currency receivables, payables or other monetary items. |
| 499 | Realised Currency Gains | Records exchange gains or losses realised when a foreign-currency transaction is settled. | Realised differences between invoice recognition and receipt or payment, and other settled foreign-currency differences. Despite the account name, the balance may represent either a gain or a loss. |
| 502 | SSCL Expenses | Records the Social Security Contribution Levy borne as an expense. | SSCL charged on qualifying supplier costs or accountant-approved SSCL adjustments. Amounts should be separated from prepayment bases where the existing process requires it. |
| 506 | Write Off | Records specifically approved write-offs and correction entries. | Approved write-off of irrecoverable advances, tax receivables, historic balances or erroneous opening balances. It is not a general suspense account and should normally be used through an approved journal. |

### Depreciation and amortisation expense

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 406 | Depreciation on Computer Equipment | Records depreciation expense on computer equipment. | Periodic accountant-approved depreciation, with the credit recorded in accumulated depreciation account 708. |
| 447 | Depreciation on Electrical Equipment | Records depreciation expense on electrical equipment. | Periodic accountant-approved depreciation, with the credit recorded in account 707. |
| 448 | Depreciation on Furniture | Records depreciation expense on furniture. | Periodic accountant-approved depreciation, with the credit recorded in account 706. |
| 453 | Depreciation of Intangible Assets | Records amortisation or depreciation expense on intangible assets. | Periodic accountant-approved amortisation, with the credit recorded in account 709. |
| 461 | Depreciation on Fixtures and Fittings | Records depreciation expense on fixtures and fittings. | Periodic accountant-approved depreciation, with the credit recorded in account 710. |
| 465 | Depreciation on Leasehold Improvements | Records depreciation expense on leasehold improvements. | Periodic accountant-approved depreciation, with the credit recorded in account 711. |
| 503 | ROU Asset Amortization | Records amortisation of right-of-use assets. | Accountant-approved lease amortisation entries, with the credit recorded in account 713. |

## Fixed assets and accumulated depreciation

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 700 | Computer Equipment | Records capitalised computer equipment owned and controlled by Atlas Populi. | Computers, servers and qualifying equipment above the approved capitalisation threshold; disposals and asset adjustments. Low-value accessories belong in 441. |
| 701 | Furniture | Records capitalised furniture. | Desks, chairs, cabinets and other qualifying furniture purchases, disposals and adjustments. |
| 702 | Fixtures and Fittings | Records capitalised fixtures and fittings. | Qualifying installed fixtures, office fittings and related capital additions, disposals and adjustments. |
| 703 | Leasehold Improvements | Records capital expenditure that improves leased premises. | Fit-outs, structural improvements and other qualifying expenditure that benefits more than the current period. Repairs remain in 420 or the relevant maintenance account. |
| 704 | Electrical Equipment | Records capitalised electrical equipment. | Qualifying electrical equipment purchases, disposals and adjustments. |
| 705 | Intangible Assets | Records capitalised identifiable intangible assets. The only identified historical asset was a 2018 trademark publication fee, which was subsequently written off; the account currently has no balance. | Only costs that meet accountant-approved intangible-asset recognition criteria, plus approved disposals, impairment and write-offs. Ordinary subscriptions belong in 500. |
| 706 | Accumulated Depreciation on Furniture | Holds cumulative depreciation charged against furniture. | Credits from periodic depreciation, and approved reversals or disposal entries. Do not post asset purchases here. |
| 707 | Accumulated Depreciation on Electrical Equipment | Holds cumulative depreciation charged against electrical equipment. | Credits from periodic depreciation, and approved reversals or disposal entries. |
| 708 | Accumulated Depreciation on Computer Equipment | Holds cumulative depreciation charged against computer equipment. | Credits from periodic depreciation, and approved reversals or disposal entries. |
| 709 | Accumulated depreciation on Intangible Assets | Holds cumulative amortisation charged against account 705. Historical entries relate only to the reversal and write-off of the former trademark asset, and the account currently has no balance. | Accountant-approved amortisation, reversals and disposal or impairment entries relating to a recognised balance in account 705. Do not use when account 705 has no recognised asset. |
| 710 | Accumulated Depreciation on Fixtures and Fitting | Holds cumulative depreciation charged against fixtures and fittings. | Credits from periodic depreciation, and approved reversals or disposal entries. |
| 711 | Accumulated Depreciation on Leasehold Improvements | Holds cumulative depreciation charged against leasehold improvements. | Credits from periodic depreciation, and approved reversals or disposal entries. |
| 712 | Right Of Use Asset | Records assets recognised for leased premises or other qualifying leases. | Initial lease recognition, approved remeasurement, qualifying deposit reclassification and other accountant-approved lease adjustments. |
| 713 | Accumulated Amortization on ROU Asset | Holds cumulative amortisation charged against right-of-use assets. | Credits from periodic ROU amortisation and approved lease modification or derecognition entries. |

## Payables, tax and other liabilities

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 800 | Accounts Payable | Xero's trade-payables control account for approved supplier bills not yet paid. | Supplier bills, supplier credit notes, payments allocated to bills and authorised payable adjustments generated through the normal Xero bills process. Do not post routine manual journals here. |
| 801 | Unpaid Expense Claims | Records approved employee expense claims that remain unpaid. | Employee or director expense claims and the payments that settle them. **Confirm before use:** no current balance appeared in the reviewed trial balance. |
| 802 | Accounts Payable 2 | Secondary payables account used when an accountant-approved journal cannot be posted to Xero's locked Accounts Payable account 800. | The payables side of approved manual journals for adjustments, write-offs, reclassifications and corrections that cannot be processed directly through account 800. The other side must use the appropriate supported expense, income, asset or equity account. Ordinary supplier bills, credit notes and payments continue to use account 800 through Xero's payables process. |
| 803 | Wages Payable | Records net wages awaiting payment. Historical balance sheets show intermittent payroll balances, including during the current financial year, even though the account is nil at the latest review date. | Existing payroll-generated entries, specifically approved wage-liability journals and payments that settle those liabilities. Normal salary expense belongs in 405 or 421. |
| 820 | Sales Tax | Xero's system tax-control account for sales tax owing to or recoverable from the tax authority. | Tax amounts generated by configured Xero tax rates and payments or refunds that settle the resulting control balance. Under the observed manual VAT process, separately stated input VAT is recorded in 314. Do not create another tax-control account. |
| 830 | Income Tax Payable | Records corporate income tax owed to the tax authority. | Tax provisions transferred to the payable, assessments, payments and approved adjustments. A tax payment should clear this liability rather than automatically create a new expense. |
| 840 | Historical Adjustment | Holds accountant-approved historical or conversion adjustments. | Opening-balance and conversion corrections only. It should not be selected for ordinary current-period transactions. |
| 860 | Rounding | Records immaterial rounding differences needed to balance a supported entry. | Small rounding adjustments only. It must not be used to conceal an unexplained difference. |
| 861 | Audit Fee Payable | Records audit fees accrued but not yet paid. | Year-end audit-fee accruals, payments or reclassifications that clear the accrual, and approved corrections. The corresponding expense is normally in 451. |
| 862 | Withholding Tax | Records withholding tax deducted or otherwise payable to the tax authority. | Supplier or other withholding-tax liabilities, remittances and approved adjustments. |
| 863 | Gratuity Payable | Records the long-term employee gratuity obligation. | Accountant-approved gratuity provisions, payments, reversals and actuarial or year-end corrections. The corresponding expense is in 456. |
| 864 | Lease Liability | Records obligations arising from recognised leases. | Initial lease-liability recognition, lease payments, unwinding interest, remeasurements and other accountant-approved lease adjustments. |
| 877 | Tracking Transfers | Xero system account for transfers between tracking categories. | Xero-generated tracking-category transfer entries only. It should not be selected for ordinary coding. |

## Equity

| Code | Account | Purpose | Transactions recorded in the account |
|---|---|---|---|
| 960 | Retained Earnings | Holds cumulative profits and losses carried forward from prior financial years. | Xero year-end closing movements and accountant-approved equity adjustments. The live description says `Do not Use`; it must not be selected for routine coding. |
| 961 | Current Account | Records amounts due to or from a director. The account arose when a director funded the Emperor Residencies security deposit in 2018; the resulting LKR 243,350 amount owed to the director was written off in March 2025 and the account is now nil. The Xero description refers to the original transaction and should not be treated as the account's general purpose. | Accountant-approved director funding, repayments, settlements and write-offs. Each posting must state the director, whether the amount is due to or from that person, and the underlying transaction. |
| 970 | Owner A Share Capital | Records issued share capital. | Share subscriptions, approved changes to issued capital and formal capital corrections supported by corporate records. |

## Accounts proposed for archiving

These accounts remain active in Xero but have been removed from the working coding tables because they are no longer expected to be used.

| Code | Account | Current position | Action required |
|---|---|---|---|
| 214 | Trabeya (Private) Limited receivable | No balance appeared in the current trial balance. The account has been inactive for a long period and is no longer required for current coding. | Check that the account is not locked by a repeating transaction, bank rule or another live Xero dependency, then archive it. Historical transactions will remain available for reporting. |
| 312 | IOU | No balance appeared in the current trial balance and there is no current business requirement to use the account. | Check that the account is not locked by a repeating transaction, bank rule or another live Xero dependency, then archive it. Historical transactions will remain available for reporting. |
| 622 | Refund Received | Operationally inactive. No current or historical balance, manual journal, bank transaction, invoice or credit-note use was found in the reviewed Xero history. | Check that the account has no live Xero dependency, then archive it. Record future supplier refunds against the original transaction or the appropriate supported account rather than reactivating this unused account without a policy decision. |
| 630 | Inventory | Operationally inactive. No current or historical balance or transaction use was found, and Atlas Populi has no tracked inventory items in Xero. | Check that the account has no live Xero dependency, then archive it. Continue recording project materials and components in the relevant supported expense accounts unless Atlas Populi formally introduces an inventory process. |
| 424 | Provision for Income Tax Expense | Used for the 2017/18 income-tax provision. Later tax-expense entries consistently use account 454 with the liability in account 830. | Check for live dependencies, then archive this legacy duplicate. Use 454 for approved income-tax expense and 830 for the related liability. |
| 432 | PAYE | One authorised 2019 posting was a PAYE penalty. A 2023 payment and receipt offset each other, and no continuing PAYE expense pattern or current balance was found. More recent statutory penalties have been recorded in account 412. | Check for live dependencies, then archive this legacy account. Continue using the established payroll process for net pay and statutory settlements; record supported penalties consistently in 412 unless the accountant directs otherwise. |
| 444 | Office Maintainance | No bank transaction, invoice, credit note, manual journal or balance-sheet use was found. Accounts 420 and 428 already cover the established repair and office-maintenance treatments. | Check for live dependencies, then archive it. Use 420 for repair and servicing activity and 428 for minor fittings, parts and maintenance materials. |
| 496 | Unrealised exchange Gain 2 | Used once in March 2022 for a debtor-revaluation journal. Current foreign-exchange treatment uses 497 for bank revaluations, 498 for unrealised currency movements and 499 for realised currency movements. | Check that the 2022 journal and any report dependency do not prevent archiving, then archive this legacy duplicate. |
| 825 | Employee Tax Payable | No transaction, manual-journal or historical balance-sheet use was found in the reviewed Xero history. | Check for payroll or other live dependencies, then archive it. Do not introduce a new employee-tax liability treatment through this account without an approved payroll-process change. |
| 826 | Superannuation Payable | No transaction, manual-journal or historical balance-sheet use was found in the reviewed Xero history. Atlas Populi's employer EPF and ETF expenses use the dedicated direct and indirect expense accounts. | Check for payroll or other live dependencies, then archive it. Do not introduce this generic Xero liability into the existing EPF and ETF process without an approved payroll-process change. |

Until the archive actions are completed, none of these accounts should be used for new transactions.

## Coding rules

1. Use the most specific supported account. Accounts such as General Expenses, Write Off, Historical Adjustment and Rounding are not substitutes for investigating a transaction.
2. Use accounts 610 and 800 through Xero's invoice and bill workflows. Xero locks these system control accounts against direct journals. When an approved receivables or payables journal is required, use secondary account 317 or 802 respectively and retain the calculation and approval supporting the entry.
3. Separate the expense base, VAT Input and other levies when the approved source and existing treatment require separate lines.
4. Keep direct payroll and related EPF/ETF in 421, 417 and 418. Keep indirect payroll and related EPF/ETF in 405, 462 and 463.
5. Capitalise expenditure only when it meets the approved fixed-asset criteria. Otherwise use the relevant expense account.
6. Use depreciation, gratuity, lease, tax provision, write-off and historical-adjustment accounts only through an accountant-approved calculation or journal.
7. For foreign-currency transactions, record the underlying sale, purchase, receipt or payment in its normal account. Use the foreign-exchange accounts only for the supported exchange difference.
8. When a transaction does not clearly fit the established historical treatment, review comparable prior transactions and their supporting documents before selecting an account. Escalate genuinely new transaction types rather than forcing them into the nearest account name.

## Historical treatment applied in this reference

The coding rules above follow the treatment established by Atlas Populi's Xero history:

- Account 200 is used for Atlas Labs project and service revenue. Account 202 is used for external operational income, with recent activity dominated by CNC work.
- Account 400 is used for Atlas Populi and CNC advertising. Account 505 is used for project-coded Horcery and product-marketing activity.
- Account 412 remains the general administration account. Account 433 is the specific account for Registrar of Companies and company-secretarial work, consistent with the older postings and the external-auditor reclassification.
- Accounts 420 and 428 have historically overlapped. The recommended boundary is to use 420 for repair, servicing and recurring maintenance, and 428 for minor fittings, parts, materials and small installations. Account 444 has no established use and is proposed for archiving.
- Account 423 is an R&D account. Its history is made up of prototypes, components, trials, testing and product-development costs; it is not a travel account.
- Account 454 is the continuing income-tax expense account and account 830 holds the liability. Account 424 is a legacy 2017/18 provision account proposed for archiving.
- Current foreign-exchange treatment uses accounts 497, 498 and 499. Account 496 has one old debtor-revaluation journal and is proposed for archiving.
- Accounts 705 and 709 remain a valid asset-and-amortisation pair, but should stay nil unless the accountant approves recognition of an intangible asset.
- Account 803 remains part of the payroll-liability history. Accounts 825 and 826 have no established use and are proposed for archiving after dependency checks.
- Account 961 is the director current account. Its security-deposit wording describes the transaction that created the former balance, which was written off in March 2025.
