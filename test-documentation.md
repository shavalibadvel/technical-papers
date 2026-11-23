# Test Documentation

## 1. Test Scenarios
A one-line idea of what needs to be tested — a high-level "thing to check."
Example: "Verify a user can log in with valid credentials."
Used early in planning so you get a full picture of what to test without getting lost in detail.

## 2. Test Cases
The detailed step-by-step recipe for testing one specific thing — with steps, input, and expected result.
Example: open login page → enter `alice01` / `Pass@123` → click Login → expect Dashboard.
Used so testing is repeatable, consistent, and anyone can run the same test the same way.

## 3. Test Data
The actual values you feed into the system during testing — usernames, passwords, amounts, dates.
Example: valid login `alice01/Pass@123`, invalid login `alice01/wrongpass`, boundary amount `0, 1, 99999, 100000`.
Kept separate from test cases so it can be reused to test positive, negative, and edge cases.

## 4. Test Plan
The master blueprint for the whole testing effort — who, what, when, how, and with what resources.
It covers scope, approach, schedule, risks, and entry/exit criteria.
Used to keep the whole team aligned and to get formal sign-off before testing starts.

## 5. Test Execution Report
A summary of what actually happened when tests were run — how many passed, failed, or were blocked.
Example: 120 total, 100 passed, 15 failed, 5 blocked → 83% pass rate.
Used in status meetings to give a clear health check and support the go/no-go release decision.

## 6. Requirements Traceability Matrix (RTM)
A map that links each requirement to the test cases that verify it.
It instantly shows coverage gaps, such as requirements with no tests, and orphan tests, such as tests with no requirement.
Used to prove nothing was missed, support change impact analysis, and satisfy audits.
