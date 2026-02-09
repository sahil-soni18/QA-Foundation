# The Three Main Categories of Testing

## 1. Functional Testing

**Focus:** "What" the system does.
This verifies that the software functions according to the requirements. You already covered these!

* **Examples:** Unit, Integration, System, Sanity, and Smoke testing.
* **Key Question:** Does the "Submit" button save the data?

---

## 2. Non-Functional Testing

**Focus:** "How" the system behaves.
This checks the quality attributes of the software. A site might work perfectly for one user (Functional), but crash for 1,000 users (Non-Functional).

### Key Types of Non-Functional Testing:

* **Performance Testing:** Checking speed and response time.
* **Load Testing:** Testing the system's behavior under a specific expected load (e.g., 500 users at once).
* **Stress Testing:** Pushing the system to its breaking point to see how it recovers.
* **Usability Testing:** Checking how "user-friendly" the app is.
* **Security Testing:** Checking for vulnerabilities, hacks, and data leaks.
* **Reliability Testing:** Checking if the system can run without a crash for a long period.

---

## 3. Structural (White-Box) Testing

**Focus:** The internal logic and code structure.
While you mentioned "Maintenance," the third major pillar is actually **Structural Testing**. This is where you look at the code itself to ensure every path and branch is executed.

---

## Wait, where does Regression/Maintenance go?

Here is the direct correction for your notes: **Regression Testing is a technique, not a category.**

* **Maintenance Testing:** This is testing done on **existing** systems. It usually happens when you migrate a system to a new server or retire an old system.
* **Regression Testing:** This is performed **during** Maintenance AND **during** new development. It is the "safety net" used in all categories.

---

### Comparison Table: Functional vs. Non-Functional

| Feature | Functional Testing | Non-Functional Testing |
| --- | --- | --- |
| **Area** | Validates software actions. | Validates software performance/security. |
| **Requirement** | Based on Business Requirements. | Based on Customer Expectations (SLA). |
| **Ease of Manual** | Easy to do manually. | Very hard; usually requires tools (JMeter, LoadRunner). |
| **Example** | Checking the login logic. | Checking if the login takes less than 2 seconds. |

---

### A Real-World Scenario:

Imagine an **ATM machine**:

* **Functional:** If I enter the right PIN and ask for $50, does it give me $50?
* **Non-Functional (Performance):** Does it take 10 seconds or 10 minutes to give me that $50?
* **Non-Functional (Security):** Can someone else see my PIN?
* **Regression:** Now that we added a "Donate to Charity" button on the screen, does the "Withdraw Cash" button still work?
