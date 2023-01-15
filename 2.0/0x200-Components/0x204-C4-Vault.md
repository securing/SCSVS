# C4: Vault

## Control Objective

If a project contains a Vault smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Vault standard,

Category “C4” lists requirements related to the Vault smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C4.1** | Verify that there are no vulnerabilities associated with the Vault component. |
| **C4.2** | Verify that depositing rounds down the assets and withdrawing rounds up. |
| **C4.3** | If the vault is supposed to support fee-on-transfer tokens, make sure to check for balance change rather than amount to be transferred. |
| **C4.4** | Be mindful of dangers of supporting rebasing tokens - most protocols (like Uniswap) prohibit using them, due to the problems with it's floating balance of owners. |
| **C4.5** | Verify that the vault is only allowed to transfer tokens from msg.sender, to prohibit stealing from other users who set the allowance for the contract |
| **C4.6** | Verify that the deposit and withdraw business logic is consistent and simmetric, especially when re-sending tokens to the same address (from == to). |

## References
For more information, see also:
* [ERC4626 Tokenized Vault Standard](https://academy.apeworx.io/articles/erc-4626-tokenized-vault-standard)
* [Securing ERC4626 Implementations](https://www.youtube.com/watch?v=5KVD7EX6HWQ)
* [Yearn Finance Vault Audit](https://github.com/yearn/yearn-security/blob/master/audits/20210719_ToB_yearn_vaultsv2/ToB_-_Yearn_Vault_v_2_Smart_Contracts_Audit_Report.pdf)
