# The Curse of Flobs — QA Testing Project

## Project Overview
This project contains testing documentation for **The Curse of Flobs** — a Unity-based game created in 5 days for a game jam.

The goal is to perform structured manual testing, including test case design, execution, and bug reporting.

---

## Game Description
The Curse of Flobs is a top-down 2D game where the player must fulfill a demon's demands to lift a curse from a village of Flobs. The game consists of a tutorial and 4 stages, each introducing new mechanics: farming, sacrificing flowers, negotiating with a demon, and making moral choices that lead to different endings.

---

## Test Environment
- Platform: PC (Windows Build)
- Engine: Unity 2022.3.62f
- OS: Windows 10 22H2
- Resolution: 1920×1080
- Testing type: Manual testing

---

## Scope of Testing
The following areas are covered:

- Core gameplay mechanics
- Player controls and inventory
- Tutorial flow and task progression
- Stage transitions and timer logic
- UI/UX behavior
- Game logic and win/lose conditions
- Visual and audio feedback

---

## Testing Approach
Testing is performed using:

- Test case-based testing
- Exploratory testing

---

## Test Cases

Test cases are documented in:

`test-cases/test_cases.md`

**Total: 43 test cases** across 7 modules:

| Module | Test Cases |
|---|---|
| Main Menu | 4 |
| Tutorial | 14 |
| Stage 1 | 9 |
| Stage 2 | 3 |
| Stage 3 | 9 |

Each test case includes:
- Test Case ID
- Title
- Priority
- Preconditions
- Steps
- Expected Result
- Actual Result (where applicable)
- Status (Pass / Fail / Blocked)

---

## Bugs Summary

- Total bugs: 16
- Critical: 0
- High: 3
- Medium: 5
- Low: 8

---

## Bug Reports

Bug reports are documented in:

`bug-reports/bug_reports.md`

Each bug report includes:
- Bug ID
- Title
- Severity
- Priority
- Environment
- Preconditions
- Steps to Reproduce
- Expected Result
- Actual Result
- Attachments
