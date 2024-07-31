# Test Technique: State Transition Testing

## What is State Transition Testing?

**Definition:**
State Transition Testing is a black-box test design technique used to test the different states of a system and the transitions between those states. It is particularly useful for systems where the output depends on the sequence of previous inputs and the current state of the system.

**Purpose:**
- To ensure that the system behaves correctly as it transitions from one state to another.
- To identify defects related to state changes and transitions.

**Steps Involved:**
1. Identify the states of the system.
2. Identify the transitions between the states.
3. Create a state transition diagram or table.
4. Derive test cases based on the state transitions.

## Examples of State Transition Testing

### Example 1: ATM System

**Scenario:**
An ATM system transitions between different states based on user actions such as inserting a card, entering a PIN, and withdrawing cash.

**States:**
- Idle
- Card Inserted
- PIN Entered
- Cash Withdrawn

**State Transition Diagram:**

| Current State | Event           | Next State     |
|---------------|------------------|----------------|
| Idle          | Insert Card      | Card Inserted  |
| Card Inserted | Enter PIN        | PIN Entered    |
| PIN Entered   | Withdraw Cash    | Cash Withdrawn |
| Cash Withdrawn| Remove Card      | Idle           |

**Test Cases:**
- **Test Case 1:** Idle -> Insert Card -> Card Inserted -> Enter PIN -> PIN Entered -> Withdraw Cash -> Cash Withdrawn -> Remove Card -> Idle
- **Test Case 2:** Idle -> Insert Card -> Card Inserted -> Remove Card -> Idle
- **Test Case 3:** Idle -> Insert Card -> Card Inserted -> Enter PIN -> PIN Entered -> Remove Card -> Idle

### Example 2: Login System

**Scenario:**
A login system transitions between different states based on user actions such as entering a username, entering a password, and clicking the login button.

**States:**
- Logged Out
- Username Entered
- Password Entered
- Logged In

**State Transition Diagram:**

| Current State    | Event          | Next State       |
|------------------|-----------------|------------------|
| Logged Out       | Enter Username  | Username Entered |
| Username Entered | Enter Password  | Password Entered |
| Password Entered | Click Login     | Logged In        |
| Logged In        | Click Logout    | Logged Out       |

**Test Cases:**
- **Test Case 1:** Logged Out -> Enter Username -> Username Entered -> Enter Password -> Password Entered -> Click Login -> Logged In -> Click Logout -> Logged Out
- **Test Case 2:** Logged Out -> Enter Username -> Username Entered -> Click Logout -> Logged Out
- **Test Case 3:** Logged Out -> Enter Username -> Username Entered -> Enter Password -> Password Entered -> Click Logout -> Logged Out

### Example 3: Online Shopping Cart

**Scenario:**
An online shopping cart transitions between different states based on user actions such as adding items, removing items, and checking out.

**States:**
- Empty Cart
- Item Added
- Item Removed
- Checked Out

**State Transition Diagram:**

| Current State | Event       | Next State   |
|---------------|-------------|--------------|
| Empty Cart    | Add Item    | Item Added   |
| Item Added    | Remove Item | Item Removed |
| Item Removed  | Add Item    | Item Added   |
| Item Added    | Checkout    | Checked Out  |
| Checked Out   | Add Item    | Item Added   |

**Test Cases:**
- **Test Case 1:** Empty Cart -> Add Item -> Item Added -> Checkout -> Checked Out
- **Test Case 2:** Empty Cart -> Add Item -> Item Added -> Remove Item -> Item Removed -> Add Item -> Item Added
- **Test Case 3:** Empty Cart -> Add Item -> Item Added -> Remove Item -> Item Removed -> Checkout (invalid transition, should be handled)

---

These examples illustrate how State Transition Testing can be applied to various scenarios to ensure comprehensive testing of state changes and transitions, helping to identify defects related to state-dependent behavior.
