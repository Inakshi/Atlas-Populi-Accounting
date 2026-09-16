# Business background

**Status:** Draft for review  
**Prepared:** 16 September 2026  
**Scope:** Atlas Populi (Private) Limited, with Atlas Labs context where needed to understand the business.

Read this first, then [Finance department](finance-department.md) and [Systems and terminology](systems-and-terminology.md). These documents provide onboarding context, not transaction instructions or authority to act.

## Business and entity relationship

The local cash-forecast briefs describe Atlas Labs as the Australian parent company and Atlas Populi as its wholly owned Sri Lankan subsidiary. They describe Atlas Populi as the operating team and cost centre serving Atlas Labs. The AP Expenses FP&A handover corroborates the parent relationship and the need to keep the two entities' financial information distinct. [B1–B3]

This provides a working description of the relationship for this draft. It is drawn from internal working documents, not a corporate-register or ownership verification performed for this review.

| Entity | Background documented in the sources |
|---|---|
| Atlas Populi (Private) Limited | Based in Sri Lanka; described as the operating team/cost centre serving Atlas Labs; functional/base currency LKR. This is the entity covered by this repository. |
| Atlas Labs | Australian parent; the forecast briefs describe AUD as its functional currency and USD as a revenue currency. This is a separate entity and accounting scope. |

The existing [monthly-close checklist](../docs/10-monthly-close-agent-checklist.md) identifies a 31 March financial year-end and Asia/Colombo as the working timezone for Atlas Populi.

An Atlas Populi expense or cash forecast is not a consolidated view of the group. The local expense-model brief excludes Atlas Labs' cash, customer revenue and group runway from that particular model. That scope restriction should not be interpreted as a statement that every Finance user lacks access to Atlas Labs information. [B1–B3]

## Activities and reporting categories

The existing [accounting operating model](../docs/01-accounting-operating-model.md) records these Xero Department options at the time of its review:

- Architecture Visualisation.
- Product Engineering.
- Software Development.
- General.

Payroll documentation uses related labels, including ArchViz and G&A, and distinguishes Atlas Populi employment and contractor streams from Atlas Labs arrangements. [B4] These are useful indicators of the work and cost groupings represented in the records. They are not, by themselves, an approved organisation chart, a complete service catalogue, or proof that similarly named categories map one-to-one.

The [project and cost-code documentation](../docs/05-projects-cost-codes-and-effort.md) shows that project work can involve approved activities, resources, effort, rate cards and invoicing support. Some projects use sprint trackers; that is not documented as a universal requirement.

## Why this background matters to Finance

The local expense-forecast brief identifies a need to understand:

- Actual monthly expenditure and expected future expenditure.
- Recurring, one-off, payroll-related and statutory costs.
- The suppliers and categories driving expenditure.
- Atlas Populi's expected cash requirement.
- Forecast risks and gaps in supporting information. [B1]

These are documented planning needs, not a newly approved list of department KPIs. The broader Finance structure agreed for this repository is described in [Finance department](finance-department.md).

The expense handover distinguishes payment-voucher information, petty-cash detail, forecasting assumptions and accounting records. They describe different aspects of the same business activity: cash paid, expense incurred, accounting treatment and future commitment are not interchangeable. [B3]

## Relationships that need careful interpretation

Atlas Labs' ownership relationship does not establish the detailed funding, intercompany invoicing or settlement arrangements. Those arrangements still need to be described.

Existing project documentation contains Horcery examples. Their presence does not establish Horcery's legal relationship to Atlas Populi, which entity contracts with a customer, or which entity raises a particular invoice. Horcery-specific inventory, subscription and Stripe operations are therefore not included as Atlas Populi responsibilities in this draft.

## Points to confirm during review

1. **Commercial description:** What services or products does Atlas sell, to which customer groups, and what part of delivery does Atlas Populi perform?
2. **Entity arrangements:** Are the ownership and operating descriptions above still current? What are the actual intercompany funding, billing and settlement arrangements?
3. **Business organisation:** Are the reporting categories above the right high-level business areas? How should data-labeling work and general administration be described?
4. **Business priorities:** What current business objectives should Finance and its agents understand?

These are gaps in this draft's background description, not a separate operational task register.

## Sources and evidence limits

Repository documents linked above were checked on main at commit `2f09bbef11cef73ad5102a9e8fd2ec9c74b50fbe`. Their historical observations are not a fresh live-system verification.

The following local source references are relative to the author's AI Projects folder. They are provenance references, not links available to every repository user:

| ID | Local source | Material used |
|---|---|---|
| B1 | `Atlas/AP Finance/Cash Forecast/Cash forecast prompt.md` | Business Context; entity relationship, currencies and expense-planning questions. |
| B2 | `Atlas/AP Finance/Cash Forecast/architecutre prompt.md` | Business Context; corroborating entity and model-scope description. |
| B3 | `Atlas/AP Finance/AP_Expenses_FP&A_Master_Handover.md` — prepared 4 July 2026 | Purpose and entity/currency boundaries; role of vouchers, petty cash and forecasts. |
| B4 | `Atlas/Payroll/Payroll_Forecast_Master_Knowledge.md` | Entity/department distinctions and payroll-stream descriptions; no employee-level data reproduced. |

The review used selected relevant sections. It did not re-audit the underlying workbooks, verify live balances or legal ownership, or establish the complete commercial model.
