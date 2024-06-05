# Optimizing Workforce Management: A Linear Programming Approach for ABLE Marketing

This project focuses on optimizing the workforce management for ABLE Marketing using a Linear Programming (LP) approach. The primary goal is to determine the optimal staffing schedule and hiring/firing policy for Sales Executives while meeting monthly demands and minimizing the total cost incurred by ABLE.

## Company Overview

**ABLE** is a dynamic marketing company based in Gandhinagar, Gujarat, India, specializing in providing comprehensive 360-degree marketing solutions. Established with a clear vision, ABLE has emerged as a key player in the industry, catering specifically to Real Estate Developers.

- **Mission**: To empower Real Estate Developers by offering strategic marketing solutions that alleviate the burden of sales management.
- **Vision**: A future where developers can focus solely on construction and quality enhancement, ensuring their sales needs are professionally handled.
- **Services**: Providing highly skilled Sales Executives to clients, specializing in the Real Estate sector.
- **Clientele**: Distinguished clientele with major real estate builders.
- **Employee Strength**: Around 80 dedicated professionals.
- **Financial Performance**: Impressive annual revenue, establishing ABLE as a financially robust entity.

## Problem Statement

During the next four months, ABLE must meet the following demands for Sales Executives:

- Month 1: 20 Sales Executives
- Month 2: 30 Sales Executives
- Month 3: 15 Sales Executives
- Month 4: 10 Sales Executives

At the beginning of month 1, ABLE has 10 Sales Executives. A Sales Executive is compensated $2000 per month, with up to 160 hours of regular work and up to 20 hours of overtime per month at $15 per hour. Hiring and firing costs are $2500 and $1500 per executive, respectively. There is also a holding cost of $1000 per unassigned Sales Executive at the end of each month.

## Model Setup

**Input Variables:**

- \( i \): Index for the month \( i \in \{1, 2, 3, 4\} \)
- \( D_i \): Demand for each month \( i \)
- \( E_i \): Existing Sales Executives each month \( i \)
- \( C \): Compensation cost
- \( H \): Hiring cost
- \( L \): Layoff cost
- \( U \): Unassigned cost
- \( O \): Overtime cost
- \( RH_i \): Regular work hours
- \( OH_i \): Overtime work hours

**Decision Variables:**

- \( X_{iC} \): Number of compensated executives
- \( X_{iH} \): Number of executives hired
- \( X_{iL} \): Number of executives laid off
- \( X_{iU} \): Number of unassigned executives

**Objective:**

Minimize the total cost:
\[ \text{min} \sum_{i} \left[ X_{iC} \cdot C + O \cdot OH_i + X_{iH} \cdot H + X_{iL} \cdot L + X_{iU} \cdot U \right] \]

**Constraints:**

- \( X_{iH} \geq 0 \) (Non-Negative)
- \( X_{iC} \geq 0 \) (Non-Negative)
- \( X_{iL} \geq 0 \) (Non-Negative)
- \( X_{iU} \geq 0 \) (Non-Negative)
- \( RH_i + OH_i \geq D_i \) (Regular work hours + Overtime hours should meet the demand)

## Solver Model

The LP model is solved using appropriate solver tools to find the optimal staffing schedule.

## Recommendations to ABLE

Based on the optimized analytical decision model tailored for ABLE, the following recommendations are proposed:

1. **Month 1**: Recruit an additional 10 executives to enhance operational efficiency.
2. **Month 2**: Hire 7 more executives, resulting in the maximum executive count of 27 across the four months. This strategy aims to generate 420 hours of overtime with the existing executive team.
3. **Month 3**: Due to fluctuations in demand, a workforce adjustment is necessary, involving the layoff of 12 employees.
4. **Month 4**: Recommend a workforce reduction of 15 employees, guided by prevailing market conditions.

Considering the fluctuations in hiring and firing, a more balanced approach is suggested. To navigate these fluctuations effectively, it is recommended that ABLE explores hiring executives on a contractual basis for specific projects. This strategy provides flexibility while ensuring the company's ability to adapt to changing demands without aggressive hiring and firing practices.

## Conclusion

This project demonstrates the application of Linear Programming to optimize workforce management for ABLE Marketing. By implementing the recommended strategies, ABLE can achieve significant cost savings and improve operational efficiency.

