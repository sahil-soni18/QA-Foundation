# Integration Testing: Connecting the Dots

Once individual units are verified, they are combined and tested as a group. This phase exposes faults in the interaction between integrated units.

### Core Focus Areas

* **Interface Compatibility:** Ensuring Module A sends data in a format Module B understands.
* **API Communication:** Verifying that the application can successfully call internal or external APIs.
* **Database Integrity:** Checking if the application can correctly read from and write to the database.
* **Network/Service Latency:** Identifying issues that only appear when components talk over a network.

---

## Common Scenarios

* **The "Golden Path":** A user submits a form (Controller), which triggers business logic (Service), which then saves a record to the table (Database).
* **Third-Party Services:** Testing if your app correctly handles a response from a payment gateway like Stripe or PayPal.
* **Microservices:** Ensuring Service A can successfully request data from Service B.

---

## Integration Strategies

Not all integration testing is done the same way. There are three main approaches:

| Strategy | Description |
| --- | --- |
| **Big Bang** | All modules are integrated at once and then tested. (Risky, as it's hard to isolate the cause of a failure). |
| **Top-Down** | Testing starts from the top-level modules (UI/Controller) and works down to the database using "Stubs." |
| **Bottom-Up** | Testing starts from the lowest level (Database/Utilities) and works up using "Drivers." |

---

## Integration vs. Unit Testing

It's easy to confuse the two. Here is the main distinction:

* **Unit Test:** "Does my code correctly calculate the discount?"
* **Integration Test:** "Does the calculated discount actually get saved into the `Orders` table in the database?"

---

## Goals of Integration Testing

1. **Detect Interface Errors:** Finding bugs in how data is passed between modules.
2. **Validate System Flow:** Ensuring the end-to-end logic of a specific feature works.
3. **Identify Connectivity Issues:** Catching broken database connections or timed-out API calls early.

