# Integer Overflows/Underflows

**Integer Overflows** and **Underflows** occur when mathematical operations exceed the storage limits of a variable, causing unexpected behavior. These vulnerabilities allow attackers to manipulate values in ways that can break contract logic.\


## **How They Work** <a href="#how-they-work" id="how-they-work"></a>

1.  **Integer Overflow:** When a value exceeds the maximum limit of its data type, it wraps around to the minimum value. Example:

    ```
    solidity

    uint8 x = 255; // Max value for uint8
    x += 1;       // Overflow: x becomes 0
    ```
2.  **Integer Underflow:** When a value is reduced below the minimum limit of its data type, it wraps around to the maximum value. Example:

    ```
    solidity

    uint8 x = 0; // Min value for uint8
    x -= 1;     // Underflow: x becomes 255
    ```

## **Real-Life Impact** <a href="#real-life-impact" id="real-life-impact"></a>

Attackers exploit overflows/underflows to:

* Mint extra tokens.
* Bypass balance checks.
* Gain unauthorized access to funds.
