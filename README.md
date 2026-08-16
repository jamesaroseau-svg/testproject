# Household Financial Model

A comprehensive Excel-based financial projection model for household cash flow, net worth, debt repayment, and superannuation tracking through 2032.

## Overview

This model projects household finances across multiple dimensions:
- **Combined net worth** and **net debt position** across both partners
- **Annual cash surplus** available for additional savings or debt reduction
- **Superannuation growth** trajectory for retirement planning
- **Loan repayment schedules** with offset account dynamics
- **School fee commitments** and their impact on cash flow

The model runs from 2026 to 2032 and captures the effects of employment changes, salary growth, and discretionary mortgage overpayments.

## Model Structure

**household_financial_model_v3.xlsx** contains:

- **Assumptions** — Central control sheet for all model inputs
  - Salary and growth assumptions for both partners
  - Property loan details (Alexander St and Walter St)
  - Monthly extra repayments and offset account mechanics
  - School fee schedule (St Kevin's College)
  - Employment gap assumptions (Sue's redundancy scenario)

- **Projection** — Year-by-year cash flow and balance sheet
  - Income, tax, superannuation contributions
  - Loan balances, interest calculations, offset flows
  - Net worth build and annual surplus
  - Saturation status flags for offset accounts

- **Dashboard** — Summary metrics and key tracking
  - Net worth trajectory
  - Combined net debt
  - Superannuation position
  - Annual surplus
  - Saturation status

## Key Assumptions

### Income
- Base salaries with annual 2.5% growth
- Sue experiences a 4-month employment gap in 2027, returning at 100% of prior salary
- No salary impact beyond the gap year

### Property Loans
- **Alexander St**: $750/week extra repayment ($1,497.87/month)
- **Walter St**: Extra repayment of $267.44/month
- $26,000 annual offset account inflow from external source
- $20,000 ceiling buffer on combined offset accounts
- Overflow from Alexander offset flows to Walter once Alexander saturates

### School Fees
- St Kevin's College fees starting at $37,596 annually (2026 basis)
- Continues through the projection period

### Tax & Super
- Australian tax treatment with Medicare Levy
- Concessional superannuation contributions
- Income testing on various benefits as applicable

## Key Outputs (as at August 2026)

| Metric | 2026 | 2028 | 2030 | 2032 |
|--------|-----:|-----:|-----:|-----:|
| **Net Worth** | $2,233,904 | $2,850,297 | $3,530,806 | $4,266,874 |
| **Combined Net Debt** | $412,086 | $164,644 | –$87,699 | –$336,499 |
| **Combined Superannuation** | $798,141 | $1,006,949 | $1,260,547 | $1,557,451 |
| **Annual Surplus** | $73,129 | $49,030 | $56,450 | $64,256 |

### Saturation Status
The model tracks when offset accounts reach ceiling:
- **2029**: Alexander St offset saturates
- **2030**: Both offsets saturated (excess flows to mortgage principal)

## Recent Changes (v3)

### Bug Fixes
- **Broken formula references**: Earlier row insertions left formulas pointing to wrong cells.
  - **Resolution**: Rebuilt Projection and Dashboard sheets from scratch.

- **Salary compounding error**: Sue's salary was compounding from her reduced 2027 gap figure.
  - **Resolution**: Gap year now a one-off 2027 deduction; salary trajectory resumes intact from 2028.

### Improvements
- Updated St Kevin's fees to actual schedule ($37,596)
- Added saturation status row for offset account monitoring
- Clarified repayment and offset assumptions

## How to Use

1. Review the **Assumptions** tab to understand current settings
2. Check the **Dashboard** for a one-page summary
3. Explore the **Projection** tab for year-by-year detail
4. To model scenarios, change assumptions in the Assumptions tab — the rest recalculates automatically
