# I1: Basic

## Control Objective

The spirit of composability introduces many integrations between different entities, creating complex and multi-level relationships at the same time. This environment can introduce complex logical vulnerabilities or issues related to bad assumptions due to too much trust in external components.

Ensure that the integration process satisfies the following high-level requirements:
* We integrate with a proven component that we consider trusted,
* Vulnerabilities identified in various Token implementations have been taken into account during implementation.

Category “I1” lists requirements related to each integration with any smart contract.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **I1.1** | Verify that there are no vulnerabilities associated with the Basic category. |
| **I1.2** | Verify if the team is known and can be held liable for abuses. |
| **I1.3** | Verify that the external contract you want to use has been audited. |
| **I1.4** | Verify that the external contract you want to use has been verified on blockchain explorer (e.g., etherscan).  |
| **I1.5** | Verify that the contract with which you are integrating has passed SCSVS. |
| **I1.6** | Verify that the address of the integrated contract is correct, up-to-date, and consistent with the project documentation. |
| **I1.7** | Verify if the external contract is upgradeable in a trusted manner. |
| **I1.8** | Verify that no untrusted party can change the contract's implementation. |
| **I1.9** | Verify that external contracts comply with the principle of minimum rights and that their access to special functions is enforced by the appropriate modifiers. |
| **I1.10** | Verify whether the structures (types) received from the external contract are known and handled. |
| **I1.11** | Verify that the smart contract attributes that can be updated by the external contracts (even trusted) are monitored (e.g. using events) and the procedure of incident response is implemented (e.g. the response to an ongoing attack). |
| **I1.12** | Verify that the external contracts (even trusted) that are allowed to change the attributes of the smart contract (e.g., token price) have the following limitations implemented: a threshold for the change (e.g. no more/less than 5%) and a limit of updates (e.g., one update per day). |
| **I1.13** | Verify that the address called via low-level call/delegatecall/staticcall exists (it will return *true* if the contract does not exist). |

## References

For more information, see also:

* TODO
