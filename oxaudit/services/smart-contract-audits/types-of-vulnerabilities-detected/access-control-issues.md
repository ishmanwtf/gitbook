# Access Control Issues

**Access Control Issues** occur when a smart contract fails to properly restrict who can call certain functions. This can allow unauthorized users to perform sensitive operations, such as minting tokens, transferring ownership, or withdrawing funds.

## **How They Work** <a href="#how-they-work" id="how-they-work"></a>

1.  **No Restrictions:** If functions are not protected, anyone can call them. Example:

    ```
    solidity

    function mint(uint256 _amount) public {
        // Anyone can mint tokens
        totalSupply += _amount;
    }
    ```
2.  **Improper Authorization:** If authorization checks are incorrect or incomplete, attackers can bypass restrictions. Example:

    ```
    solidity

    function updateOwner(address _newOwner) public {
        // Missing restriction to allow only the current owner
        owner = _newOwner;
    }
    ```

## **Real-Life Impact** <a href="#real-life-impact" id="real-life-impact"></a>

Attackers can exploit access control flaws to:

* Take ownership of a contract.
* Mint or transfer tokens they shouldn’t have.
* Drain contract funds.
