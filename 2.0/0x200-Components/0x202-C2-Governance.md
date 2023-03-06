# C2: Governance

## Control Objective

If a project contains a Governance smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Governance standard,
* The project is managed by a DAO or a multisig contract,
* Vulnerabilities identified in various Governance implementations have been taken into account during implementation.

Category “C2” lists requirements related to the Governance smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C2.1** | Verify that there are no vulnerabilities associated with the Governance component. |
| **C2.2** | Verify that Governance contract follows tested and stable Governance standards. |
| **C2.3** | (DAO) Verify that the governance contract is protected from the attacks that use flash loans. |
| **C2.4** | (DAO) Verify that the votes over taking actions by governance are counted correctly, following the documentation.  |
| **C2.5** | (DAO) Verify that the delays associated with the enforcement of actions are consistent with those described in the documentation. |
| **C2.6** | (DAO) Verify that the actions can only be performed after voting is completed (unless explicitly stated otherwise in the documentation).
| **C2.7** | (DAO) Verify that the actions can be performed only following the voting result (voted yes - must be performed, voted no or not obtaining the required number of votes - cannot be performed).
| **C2.8** | Verify that special actions that can be performed only by Governance are marked in the documentation. |
| **C2.9** | Verify that the Governance cannot do more than declared in the documentation. |
| **C2.10** | Verify that the ownership transfer is a 2-step process where the candidate accepts it in a separate transaction and the previous owner does not lose privileges until it is done. |
| **C2.11** | Verify that key operations on the Governance contract can only be performed with the appropriate permissions. Functions in this contract should not be available to general users.|

## References

For more information, see also:

* [Strategies for Secure Governance with Smart Contracts](https://www.youtube.com/watch?v=GbDAmMdmh8Q)
* [MakerDAO Governance Module](https://docs.makerdao.com/smart-contract-modules/governance-module)
