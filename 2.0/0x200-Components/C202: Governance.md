# C202: Governance

## Control Objective

If a project contains a Governance smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Governance standard,
* The project is managed by a DAO or a multisig contract,
* Vulnerabilities identified in various Governance implementations have been taken into account during implementation.

Category “C202” lists requirements related to the Governance smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **202.1** | Verify that there are no vulnerabilities associated with Governance component. |
| **202.2** | Verify that Governance contract follows tested and stable Governance standard. |
| **202.3** | (DAO) Verify that the governance contract is protected from the attacks that use flash loans. |
| **202.4** | (DAO) Verify that the votes over taking actions by governance are counted correctly, in accordance with the documentation.  |
| **202.5** | (DAO) Verify that the delays associated with the enforcement of actions are consistent with those described in the documentation. |
| **202.6** | Verify that special actions that can be performed only by Governance are clearly marked in the documentation. |
| **202.7** | Verify that Governance cannot more than declare in the documentation. |
| **202.8** | Verify that the ownership transfer is a 2-step process where the candidate accepts it in a separate transaction and the previous owner does not lose privileges until it is done. |

## References

For more information, see also:

* [Strategies for Secure Governance with Smart Contracts](https://www.youtube.com/watch?v=GbDAmMdmh8Q)
