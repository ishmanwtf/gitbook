# Common Layer 2 Vulnerabilities

Layer 2 solutions have specific vulnerabilities that don’t typically affect Layer 1 blockchains. Here are two common risks that projects should be aware of:

* **Bridge Vulnerabilities**:
  * Bridges are used to move assets between Layer 1 and Layer 2 (or between different Layer 2 solutions). They serve as a gateway for transferring tokens or data from one chain to another.
  * However, **bridges can be points of failure** because they manage valuable assets and complex operations. If a bridge has a vulnerability, it could allow attackers to steal or lock assets permanently.
  * Auditing bridges is critical to ensure that they are protected against attacks, operate reliably, and securely handle cross-chain transactions.
* **Data Availability and Consensus Risks**:
  * For a Layer 2 solution to work effectively, it needs a way to confirm that all transaction data is available and that all participants agree on the current state of the system (consensus).
  * However, maintaining **data availability** and **consensus** can be challenging, especially if the Layer 2 solution operates outside the main blockchain. If data becomes unavailable or consensus is lost, it can lead to issues like delays, incorrect balances, or even halted operations.
  * These risks highlight the importance of ensuring that Layer 2 systems have strong data verification processes and reliable consensus mechanisms. Auditing can reveal weak spots in these areas and help projects address them before they cause problems.
