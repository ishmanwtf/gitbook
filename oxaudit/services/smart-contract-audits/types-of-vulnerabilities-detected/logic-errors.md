# Logic Errors

**Logic Errors** are mistakes in the design or implementation of a smart contract’s functionality. These errors cause the contract to behave incorrectly, even though it may run without throwing errors. Such issues often lead to unexpected outcomes, financial losses, or vulnerabilities.

#### **How They Work** <a href="#how-they-work" id="how-they-work"></a>

1.  **Incorrect Conditions:** Logic errors can occur when conditions in `if` or `require` statements are wrong. Example:



    ```
    solidity

    function withdraw(uint256 _amount) public {
        // Incorrect condition allows withdrawal even with insufficient balance
        if (balances[msg.sender] > _amount) {
            payable(msg.sender).transfer(_amount);
        }
    }
    ```
2.  **Flawed Loops or Calculations:** Errors in loops or arithmetic can result in incorrect outputs. Example:



    ```
    solidity

    function calculateReward(uint256 _staked) public pure returns (uint256) {
        return _staked / 0; // Division by zero leads to a revert
    }
    ```
3.  **Improper State Updates:** Forgetting to update contract state can cause inconsistencies. Example:



    ```
    solidity

    function transfer(address _to, uint256 _amount) public {
        require(balances[msg.sender] >= _amount, "Insufficient funds");
        // Missing balance update
        payable(_to).transfer(_amount);
    }
    ```

**Real-Life Impact**

Logic errors can lead to:

* Loss of funds or tokens.
* Contracts functioning in unintended ways.
* Exploitable vulnerabilities for attackers.
