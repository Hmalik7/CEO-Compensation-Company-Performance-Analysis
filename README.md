# 📊 CEO Compensation Analysis Project

## 📜 Executive Summary

This repository contains comprehensive analysis of factors influencing CEO compensation across industries using data from PitchBook. The project examines the relationship between executive pay and various financial and market indicators to develop predictive models and insights for investors, boards, and policymakers.

## 🔍 Introduction

CEO compensation remains a central topic in corporate governance and financial research, generating significant discourse around fairness, performance incentives, and economic inequality. Executive pay structures typically integrate:

- Base salary
- Performance bonuses
- Stock options
- Long-term incentive plans

These components aim to align CEO interests with shareholder value. However, a fundamental question persists: **Is CEO pay primarily driven by company performance, or do other structural and market factors play a more significant role?**

Understanding these dynamics is essential for:
- 💼 Investors evaluating compensation justification
- 🏛️ Policymakers addressing governance concerns
- 🔖 Corporate boards designing effective pay structures

## 📚 Literature Review

Previous research has examined key drivers of executive compensation:

| Researchers | Year | Key Findings |
|-------------|------|--------------|
| Anderson, Banker, and Ravindran | 2000 | Firm size and growth opportunities significantly impact CEO salaries in the IT sector |
| Banerjee | 2022 | Global salary discrepancies exist across regions and industries |
| Bouteska, Sharif, and Zoghbi | 2024 | CEO pay linked to both firm performance and risk-taking behavior |
| Elsayed and Elbardan | 2018 | High-powered incentive structures often lead to earnings manipulation |

Despite these valuable insights, no widely accepted model accurately predicts CEO compensation across diverse industries and market conditions.

## ❓ Research Questions

This analysis focuses on two primary questions:

1. **What financial and market factors most strongly influence CEO compensation?**
2. **Can we develop a reliable predictive model to estimate CEO total compensation based on these indicators?**

## 🧮 Data & Methodology

### Data Source

Data was sourced from **PitchBook UW**, providing a comprehensive dataset of CEO compensation figures and company metrics.

### Variables

#### Dependent Variable:
- 💰 CEO Total Compensation

#### Independent Variables:

**Company Financials:**
- 📈 Total Revenue
- 👥 Revenue per Employee

**Profitability Metrics:**
- 📊 Return on Invested Capital (ROIC)
- 📊 Return on Assets (ROA)
- 📊 Net Profit Margin
- 📊 EBITDA Margin
- 📊 Revenue Growth

**Debt & Leverage:**
- 💳 Net Debt
- 💳 Debt to Capital Ratio
- 💳 Total Assets

**Market Indicators:**
- 📉 Price % Change YTD
- 🏢 Enterprise Value (EV)

**Categorical Factors:**
- 🗺️ HQ State/Province
- 🏭 Primary Industry Group
- 👔 CEO Attributes

### Data Preprocessing

Our methodology included rigorous data preparation:

1. **Data Cleaning:** Formatting column names and handling negative values (`ceo_data`)
2. **Missing Value Treatment:** Replacing null values with:
   - Median values for quantitative variables
   - Mode values for qualitative variables

This preprocessing yielded two analytical datasets:
- `ceo_data`: Clean dataset with NA values preserved
- `imputed_data`: Complete dataset with NA values replaced by median/mode

### Analytical Approach

The analysis employs multiple statistical techniques:

- 🔗 Correlation Analysis
- 📏 Multiple Linear Regression
- 📊 Data Visualization
- 🧪 Hypothesis Testing

## 🔬 Key Findings

### 📍 Geographic Analysis
- Illinois and California-based CEOs received the highest average compensation
- Nevada-headquartered companies showed the lowest CEO pay
- Headquarters location alone was not a strong predictor of compensation

### 🔗 Key Correlating Factors
Five financial factors showed the strongest relationships with CEO compensation:
- 🏢 **Enterprise Value (EV)** – Measure of total company worth
- 📊 **Revenue Per Employee** – Efficiency metric linking revenue to workforce size
- 👥 **Number of Employees** – Indicator of company size
- 💰 **Return on Invested Capital (ROIC)** – Profitability measure
- 📈 **Price % Change YTD** – Stock market performance indicator

### 📉 Regression Model Performance
- Multiple linear regression explained only 13.16% of variance (R² = 0.1316)
- Enterprise Value and Revenue Per Employee showed strongest positive relationships
- Residual analysis revealed non-linear patterns in the data
- Model struggled particularly with predicting higher compensation levels

### 🏭 Industry Comparison
- ANOVA test confirmed significant differences across sectors (p = 0.0191)
- Software, semiconductor, and computer hardware industries showed highest median CEO pay
- Results suggest industry-specific factors influence compensation structures

### 💳 Debt Level Analysis
- CEOs of highly leveraged firms earn significantly more ($12.48M vs $7.43M, p < 0.005)
- Suggests financial complexity and risk management responsibilities influence compensation

## 💭 Discussion & Implications

Our analysis reveals that while certain financial metrics correlate with CEO compensation, they don't fully explain the variations observed across companies. This suggests several important implications:

### 🧩 Complex Determinants
- Financial metrics alone explain only a modest portion of CEO pay variation
- Qualitative factors likely play significant roles:
  - Board composition and influence
  - CEO negotiation power
  - Corporate governance policies
  - Leadership qualities and reputation

### 🏢 Industry Dynamics
- High-tech sectors (software, semiconductors, hardware) show elevated compensation levels
- Likely reflects intense competition for executive talent in these industries
- Industry-specific performance metrics may be more relevant than cross-industry comparisons

### ⚖️ Risk-Reward Relationship
- Higher compensation in high-debt firms suggests a risk premium for managing financial complexity
- CEOs taking on greater financial risk appear to be compensated accordingly

### 📊 Modeling Limitations
- Linear models inadequately capture CEO compensation dynamics
- Advanced techniques (decision trees, random forests, machine learning) would likely improve predictive power
- Future models should incorporate non-financial variables

## 📋 Applications & Stakeholder Insights

Our findings provide actionable insights for multiple stakeholders:

- **Investors:** 
  - Better evaluate whether compensation aligns with performance
  - Identify potential red flags when CEO pay significantly deviates from predicted values

- **Corporate Boards:** 
  - Design more effective performance-driven pay structures
  - Benchmark compensation against relevant industry peers
  - Consider financial complexity when designing packages

- **Policymakers & Regulators:** 
  - Develop more nuanced approaches to compensation oversight
  - Ensure transparency in pay practices
  - Address potential governance risks

- **Researchers:** 
  - Foundation for further investigation into non-financial determinants
  - Exploration of non-linear modeling approaches

## ⚠️ Limitations

1. **Data Scope** – Analysis primarily uses publicly available financial data, potentially missing insights from private companies
2. **Missing Variables** – Did not include CEO tenure, stock ownership, or leadership attributes
3. **Linear Approach** – Initial modeling may not capture complex, non-linear relationships
4. **Temporal Factors** – Analysis provides a snapshot but may not capture evolving compensation trends

## 🛠️ Technical Implementation

This project is implemented using:

- **Programming Language:** [R/Python]
- **Key Libraries:** [Data manipulation and statistical libraries]
- **Visualization Tools:** [Visualization packages]

## 👥 Contributors

- **Harsh Malik**
- **Sai K**
- **Inaya R**
- **Anushna G**

## 📎 References

Anderson, M., Banker, R., & Ravindran, S. (2000). Executive compensation in the information technology industry.

Banerjee, A. (2022). Global salary discrepancies: A comparative analysis.

Bouteska, A., Sharif, T., & Zoghbi, G. (2024). CEO compensation, firm performance and risk-taking behavior.

Elsayed, N., & Elbardan, H. (2018). Investigating the associations between executive compensation and firm performance.

---

*This research contributes to the broader conversation on executive compensation by employing data-driven methods to examine how financial and market indicators shape CEO pay structures across industries.*
