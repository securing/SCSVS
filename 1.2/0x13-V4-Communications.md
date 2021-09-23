# V4: Communications

## Control Objective

Communications includes the topic of the relations between smart contracts and their libraries.

Ensure that a verified contract satisfies the following high-level requirements:
* The external calls from and to other contracts have considered abuse case and are authorized,
* Used libraries are safe and the state-of-the-art security libraries are used.

Category “V4” lists requirements related to the function calls between the verified contracts and other contracts out of the scope of the application.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **4.1** | Verify that libraries which are not part of the application (but the smart contract relies on to operate) are identified. | 
| **4.2** | Verify that contract does not use hard-coded addresses unless necessary. If the hard coded address is used, make sure that its contract has been audited. | 
| **4.3** | Verify that contracts and libraries which call external security services have a centralized implementation. | 
| **4.4** | Verify that *delegatecall* is not used with untrusted contracts. | 
| **4.5** | Verify that re-entrancy attack is mitigated by blocking recursive calls from other contracts. Do not use *call* and *send* function unless it is a must. | 
| **4.6** | Verify that the result of low-level function calls (e.g. *send*, *delegatecall*, *call*) from another contracts is checked. | 
| **4.7** | Verify that third party contracts do not shadow special functions (e.g. *revert*). | 
| **4.8** | Verify that there are no vulnerabilities associated with communications. | 


## References

For more information, see also:

* [Security Considerations: Sending and Receiving Ether](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#sending-and-receiving-ether)
* [DASP 10: Unchecked Return Values For Low Level Calls](https://www.dasp.co/#item-4)
* [SWC-107 Reentrancy](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-107)
* [SWC-112 Delegatecall to Untrusted Callee](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-112)

