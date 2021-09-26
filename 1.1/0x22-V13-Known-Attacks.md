# V13: Known attacks

## Control Objective

The _Known attacks_ category has a different form from the other categories. It covers all known attacks and link them to the requirements from other categories.

Category “V13” aims to ensure that a verified contract is protected from the known attacks.

## Security Verification Requirements

| # | Description | 
| --- | --- |
| **13.1** | Verify that the contract is not vulnerable to Integer Overflow and Underflow attacks.
|     | [5.1] Verify that the values and math operations are resistant to integer overflows. Use SafeMath library for arithmetic operations. |
|     | [5.2] Verify that the extreme values (e.g. maximum and minimum values of the variable type) are considered and does change the logic flow of the contract. |
| **13.2** | Verify that the contract is not vulnerable to Reentrancy attack.
|     | [4.5] Verify that the re-entrancy attack is mitigated by blocking recursive calls from the other contracts. Do not use *call* and *send* functions unless it is a must. |
| **13.3** | Verify that the contract is not vulnerable to Access Control issues.
|     | [2.1] Verify that the principle of least privilege exists - other contracts should only be able to access functions or data for which they possess specific authorization. |
|     | [2.2] Verify that new contracts with access to the audited contract adhere to the principle of minimum rights by default. Contracts should have a minimal or no permission until access to the new features is explicitly granted. |
|     | [2.3] Verify that the creator of the contract complies with the rule of least privilege and his rights strictly follow the documentation. |
|     | [2.4] Verify that the contract enforces the access control rules specified in a trusted contract, especially if the dApp client-side access control is present (as the client-side access control can be easily bypassed). |
|     | [2.5] Verify that there is a centralized mechanism for protecting access to each type of protected resource. |
|     | [2.6] Verify that the calls to external contracts are allowed only if necessary. |
|     | [2.7] Verify that visibility of all functions is specified. |
|     | [2.8] Verify that the initialization functions are marked internal and cannot be executed twice. |
|     | [2.9] Verify that the code of modifiers is clear and simple. The logic should not contain external calls to untrusted contracts. |
|     | [2.10] Verify that the contract relies on the data provided by right sender and contract does not rely on *tx.origin* value. |
|     | [2.11] Verify that all user and data attributes used by access controls are kept in trusted contract and cannot be manipulated by other contracts unless specifically authorized. |
|     | [2.12] Verify that the access controls fail securely including when a revert occurs. |
|     | [3.4] Verify that there is a component that monitors access to sensitive contract data using events. |
|     | [7.4] Verify that the contract does not check whether the address is a contract using extcodesize opcode. |
| **13.4** | Verify that the contract is not vulnerable to Silent Failing Sends and Unchecked-Send attacks.
|     | [4.6] Verify that the result of low-level function calls (e.g. *send*, *delegatecall*, *call*) from another contracts is checked. |
|     | [4.7] Verify that the third party contracts do not shadow special functions (e.g. *revert*). |
| **13.5** | Verify that the contract is not vulnerable to Denial of Service attacks.
|     | [7.3] Verify that the contract does not iterate over unbound loops. |
|     | [9.1] Verify that the self-destruct functionality is used only if necessary. |
|     | [9.2] Verify that the business logic does not block its flows when any of the participants is absent forever. |
|     | [9.3] Verify that the contract logic does not disincentivize users to use contracts (e.g. the cost of transaction is higher that the profit). |
|     | [9.4] Verify that the expressions of functions assert or require have a passing variant. |
|     | [9.5] Verify that if the fallback function is not callable by anyone, it is not blocking the functionalities of contract and the contract is not vulnerable to Denial of Service attacks. |
|     | [9.6] Verify that the function calls to external contracts (e.g. send, call) are not the arguments of require and assert functions. |
| **13.6** | Verify that the contract is not vulnerable to Bad Randomness issues.
|     | [7.5] Verify that the contract does not generate pseudorandom numbers trivially basing on the information from blockchain (e.g. seeding with the block number). |
| **13.7** | Verify that the contract is not vulnerable to Front-Running attacks.
|     | [8.7] Verify that the contract uses mechanisms that mitigate transaction-ordering dependence (front-running) attacks (e.g. pre-commit scheme). |
| **13.8** | Verify that the contract is not vulnerable to Time Manipulation issues.
|     | [8.6] Verify that the sensitive operations of contract do not depend on the block data (i.e. block hash, timestamp). |
| **13.9** | Verify that the contract is not vulnerable to Short Address Attack.
|     | [6.2] 	Verify that the length of passed address is determined and validated by smart contract. |
| **13.10** | Verify that the contract is not vulnerable to Insufficient Gas Griefing attack.
|     | [7.1] Verify that the usage of gas in smart contracts is anticipated, defined and have clear limitations that cannot be exceeded. Both, code structure and malicious input should not cause gas exhaustion. |
|     | [7.2] Verify that two types of the addresses are considered when using the send function. Sending Ether to contract address costs more than sending Ether to personal address. |
|     | [7.3] Verify that the contract does not iterate over unbound loops. |
|     | [7.4] Verify that the contract does not check whether the address is a contract using *extcodesize* opcode. |
|     | [7.10] Verify that the external keyword is used for functions that can be called externally only to save gas. |

## References

For more information, see also:

* [DASP - Top 10](https://dasp.co/)
* [Known Attacks](https://consensys.github.io/smart-contract-best-practices/known_attacks/)
