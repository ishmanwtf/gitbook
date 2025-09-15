# Denial of Service (DoS) Attacks

A **Denial of Service (DoS) Attack** is a malicious attempt to disrupt the normal operation of a smart contract, making it inaccessible or causing it to fail in performing its intended functions. Attackers exploit flaws in the contract logic or overwhelm it with excessive transactions.

## **How DoS Attacks Work** <a href="#how-dos-attacks-work" id="how-dos-attacks-work"></a>

1. **Gas Limit Exploitation:** Attackers create operations that exceed the block gas limit, causing transactions to fail. Example: A loop that processes a large number of operations.
2.  **Blocking Resources:** Attackers monopolize contract resources or logic, such as being the only recipient of rewards. Example:



    ```
    solidity

    function rewardWinner(address winner) public {
        require(msg.sender == owner, "Not authorized");
        payable(winner).transfer(prize);
    }
    ```

    If the `winner` address is a contract with a `fallback` function that always reverts, the reward transfer fails, blocking the function.
3. **Spamming Transactions:** Attackers flood the network with spam transactions targeting the contract, making legitimate transactions expensive or impossible.

## **Real-Life Impact** <a href="#real-life-impact" id="real-life-impact"></a>

* **Loss of Functionality:** The contract becomes inaccessible or unable to perform its main purpose.
* **High Gas Costs:** Users face increased gas costs to interact with the contract.
* **Funds Locked:** Assets may be permanently locked in the contract.

## **Types of DoS Attacks** <a href="#types-of-dos-attacks" id="types-of-dos-attacks"></a>

1. **Gas Limit DoS:** Exploiting high gas-consuming functions to exceed block limits.
2. **Storage Exhaustion DoS:** Overloading the contract with data to increase storage costs.
3. **Logic-Based DoS:** Exploiting poorly designed functions or specific edge cases.
