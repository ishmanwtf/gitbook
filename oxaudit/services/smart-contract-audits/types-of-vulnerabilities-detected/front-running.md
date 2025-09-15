# Front-Running

**Front-Running** is a blockchain attack where a malicious actor exploits the transparency of the transaction pool (mempool) to manipulate the order of transactions. This often involves submitting a higher gas fee to prioritize their transaction over others, gaining an unfair advantage.

## **How Front-Running Works** <a href="#how-front-running-works" id="how-front-running-works"></a>

1. **Observation in the Mempool:** All pending transactions are visible in the mempool before being mined. Attackers monitor these transactions for valuable operations (e.g., token swaps, arbitrage).
2. **Submitting a Competing Transaction:** The attacker submits their transaction with a **higher gas fee** to ensure it is mined **before** the original transaction.
3. **Execution Advantage:** By front-running, the attacker can manipulate prices, exploit vulnerabilities, or profit from arbitrage.

## **Example** <a href="#example" id="example"></a>

Imagine a user submitting a transaction to buy a token on a decentralized exchange (DEX):

* User: Buys 100 tokens at a price of 1 ETH per token.
* Attacker: Spots the transaction in the mempool and submits a **buy order** with a higher gas fee.
* Outcome: The attacker’s transaction is mined first, increasing the token price. The user ends up buying tokens at a higher price, while the attacker sells them at a profit.

## **Types of Front-Running Attacks** <a href="#types-of-front-running-attacks" id="types-of-front-running-attacks"></a>

1. **Trade Front-Running:** Exploiting trades on decentralized exchanges.
2. **Arbitrage Front-Running:** Taking advantage of arbitrage opportunities visible in pending transactions.
3. **Transaction Reordering:** Reordering transactions to prioritize a malicious one.
