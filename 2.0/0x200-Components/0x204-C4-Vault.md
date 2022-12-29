# C4: Vault

## Control Objective

If a project builds a Vault smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Vault standard,
* Stores user funds securely,
* Vulnerabilities identified in various Vault implementations have been taken into account during implementation.

Category “C4” lists requirements related to the Vault smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C4.1** | Verify that there are no vulnerabilities associated with the Vault component. |
| **C4.2** | Verify that the user's balance is updated based on funds received and not funds sent. |
| **C4.3** | Verify that only the user has access to their funds unless they explicitly allow their funds to be managed. |
| **C4.4** | Verify that the user can safely withdraw their funds at any time, even during an emergency pause. |
| **C4.5** | Verify that if there is a Vault in the system, then users' funds are stored on it. |
| **C4.6** | Verify that shares are distributed in proportion to the user's deposited funds. |
| **C4.7** | Verify that the same amount of shares for different users allows the same amount of funds to be withdrawn. |
| **C4.8** | Verify that a user depositing the same amount earlier will get more rewards than the one who deposits the same amount later. |

## References

For more information, see also:

* [Vault | Solidity 0.8](https://www.youtube.com/watch?v=HHoa0c3AOqo)
* [EIP-4626](https://eips.ethereum.org/EIPS/eip-4626)
