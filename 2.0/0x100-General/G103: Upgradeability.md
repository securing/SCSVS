# G103: Upgradeability

## Control Objective

The ability to update business logic, parameters and expand the architecture of a project based on smart contracts is one of the areas particularly exposed to various risks. During the update, in addition to the many benefits and opportunities they bring, bugs may be introduced that were not previously present in contracts.

Ensure that your project satisfies the following high-level requirements:
* The update procedure includes an attempt to perform it on a local fork,
* Backward compatibility is maintained and contracts behave as intended,
* Users have the opportunity to see what changes may be introduced and are informed about them early enough so that they have time to react if necessary.

Category “G103” lists requirements related to the upgradeabilitiy of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **103.1** | Verify that there are no vulnerabilities associated with upgradeability. |
| **103.2** | Verify that the team has made an update attempt  at a fork of the main network and checked that everything works as expected on the local copy. |
| **103.3** | Verify that the upgrade process is executed by a multisig contract where more than one person must approve the operation. |
| **103.4** | Verify that timelocks are used for important operations so that the users have time to observe upcoming changes (please note that removing the potential vulnerability in this case may be more difficult). |
| **103.5** | Verify that *initialize()* can only be called once. |
| **103.6** | Verify that *initialize()* can only be called by an authorized role through appropriate modifiers (e.g. *initializer*, *onlyOwner*). |
| **103.7** | Verify if the update process is done in one transaction so that no one can front-run it. |
| **103.8** | Verify that upgradeable contracts have reserved gap on slots to prevent overwriting. |
| **103.9** | Verify that the number of reserved (as a gap) slots has been reduced appropriately if new variables have been added. |
| **103.10** | Verify that there are no changes in the order in which the contract state variables are declared, nor their types. |
| **103.11** | Verify if the new values returned by the functions are the same as in the previous version of the contract (e.g. *owner()*, *balanceOf(address)*). |

## References

For more information, see also:

* [Contract upgrade anti-patterns](https://blog.trailofbits.com/2018/09/05/contract-upgrade-anti-patterns)
* [Security in Upgrades of Smart Contracts](https://www.youtube.com/watch?v=5WE6PEc305w)