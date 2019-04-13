# V4: Communications

## Control Objective

Ensure that a verified contract satisfies the following high level requirements:
* TODO

Category “V4” lists requirements related to the function calls between the verified contracts and other contracts out of the scope of the application.

## Security Verification Requirements

| # | Description |  Since |
| --- | --- | --- | 
| **4.1** | Verify that libraries which are not part of the application (but the smart contract relies on to operate) are identified. | 1.0 |
| **4.2** | Verify that contract does not use hardcoded addresses unless necessary. If the hardcoded adress is used, make sure that its contract has been audited. | 1.0 |
| **4.3** | Verify that contracts and libraries which call external security services have a centralized implementation. | 1.0 |
| **4.4** | Verify that *delegatecall* is not used with untrusted contracts. | 1.0 |
| **4.5** | Verify that re-entrancy attack are mitigated by blocking recursive calls from other contracts. Do not use *call* and *send* function unless it is a must. | 1.0 |
| **4.6** | Verify that the result of low-level function calls (e.g. *send*, *delegatecall*, *call*) from another contracts is checked. | 1.0 |
| **4.7** | Verify that third party contracts does not shadow special functions (e.g. *revert*). | 1.0 |


## References

For more information, see also:

* TODO