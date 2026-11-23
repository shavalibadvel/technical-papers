# Bug Management

## 1. Bug Life Cycle
The journey of a bug from the moment it's found until it's closed.
Typical flow: New → Assigned → Open → Fixed → Retest → Closed (or Reopened / Rejected / Duplicate / Deferred).
Used in bug trackers (Jira, Bugzilla, Azure DevOps) so every bug has a clear owner, status, and history.

## 2. Bug Reporting
Writing a clear, complete record of a bug so a developer can fix it without asking questions.
A good report includes: title, environment, build, severity, priority, steps, expected vs actual, and evidence.
Used to make bugs reproducible and fixable on the first try, and to build a traceable audit trail.

## 3. Severity vs Priority
Severity = how badly the bug breaks the product (technical, set by the tester).
Priority = how urgently it should be fixed (business, set by the product owner).
They are different — a rare crash can be high severity but low priority, while a typo on the homepage can be low severity but high priority.

### 4. Reproduction Steps
The exact numbered recipe a developer follows to make the bug happen on their own machine.
They include preconditions, environment, and exact input values.
Used so bugs don't get closed as "can't reproduce" and so fixes can be verified the same way.

### 5. Expected vs Actual Results
Expected = what should happen according to the requirement or spec.
Actual = what really happened when the steps were run.
A bug exists exactly when Expected ≠ Actual — this pair is the proof that a defect is real.






