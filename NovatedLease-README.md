# Novated Lease vs Car Loan Calculator

## Overview

This calculator compares the total cost of ownership between a **Novated Lease** and a traditional **Car Loan**, helping users determine which vehicle financing option saves them more money based on their individual circumstances.

---

## How It Works

### Novated Lease
A novated lease is a three-way agreement between you, your employer, and a finance company. Your employer deducts lease payments and running costs from your salary in two ways:
- **Pre-tax (Salary Sacrifice)** — reduces your taxable income
- **Post-tax (Employee Contribution Method)** — paid from after-tax income to reduce FBT

### Car Loan
A traditional car loan where you borrow money to purchase the vehicle and make repayments from your after-tax income. No tax benefits apply.

---

## Input Fields

### Your Income
| Field | Description |
|-------|-------------|
| Gross Annual Salary | Your total annual salary before tax |
| Medicare Levy Rate | Default 2% (standard rate) |

### Vehicle Details
| Field | Description |
|-------|-------------|
| Vehicle Type | Standard (20% FBT) or Electric Vehicle (0% FBT exempt) |
| Vehicle Cost (FBT Base) | Purchase price excluding GST |
| Vehicle Cost (inc GST) | Auto-calculated: FBT Base × 1.10 |

### Novated Lease Option
| Field | Description |
|-------|-------------|
| Lease Term | Duration in months (12-60) |
| Interest Rate (p.a.) | Annual interest rate for the lease |
| Residual Value % | Percentage of vehicle cost due at end of lease |
| Residual Amount | Auto-calculated: Vehicle Cost × Residual % |
| Monthly Lease Payment | Auto-calculated using PMT formula |
| Annual Lease Payment | Auto-calculated: Monthly × 12 |
| Monthly Total (inc. Running Costs) | Auto-calculated: Total annual costs ÷ 12 |

### Finance Option
| Field | Description |
|-------|-------------|
| Loan Term | Duration in months (12-84) |
| Interest Rate (p.a.) | Annual interest rate for the loan |
| Deposit | Upfront payment reducing loan principal |
| Balloon / Residual | Optional lump sum due at end of loan |
| Monthly Repayment | Auto-calculated using PMT formula |
| Annual Repayment | Auto-calculated: Monthly × 12 |

### Running Costs (Annual)
| Field | Description |
|-------|-------------|
| Fuel | Annual fuel expenses |
| Servicing | Annual service and maintenance |
| Tyres | Annual tyre replacement/rotation |
| Registration + CTP | Annual registration and compulsory third party insurance |
| Insurance | Annual comprehensive insurance |
| Management Fee | Novated lease administration fee |
| Roadside Assist | Annual roadside assistance |

---

## Calculations

### 1. Lease/Loan Payment (PMT Formula with Balloon)

```
Monthly Payment = (P - PV(B)) × [r(1+r)^n] / [(1+r)^n - 1]

Where:
P = Principal (loan amount)
B = Balloon/Residual amount
PV(B) = Present value of balloon = B / (1+r)^n
r = Monthly interest rate (annual rate / 12 / 100)
n = Number of months
```

### 2. Running Costs Calculation

```
Running Costs Subtotal = Fuel + Servicing + Tyres + Registration + Insurance + Management + Roadside
Subtotal (Lease + Running) = Lease Payment + Running Costs Subtotal
GST = Subtotal × 10%
Total Novated Lease Costs = Subtotal × 1.10
```

### 3. FBT and Employee Contribution (ECM)

```
FBT Rate:
- Standard Vehicle = 20%
- Electric Vehicle = 0% (FBT exempt)

Employee Contribution (ECM) = Vehicle Cost (FBT Base) × FBT Rate
```

### 4. Salary Sacrifice Calculation

```
Total Running Costs (inc GST)
− Employee Contribution (ECM)
= Net Cost

GST Input Credit = Net Cost ÷ 11

Salary Sacrifice Amount = Net Cost − GST Input Credit
```

### 5. Tax Calculations (2024-25 Australian Tax Rates)

#### PAYG Tax Brackets
| Taxable Income | Tax Rate |
|----------------|----------|
| $0 - $18,200 | 0% |
| $18,201 - $45,000 | 16% on excess over $18,200 |
| $45,001 - $135,000 | $4,288 + 30% on excess over $45,000 |
| $135,001 - $190,000 | $31,288 + 37% on excess over $135,000 |
| $190,001+ | $51,638 + 45% on excess over $190,000 |

#### Without Novated Lease
```
Taxable Income = Gross Salary
PAYG Tax = Calculated per brackets above
Medicare Levy = Gross Salary × Medicare Rate
Net Income = Gross Salary − PAYG − Medicare
```

#### With Novated Lease
```
Taxable Income = Gross Salary − Salary Sacrifice Amount
PAYG Tax = Calculated per brackets above (on reduced income)
Medicare Levy = Taxable Income × Medicare Rate
Net Income = Taxable Income − PAYG − Medicare
```

### 6. Savings Calculation

```
Income Tax Savings = (PAYG without − PAYG with) + (Medicare without − Medicare with)
GST Savings = GST Input Credit
Total Annual Savings = Income Tax Savings + GST Savings
```

### 7. Total Cost of Ownership (Over Full Term)

#### Car Loan
```
Total Loan Repayments = Monthly Payment × Loan Term
Total Running Costs = Annual Running Costs × (Loan Term ÷ 12)
Balloon Payment = As specified
Total Cost Over Term = Repayments + Running Costs + Balloon
```

#### Novated Lease
```
Total Pre-Tax Contributions = Salary Sacrifice × (Lease Term ÷ 12)
Total Post-Tax (ECM) = ECM × (Lease Term ÷ 12)
Residual Payment = Residual Amount × 1.10 (inc GST)
Gross Cost = Pre-Tax + Post-Tax + Residual

Total Tax Savings = Annual Tax Savings × (Lease Term ÷ 12)
Total GST Savings = Annual GST Savings × (Lease Term ÷ 12)

Net Cost Over Term = Gross Cost − Tax Savings − GST Savings
```

#### True Savings Comparison
```
True Savings = Car Loan Total Cost − Novated Lease Net Cost

If positive: You save with Novated Lease
If negative: You pay extra with Novated Lease
```

---

## Example Calculation

### Inputs
- Gross Salary: $80,000
- Vehicle Cost (FBT Base): $55,075
- Lease Term: 60 months
- Lease Interest Rate: 8.3%
- Residual: 28.13%
- Annual Running Costs: ~$5,500

### Results

#### Novated Lease
| Item | Amount |
|------|--------|
| Monthly Lease Payment | ~$860 |
| Annual Lease Payment | ~$10,315 |
| Total Running Costs (inc GST) | ~$17,382 |
| Employee Contribution (ECM) | $11,015 |
| GST Input Credit | $579 |
| Salary Sacrifice | $5,789 |

#### Tax Comparison
| Item | Without Lease | With Lease | Difference |
|------|---------------|------------|------------|
| Taxable Income | $80,000 | $74,211 | $5,789 |
| PAYG Tax | $14,788 | $13,051 | $1,737 |
| Medicare Levy | $1,600 | $1,484 | $116 |
| Net Income | $63,612 | $59,676 | -$3,936 |

#### Annual Savings
| Item | Amount |
|------|--------|
| Income Tax Savings | ~$1,853 |
| GST Savings | ~$579 |
| **Total Annual Savings** | **~$2,432** |

---

## Important Notes

1. **GST Treatment**: The calculator applies 10% GST to all running costs. In reality, Registration & CTP are GST-free, and insurance has complex GST treatment. This simplified approach matches industry-standard calculators like beCarWise.

2. **EV Exemption**: Electric vehicles are FBT-exempt (0% rate) if the vehicle value is below the luxury car tax threshold ($91,387 for 2024-25).

3. **Medicare Levy**: Uses a flat rate without accounting for low-income exemptions or Medicare Levy Surcharge.

4. **Residual Value**: At lease end, you must pay the residual to own the vehicle, refinance it, or return the vehicle.

5. **Reportable Fringe Benefits**: Salary sacrifice amounts become reportable fringe benefits, which may affect government benefits, HECS/HELP repayments, and child support calculations.

---

## Disclaimer

This calculator provides estimates only based on 2024-25 Australian tax rates (post Stage 3 tax cuts). Results may vary based on individual circumstances, employer arrangements, and specific lease terms. This is not financial advice. Please consult a qualified financial advisor or novated lease provider for figures specific to your situation.

---

## Technical Implementation

- **Built with**: HTML, CSS, JavaScript
- **No dependencies**: Runs entirely in the browser
- **Mobile responsive**: Adapts to all screen sizes
- **Real-time calculation**: Updates instantly as inputs change

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 2024 | Initial release with basic novated lease calculator |
| 2.0 | 2024 | Added EV toggle, finance comparison, total cost of ownership |
| 2.1 | 2024 | Added monthly total including running costs, improved savings comparison |
