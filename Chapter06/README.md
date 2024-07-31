# Test Technique: Decision Table Testing

## What is Decision Table Testing?

**Definition:**
Decision Table Testing is a black-box test design technique used to determine the system's behavior based on different combinations of inputs and conditions. It is particularly useful for testing systems with complex business rules and logical relationships.

**Purpose:**
- To ensure that all possible combinations of inputs and their corresponding outputs are tested.
- To capture and verify the system's logic in a tabular form.

**Steps Involved:**
1. Identify the conditions (inputs) and actions (outputs).
2. Create a decision table with all possible combinations of conditions.
3. Define the corresponding actions for each combination.
4. Derive test cases based on the decision table.

## Examples of Decision Table Testing

### Example 1: Loan Approval System

**Scenario:**
A loan approval system considers two conditions: credit score (good or bad) and employment status (employed or unemployed). The actions are to approve or reject the loan.

**Conditions:**
- Credit Score: Good, Bad
- Employment Status: Employed, Unemployed

**Decision Table:**

| Credit Score | Employment Status | Loan Approval |
|--------------|-------------------|---------------|
| Good         | Employed          | Approve       |
| Good         | Unemployed        | Reject        |
| Bad          | Employed          | Reject        |
| Bad          | Unemployed        | Reject        |

**Test Cases:**
- **Test Case 1:** Good credit score, employed -> Approve
- **Test Case 2:** Good credit score, unemployed -> Reject
- **Test Case 3:** Bad credit score, employed -> Reject
- **Test Case 4:** Bad credit score, unemployed -> Reject

### Example 2: Online Shopping Cart Discount

**Scenario:**
An online shopping cart applies discounts based on the customer's membership status and the total purchase amount.

**Conditions:**
- Membership Status: Member, Non-Member
- Purchase Amount: >$100, ≤$100

**Decision Table:**

| Membership Status | Purchase Amount | Discount     |
|-------------------|-----------------|--------------|
| Member            | > $100          | 20% Discount |
| Member            | ≤ $100          | 10% Discount |
| Non-Member        | > $100          | 5% Discount  |
| Non-Member        | ≤ $100          | No Discount  |

**Test Cases:**
- **Test Case 1:** Member, purchase amount > $100 -> 20% Discount
- **Test Case 2:** Member, purchase amount ≤ $100 -> 10% Discount
- **Test Case 3:** Non-Member, purchase amount > $100 -> 5% Discount
- **Test Case 4:** Non-Member, purchase amount ≤ $100 -> No Discount

### Example 3: Employee Overtime Calculation

**Scenario:**
An employee's overtime pay is calculated based on their hours worked and their employment type (contractor or full-time).

**Conditions:**
- Employment Type: Contractor, Full-Time
- Hours Worked: >40 hours, ≤40 hours

**Decision Table:**

| Employment Type | Hours Worked | Overtime Pay      |
|-----------------|--------------|-------------------|
| Contractor      | > 40 hours   | 1.5x Hourly Rate  |
| Contractor      | ≤ 40 hours   | No Overtime Pay   |
| Full-Time       | > 40 hours   | 2x Hourly Rate    |
| Full-Time       | ≤ 40 hours   | No Overtime Pay   |

**Test Cases:**
- **Test Case 1:** Contractor, worked > 40 hours -> 1.5x Hourly Rate
- **Test Case 2:** Contractor, worked ≤ 40 hours -> No Overtime Pay
- **Test Case 3:** Full-Time, worked > 40 hours -> 2x Hourly Rate
- **Test Case 4:** Full-Time, worked ≤ 40 hours -> No Overtime Pay

---

These examples illustrate how Decision Table Testing can be applied to various scenarios to ensure comprehensive testing of all possible input combinations and their corresponding actions.
