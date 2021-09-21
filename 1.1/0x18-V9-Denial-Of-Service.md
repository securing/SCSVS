# V9: Denial of service

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* The contract logic prevents influencing the availability of the contract.

Category “V9” lists requirements related to the possible denial of service of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **9.1** | Verify that the self-destruct functionality is used only if necessary. If it is included in the contract, it should be clearly described in the documentation. | 
| **9.2** | Verify that the business logic does not block its flows when any of the participants is absent forever.  | 
| **9.3** | Verify that the contract logic does not disincentivize users to use contracts (e.g. the cost of transaction is higher that the profit). | 
| **9.4** | Verify that the expressions of functions assert or require to have a passing variant. | 
| **9.5** | Verify that if the fallback function is not callable by anyone, it is not blocking the functionalities of contract and the contract is not vulnerable to Denial of Service attacks. | 
| **9.6** | Verify that the function calls to external contracts (e.g. *send*, *call*) are not the arguments of *require* and *assert* functions. | 
| **9.7** | Verify that the function declarations are callable by the used compiler version (see the *Uncallable function example* link below). |
| **9.8** | Verify that there are no vulnerabilities associated with availability. | 

## References

For more information, see also:

* [DASP 10: Denial of Service](https://www.dasp.co/#item-5)
* [Gas Limit and Loops](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#gas-limit-and-loops)
* [Gas Limit DoS on the Network via Block Stuffing](https://consensys.github.io/smart-contract-best-practices/known_attacks/#gas-limit-dos-on-the-network-via-block-stuffing)
* [DoS with Block Gas Limit](https://consensys.github.io/smart-contract-best-practices/known_attacks/#dos-with-block-gas-limit)
* [SWC-128 DoS With Block Gas Limit](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-128)
* [SWC-113 DoS with Failed Call](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-113)
* [Uncallable function example](https://github.com/ethereum/EIPs/issues/820#issuecomment-454021564)
