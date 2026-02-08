# System vs. Acceptance Testing

At these stages, we stop looking at the code and start looking at the **product** from the perspective of a user.

## 1. System Testing: The "Full Picture"

System testing is a **Black-Box** testing type where the complete, integrated software is evaluated. The goal is to ensure the system meets its functional and non-functional requirements in an environment that mimics reality.

* **Focus:** End-to-end (E2E) workflows and "System-wide" behavior.
* **Environment:** A "Staging" or "Pre-production" environment that looks exactly like the real world.
* **Examples:**
* **The Happy Path:** User logs in  searches for a laptop  adds to cart  pays via credit card  receives a confirmation email.
* **Performance:** Does the whole system crash when 1,000 users check out at once?
* **Security:** Can a user access the "Admin" panel by changing a URL?



---

## 2. Acceptance Testing: The "Final Handshake"

This is the final level of testing before the software goes "Live." Its purpose isn't just to find bugs, but to prove that the software **delivers business value**.

* **Goal:** To gain confidence that the software is ready for deployment.
* **Key Question:** "Does this solve the problem the client paid us to solve?"

### Common Types of Acceptance Testing

| Type | Who Does It? | Where/When? |
| --- | --- | --- |
| **Alpha Testing** | Internal QA & Developers | At the developer’s site (Internal). |
| **Beta Testing** | Real Users/Customers | In the user's real environment (External). |
| **UAT (User Acceptance)** | Business Owners/Clients | Final check before signing off on the project. |

---

## Key Differences at a Glance

| Feature | System Testing | Acceptance Testing |
| --- | --- | --- |
| **Performed by** | Professional Testers (QA). | Users, Clients, and Product Owners. |
| **Objective** | Find technical bugs in the system. | Confirm the software is "fit for use." |
| **Based on** | Technical/System Specifications. | Business Requirements & User Needs. |
| **Example** | Does the "Checkout" button work? | Is the "Checkout" flow intuitive for a customer? |

---

## The Big Picture: Levels of Testing

To wrap up our journey through the levels, here is how they stack up:

1. **Unit:** Is this brick solid?
2. **Integration:** Do these two bricks stick together?
3. **System:** Is the whole wall straight and strong?
4. **Acceptance:** Does the customer like the color of the wall?

