# Reentrancy Attacks

A **Reentrancy Attack** is a common vulnerability in smart contracts that occurs when a malicious contract repeatedly calls a function (often the `withdraw` function) in another contract **before the initial execution is complete**. This allows the attacker to drain funds from the vulnerable contract before it has a chance to update its state (like account balances).

## Key Problem in the Vulnerable Code

The vulnerable function performs **Interactions** (sending Ether) **before Effects** (updating the contract’s state). Here’s an example:

```
solidity

function withdraw(uint256 _amount) public {
    require(balances[msg.sender] >= _amount, "Insufficient balance");

    // Sending Ether before updating the balance (vulnerable)
    (bool success, ) = msg.sender.call{value: _amount}("");
    require(success, "Transfer failed");

    // Updating balance after sending Ether
    balances[msg.sender] -= _amount;
}
```

## **How Reentrancy Attacks Work** <a href="#how-reentrancy-attacks-work" id="how-reentrancy-attacks-work"></a>

1. **Setup:** The attacker deposits Ether into the vulnerable contract.
2. **Withdrawal:** The attacker calls the vulnerable contract’s `withdraw` function to withdraw their deposit.
3. **Reentrant Call:** During the withdrawal, the vulnerable contract sends Ether to the attacker’s contract. The attacker’s contract triggers a **reentrant call** to the `withdraw` function **before the vulnerable contract updates its balance**.
4. **Repeat and Drain:** The attacker repeats this process in a loop, withdrawing funds multiple times, until the vulnerable contract runs out of Ether.
