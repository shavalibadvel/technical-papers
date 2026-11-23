# Testing Approaches (by what you see)

## 1. Black Box Testing
Testing the software without looking at the code — you only care about inputs and outputs.
Example: enter a password and check if login works — you don't care how the code checks it.
Used for functional testing, UAT, and any test written from requirements or from a user's point of view.

## 2. White Box Testing
Testing the software with full knowledge of the internal code — you look at logic, branches, and paths.
Example: check that every `if/else` branch in a function is executed at least once.
Used by developers and SDETs for unit testing, code coverage, and finding hidden logic errors.

## 3. Grey Box Testing
A mix of black box and white box — you know some internals (like the database schema or APIs) but test mostly from the outside.
Example: test a login API knowing the token format, but without reading the API source code.
Used for integration testing, security testing, and API testing where partial knowledge helps design better tests.

---

# Testing Approaches (by intent)

## 4. Positive Testing
Testing with valid, expected inputs to confirm the system does what it *should* do.
Example: log in with correct username and password → expect successful login.
Used to verify that the happy path works — the most common real-world usage.

## 5. Negative Testing
Testing with invalid, unexpected, or malicious inputs to confirm the system fails gracefully.
Example: log in with a wrong password, empty fields, or SQL injection text → expect a clean error, not a crash.
Used to check robustness, error handling, and security — often where the most serious bugs hide.

---

# Test Design Techniques (how to pick test cases)

## 6. Boundary Value Analysis (BVA)
Testing the edges of an input range — the minimum, maximum, and just inside/outside values.
Example: if age must be 18–60, test 17, 18, 19, 59, 60, 61.
Used because most bugs live at the boundaries — off-by-one errors are extremely common.

## 7. Equivalence Partitioning (EP)
Splitting inputs into groups (partitions) where all values behave the same, then testing one value per group.
Example: age 18–60 is valid (test 30), age <18 is invalid (test 10), age >60 is invalid (test 70).
Used to reduce the number of test cases while still covering every kind of input — you don't need to test 100 values when 3 prove the same thing.

## 8. Decision Table Testing
Listing all combinations of conditions and the action the system should take for each, in a table.
Example: "Logged in? / Has permission? → Show admin menu?" → 4 combinations, each with an expected result.
Used for complex business rules with multiple conditions — it catches missed combinations and contradictory logic.

## 9. State Transition Testing
Testing how the system moves between states based on events — and that illegal transitions are blocked.
Example: Order states: Created → Paid → Shipped → Delivered. Test that you cannot go from Created straight to Delivered.
Used for workflows, order systems, login sessions, and any feature with a clear lifecycle.

