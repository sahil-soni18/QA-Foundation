# Regression Testing

Regression testing is the process of re-testing a software application after changes have been made to ensure that the **existing functionality** still works correctly and that no new bugs have been introduced as a side effect.

> **The Mantra:** "Does the old stuff still work now that we've added the new stuff?"

---

## Your Example Breakdown (The "Domino Effect")

* **The Change:** Developer adds a Date Filter to the "View Balance" module.
* **The Expected Result:** User can see past balances.
* **The Regression Bug:** The "Transfer Money" module (which was never touched by the developer) starts using the "Filtered Balance" instead of the "Actual Balance."
* **Why it happened:** Both modules likely share a single variable or database query called `getBalance()`. The new filter modified this query globally.

---

## When do we perform Regression Testing?

It isn't just for new features. We run regression tests when:

1. **New Functionality** is added (your example).
2. **A Bug is Fixed** (to ensure the fix didn't break something else).
3. **Code is Refactored** (cleaning up code without changing what it does).
4. **Environment Changes** (updating the database version or the server OS).

---

## The Regression Testing Strategy

Since you can't test *everything* every time (remember: **Exhaustive testing is impossible**), teams usually choose one of these three paths:

| Strategy | Description |
| --- | --- |
| **Retest All** | Running every single test case in the suite. (Safest, but very slow and expensive). |
| **Regression Selection** | Picking only the test cases that are "related" to the modified area. |
| **Prioritization** | Testing the most critical features (e.g., Login, Payments) first. |

---

## Regression vs. Retesting (Common Confusion)

It is easy to mix these up, but they have different goals:

* **Retesting:** I found a bug, the developer "fixed" it, so I run the **exact same test** again to see if the bug is gone. (Checking the fix).
* **Regression Testing:** The bug is fixed, now I check **all the other related features** to make sure the fix didn't break them. (Checking the side effects).

---

## Regression and Automation

Regression testing is the **#1 candidate for automation**. Because these tests are repetitive and performed frequently (every time there is a code change), manual testers often get bored and miss things.

* **Tools used:** Selenium, Playwright, Cypress, or Appium.
* **The Goal:** A "one-click" suite that tells the team "The system is still healthy" in minutes.

