# G3: Upgradeability

## Control Objective

The ability to update business logic, parameters and expand the architecture of a project based on smart contracts is one of the areas particularly exposed to various risks. During the update, in addition to the many benefits and opportunities they bring, bugs may be introduced that were not previously present in contracts.

Ensure that your project satisfies the following high-level requirements:
* The update procedure includes an attempt to perform it on a local fork,
* Backward compatibility is maintained and contracts behave as intended,
* Users have the opportunity to see what changes may be introduced and are informed about them early enough so that they have time to react if necessary.

Category “G3” lists requirements related to the upgradeabilitiy of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **G3.1** | Verify that there are no vulnerabilities associated with upgradeability. |
| **G3.2** | Verify that the team has made an update attempt at a fork of the main network and checked that everything works as expected on the local copy. |
| **G3.3** | Verify that the upgrade process is executed by a multisig contract where more than one person must approve the operation. |
| **G3.4** | Verify that timelocks are used for important operations so that the users have time to observe upcoming changes (please note that removing the potential vulnerability in this case may be more difficult). |
| **G3.5** | Verify that *initialize()* can only be called once. |
| **G3.6** | Verify that *initialize()* can only be called by an authorized role through appropriate modifiers (e.g. *initializer*, *onlyOwner*). |
| **G3.7** | Verify if the update process is done in one transaction so that no one can front-run it. |
| **G3.8** | Verify that upgradeable contracts have reserved gap on slots to prevent overwriting. |
| **G3.9** | Verify that the number of reserved (as a gap) slots has been reduced appropriately if new variables have been added. |
| **G3.10** | Verify that there are no changes in the order in which the contract state variables are declared, nor their types. |
| **G3.11** | Verify if the new values returned by the functions are the same as in the previous version of the contract (e.g. *owner()*, *balanceOf(address)*). |
| **G3.12** | Verify that the implementation is initialized. |
| **G3.13** | Verify that the implementation can't be destroyed. |

## References

For more information, see also:

* [Contract upgrade anti-patterns](https://blog.trailofbits.com/2018/09/05/contract-upgrade-anti-patterns)
* [Security in Upgrades of Smart Contracts](https://www.youtube.com/watch?v=5WE6PEc305w)