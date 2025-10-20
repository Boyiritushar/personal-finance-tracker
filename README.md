🚀 My November 2025 Financial Toolkit

Welcome to my personal budget repository! This project is a straightforward way to track monthly income, manage expenses using the 50/30/20 principle, and project long-term investment growth. Think of this as the logic engine behind my financial decisions for November 2025.

The core data is contained in the spreadsheet extract: budgeting.xlsx - November 2025.csv.

1. The November Snapshot: Where the Money Goes

This section breaks down how my income is accounted for, right down to the final Rupee available for spending or saving.

A. Income & Financial Flow

The first step is always to figure out the Final Income—the money I actually have to budget with after my fixed contributions are handled. We start with the Total Income (the sum of all income sources, $\sum \text{Income Sources}$). From this, a fixed contribution of ₹4,000 is immediately deducted and labeled To House. The remainder is the Final Income ($\text{Total Income} - \text{To House}$), which is the true budget amount. Finally, Savings is calculated by subtracting the Total Expenses (the sum of all categorized items, $\sum \text{Expense Items}$) from the Final Income ($\text{Final Income} - \text{Total Expenses}$).

B. Budget Allocation: The 50/30/20 Rule

This is the strategic heart of the budget. I aim to split my Final Income into three buckets based on a 49%/20%/31% ratio (a variation of the standard 50/30/20 rule). The Goal Amount for each category is determined by multiplying the Final Income by its target percentage (e.g., Needs is $\text{Final Income} \times 0.49$).

Needs (49%): Covers essential living costs like rent and groceries.

Wants (20%): Accounts for non-essential spending like entertainment and dining.

Investments (31%): The fixed amount allocated solely for long-term wealth building.

2. Investment Growth: Planning for "Future Me"

This section outlines the strategy for growing the monthly Investment contribution over a 20-year Goal Period. The growth is assumed to be compounded monthly (12 Compounding Periods per year). The individual Allocation percentage for each asset (e.g., gold, stocks) is used alongside its Annual Expected Return to determine the overall portfolio performance.

The Financial Formulas

The growth projections rely on two main calculations, both explained using their core Excel function structure:

A. Blended CAGR Calculation

The first step is calculating the Blended CAGR (Compound Annual Growth Rate), which is the single, weighted-average annual return for the entire portfolio. It reflects the expected returns of individual assets based on how much money is allocated to each.

Mathematically, the Blended CAGR is the sum of (Asset Allocation $\times$ Asset Annual Returns), shown as $\sum (\text{Asset Allocation} \times \text{Annual Returns})$. Although the underlying spreadsheet logic sometimes uses a non-standard Excel structure to pull these weights (like =FV(rate, nper, 0, -present_value)), its purpose is always to calculate this weighted average, resulting in the final portfolio rate (e.g., 0.1270). This rate is then used in the Future Value projection.

B. Future Value (FV) Projection

This function projects what the total investment pot will be worth at the end of the 20-year term, assuming consistent monthly investments. It uses the Excel Future Value function for an annuity:

$$\text{FV} = \text{FV}(\text{rate}/12, \text{years}*12, -\text{monthly\_investment}, 0, 0)$$

Here’s what each part of the formula does:

rate/12: Divides the Blended CAGR (the annual rate) by 12 to get the precise monthly interest rate.

years*12: Calculates the Total Periods (Nper) by multiplying the 20-year goal period by 12 months, resulting in 240 payments.

-monthly\_investment: Represents the Monthly Payment (PMT), which is the fixed monthly investment contribution (e.g., ₹3038). It must be entered as a negative number because it is cash leaving the investor's pocket.

0: Sets the Present Value (PV) to zero, assuming the investor is starting without any existing lump sum.

0: Specifies that the payment is made at the end of each compounding period (month).****

