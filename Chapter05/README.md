# Test Technique: Boundary Value Analysis (BVA)

## What is Boundary Value Analysis?

**Definition:**
Boundary Value Analysis (BVA) is a software testing technique that focuses on the boundaries between partitions. Instead of choosing any element from an equivalence class, BVA selects elements at the edges of the equivalence class. The rationale is that errors are more likely to occur at the boundaries of input ranges rather than in the middle.

**Purpose:**
- To identify defects that occur at the boundary edges of input domains.
- To ensure that the system handles edge conditions correctly.

**Steps Involved:**
1. Identify the boundaries of the input domain.
2. Create test cases at the boundaries, just inside the boundaries, and just outside the boundaries.

## Examples of Boundary Value Analysis

### Example 1: Validating Age Input

**Scenario:**
A field accepts ages between 18 and 60 inclusive.

**Boundaries:**
- Lower Boundary: 18
- Upper Boundary: 60

**Test Cases:**
- **Lower Boundary:** Age = 18 (exact boundary)
- **Just Below Lower Boundary:** Age = 17
- **Just Above Lower Boundary:** Age = 19
- **Upper Boundary:** Age = 60 (exact boundary)
- **Just Below Upper Boundary:** Age = 59
- **Just Above Upper Boundary:** Age = 61

### Example 2: Password Length Validation

**Scenario:**
A password field must accept passwords that are between 8 and 12 characters long.

**Boundaries:**
- Lower Boundary: 8 characters
- Upper Boundary: 12 characters

**Test Cases:**
- **Lower Boundary:** Password = "Passwrd1" (8 characters)
- **Just Below Lower Boundary:** Password = "Passwrd" (7 characters)
- **Just Above Lower Boundary:** Password = "Password" (9 characters)
- **Upper Boundary:** Password = "Passwrd12345" (12 characters)
- **Just Below Upper Boundary:** Password = "Passwrd1234" (11 characters)
- **Just Above Upper Boundary:** Password = "Passwrd123456" (13 characters)

### Example 3: Input Field for a Month

**Scenario:**
A field accepts numeric input for months, where the valid months are 1 through 12.

**Boundaries:**
- Lower Boundary: 1
- Upper Boundary: 12

**Test Cases:**
- **Lower Boundary:** Month = 1 (exact boundary)
- **Just Below Lower Boundary:** Month = 0
- **Just Above Lower Boundary:** Month = 2
- **Upper Boundary:** Month = 12 (exact boundary)
- **Just Below Upper Boundary:** Month = 11
- **Just Above Upper Boundary:** Month = 13

---

These examples illustrate how Boundary Value Analysis can be applied to different scenarios to create test cases that focus on the boundaries of input domains, ensuring comprehensive testing of edge conditions.
