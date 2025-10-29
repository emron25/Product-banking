Digital Banking: Coreless Saga Pattern Simulator

This project demonstrates a key architectural challenge in modern banking systems: maintaining transactional consistency (ACID) across multiple, independently deployed microservices using the Saga Pattern.

The simulation showcases a cross-service fund transfer (e.g., Checking to Savings) where the two accounts are managed by different, autonomous services, each with its own local database.

- Key Architectural Concepts Demonstrated

Coreless Hybrid Architecture: The design separates core ledger management (Checking and Savings balances) into distinct microservices.

Distributed Transactions (Saga Pattern): A single logical transfer is broken into local transactions orchestrated by a central component.

Compensation Logic: In case of a failure in a later step (e.g., the credit fails), a Compensating Transaction is automatically triggered to undo the successful previous step (rollback the debit), ensuring the overall system remains consistent.

- Features and Capabilities

Real-time Simulation: Visualize the multi-step transaction process, including simulated network latency.

Failure Injection: Users can intentionally simulate a failure in the credit step to observe the Saga's automatic rollback mechanism.

Trilingual UI: The application supports English, Persian (فارسی), and Arabic (العربية) with correct Right-to-Left (RTL) layout handling for localization standards.

Modern UI/UX: The interface uses a clean, dark-mode design inspired by modern digital wallet applications like Trust Wallet.

- How to Run the Simulator

This project is contained entirely within a single index.html file (or DigitalBankingSim.html).

Clone or download the repository.

Open the DigitalBankingSim.html file directly in any modern web browser.

Use the controls to run a transfer:

Success Scenario: Keep the "Simulate Failure" box unchecked.

Failure Scenario: Check the "Simulate Failure" box to test the compensation/rollback logic.
