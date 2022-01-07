# G8: Denial of service

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* The contract logic prevents influencing the availability of the contract.

Category “G8” lists requirements related to the possible denial of service of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **G8.1** | Verify that there are no vulnerabilities associated with Denial of Service. | 
| **G8.2** | Verify that the contract does not iterate over unbound loops.  | 
| **G8.3** | Verify that self-destruct functionality is used only if necessary.  If it is included in the contract, it should be clearly described in the documentation. | 
| **G8.4** | Verify that the business logic does not block its flows when any of the participants is absent forever. | 
| **G8.5** | Verify that the contract logic does not disincentivize users to use contracts (e.g. the cost of transaction is higher than the profit). | 
| **G8.6** | Verify that expressions of functions assert or require have a passing variant. | 
| **G8.7** | Verify that if fallback function is not callable by anyone, it is not blocking the functionalities of contract |
| **G8.8** | Verify that there are no costly operations in a loop. | 
| **G8.9** | Verify that there are no calls to untrusted contracts in a loop. | 
| **G8.10** | Verify that if there is a possibility of suspending the operation of the contract, it is also possible to resume it. | 
| **G8.11** | Verify that if allow lists and list deny are used, it does not interfere with normal operation of the system. | 
| **G8.12** | Verify that there are no DoS caused by overflows and underflows. | 

## References

For more information, see also:

* [DASP 10: Denial of Service](https://www.dasp.co/#item-5)
* [Gas Limit and Loops](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#gas-limit-and-loops)
* [Gas Limit DoS on the Network via Block Stuffing](https://consensys.github.io/smart-contract-best-practices/known_attacks/#gas-limit-dos-on-the-network-via-block-stuffing)
* [DoS with Block Gas Limit](https://consensys.github.io/smart-contract-best-practices/known_attacks/#dos-with-block-gas-limit)
* [SWC-128 DoS With Block Gas Limit](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-128)
* [SWC-113 DoS with Failed Call](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-113)
* [Uncallable function example](https://github.com/ethereum/EIPs/issues/820#issuecomment-454021564)