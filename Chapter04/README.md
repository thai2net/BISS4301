# Test Technique: Equivalence Partitioning (EP)

## What is Equivalence Partitioning?

**Definition:**
Equivalence Partitioning (EP) is a software testing technique that divides the input data of a software application into partitions of equivalent data from which test cases can be derived. The idea is to identify classes of input conditions that are treated the same by the software, ensuring that one test case from each partition is enough to represent all data within that partition.

**Purpose:**
- To reduce the number of test cases to a manageable level while maintaining adequate test coverage.
- To identify both valid and invalid input conditions.

**Steps Involved:**
1. Identify the input domain of the application.
2. Divide the input data into partitions or classes where each partition is expected to be treated the same by the system.
3. Select representative values from each partition for testing.

## Examples of Equivalence Partitioning

### Example 1: Validating Age Input

**Scenario:**
A field accepts ages between 18 and 60 inclusive.

**Partitions:**
- Valid Partition: [18-60]
- Invalid Partition 1: Below 18
- Invalid Partition 2: Above 60

**Test Cases:**
- **Valid Test Case:** Age = 25 (within the valid range)
- **Invalid Test Case 1:** Age = 15 (below the valid range)
- **Invalid Test Case 2:** Age = 65 (above the valid range)

### Example 2: Password Length Validation

**Scenario:**
A password field must accept passwords that are between 8 and 12 characters long.

**Partitions:**
- Valid Partition: [8-12 characters]
- Invalid Partition 1: Less than 8 characters
- Invalid Partition 2: More than 12 characters

**Test Cases:**
- **Valid Test Case:** Password = "Password1" (9 characters, within the valid range)
- **Invalid Test Case 1:** Password = "Pass" (4 characters, below the valid range)
- **Invalid Test Case 2:** Password = "ThisIsAVeryLongPassword" (21 characters, above the valid range)

### Example 3: Input Field for a Month

**Scenario:**
A field accepts numeric input for months, where the valid months are 1 through 12.

**Partitions:**
- Valid Partition: [1-12]
- Invalid Partition 1: Less than 1
- Invalid Partition 2: Greater than 12

**Test Cases:**
- **Valid Test Case:** Month = 6 (within the valid range)
- **Invalid Test Case 1:** Month = 0 (below the valid range)
- **Invalid Test Case 2:** Month = 13 (above the valid range)

---

These examples illustrate how Equivalence Partitioning can be applied to different scenarios to create effective and efficient test cases by covering representative values from each partition.
