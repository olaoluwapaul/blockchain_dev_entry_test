# Part B: Test Scenarios Guide

**Contract Name:** [SkillsMarketplace / SecureLottery]  

---

## Writing Effective Tests - Step by Step

1. **Understand the Contract**: First review all functions in your contract
2. **Identify Key Behaviours**: What should work correctly? What could go wrong?
3. **Plan Test Cases**: For each important behaviour, plan:
   - Happy path (normal operation)
   - Edge cases (unusual but possible situations)
   - Attack scenarios (potential vulnerabilities)

## Test Scenario 1: Happy Path (Example Template)

**Description**:  
Test normal operation where everything works as expected

**Steps to Follow**:
1. Call function X with valid parameters
2. Check contract state changes
3. Verify emitted events (if any)

**Expected Result**:  
- State should update correctly
- No errors should occur
- Events should match expected values

**Testing Tip**: Start with happy paths before moving to edge cases

---

## Test Scenario 2: Security Testing (Example Template)

**Description**:  
Verify your contract's protection against common vulnerabilities

**Common Vulnerabilities to Test**:
- Reentrancy attacks
- Integer overflows/underflows
- Access control issues
- Front-running

**Testing Approach**:
1. Identify a potential vulnerability in your contract
2. Write a test that attempts to exploit it
3. Verify your safeguards work:
   - Require statements
   - Modifiers
   - Proper state updates

**Example Test Case**:
1. Attempt to withdraw funds twice in a reentrancy attack
2. Check that contract:
   - Locks state during execution
   - Prevents double spending
   - Emits correct error messages

---

## Test Scenario 3: Edge Case Testing (Example Template)

**Description**:  
Test how your contract handles unusual but possible situations

**Common Edge Cases to Consider**:
- Minimum/maximum values (0, max uint, etc.)
- Empty inputs or states
- Boundary conditions
- Unexpected sequences of operations

**Testing Approach**:
1. Identify a potential edge case in your contract
2. Write a test that triggers this condition
3. Verify your contract:
   - Handles it gracefully
   - Maintains correct state
   - Provides clear error messages if needed

**Example Test Case**:
1. Attempt to transfer 0 tokens
2. Check that contract:
   - Doesn't fail
   - Doesn't change balances
   - Emits appropriate event (if any)

---

**Total Test Scenarios:** 3  
**Coverage Assessment:** After writing your tests, calculate what percentage of contract functionality they cover. For each contract:
1. List all functions and modifiers
2. Check which ones are tested
3. Calculate: (Tested Items / Total Items) * 100

Aim for at least 80% coverage. Include:
- Edge cases
- Error conditions
- All state transitions