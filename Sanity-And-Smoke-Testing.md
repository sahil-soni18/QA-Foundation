Think of it this way: **Smoke testing** checks if the "engine" starts, while **Sanity testing** checks if a specific "repair" actually worked.

---

## 1. Smoke Testing (The "Build Verification" Test)

The name comes from hardware testing: when you plug in a new board, if you see smoke, you immediately unplug it—no further testing needed.

* **When:** Performed on a **new build** (a fresh version of the code) sent by developers.
* **Goal:** To verify that the **critical core functionalities** are working. If the smoke test fails, the QA team rejects the build and sends it back to developers immediately.
* **Scope:** Wide but shallow (covers the whole app, but not in detail).
* **Example:** Can the user log in? If they can't even log in, there is no point in testing the "Profile Edit" feature.

---

## 2. Sanity Testing (The "Bug Fix" Test)

Sanity testing is a subset of regression testing. It is performed after receiving a software build with minor code changes or bug fixes.

* **When:** Performed on a **stable build** after specific bugs have been fixed or small changes made.
* **Goal:** To verify that the specific bugs are fixed and that the logic for those features is "sane" (working as expected).
* **Scope:** Narrow and deep (focuses only on the changed components).
* **Example:** If a developer fixed a bug in the "Shopping Cart" total calculation, you only test the cart and checkout. You don't need to check the "Search" feature during a sanity test.

---

## Key Differences at a Glance

| Feature | Smoke Testing | Sanity Testing |
| --- | --- | --- |
| **Subset of** | Acceptance/Regression Testing | Regression Testing |
| **Objective** | To check the **stability** of the build. | To check the **rationality** of a fix. |
| **Scripted?** | Usually documented or automated. | Usually undocumented (informal). |
| **Analogy** | Does the car start and have tires? | Do the windshield wipers work now? |

---

## Where do they fit in the cycle?

1. **Developer** completes code and creates a "Build."
2. **Smoke Testing** is run.
* *Fails?* Build is rejected.
* *Passes?* Testing continues.


3. **General Testing** occurs; bugs are found and sent back.
4. **Developer** fixes bugs and sends a "New Build."
5. **Sanity Testing** is run to verify those specific fixes.

---

### Important "Level-Up" Concept: The Daily Build

In modern companies (using DevOps), **Smoke Tests are almost always automated.** Every time a developer saves code, the system automatically runs a "Smoke Suite" to ensure the main branch isn't broken. This is known as **Continuous Integration (CI).**

