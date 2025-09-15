# Tools and Techniques Used

OXAudit uses specialized tools and techniques to perform effective penetration testing. Below are two key methods that the OXAudit team employs:

* **Fuzz Testing**:
  * **What Is it**: Fuzz testing, or “fuzzing,” is a technique where the system is bombarded with random data to see if it breaks or behaves unexpectedly.
  * **How It's Works**: The testing tool inputs a large volume of random or unexpected data to various parts of the system (e.g., contract functions, APIs) to identify any weak points or bugs that may not be visible through standard testing.
  * **Why It’s Important**: Fuzz testing can expose vulnerabilities that regular testing might miss, such as crashes, memory leaks, or unexpected behaviors. This helps ensure the system is robust enough to handle unusual inputs and edge cases.
* **Social Engineering Simulations**:
  * **What Is It**: Social engineering simulations mimic attempts to manipulate people into giving up sensitive information, such as credentials or access.
  * **How It's Works**: OXAudit tests for social engineering vulnerabilities by simulating phishing emails, fake phone calls, or deceptive messages. This helps assess how well users and team members understand security risks and how they respond to suspicious messages.
  * **Why It’s Important**: Social engineering is a common method attackers use to bypass technical defenses by targeting human weaknesses. Testing against these threats ensures that everyone involved is aware of security best practices and can recognize potential scams.
