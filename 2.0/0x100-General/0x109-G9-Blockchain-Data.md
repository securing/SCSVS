# G9: Blockchain data

## Control Objective

Smart contracts in public blockchains have no built-in mechanism to store secret data securely. It is important to protect sensitive data from being read by an untrusted actor.

Ensure that a verified contract satisfies the following high-level requirements:
* Data stored in a smart contract is identified and protected,
* Secret data is not kept in blockchain as plaintext,
* Smart contract is not vulnerable due to data misrepresentation.

Category “G9” lists requirements related to the blockchain data of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **G9.1** | Verify that there are no vulnerabilities associated with blockchain data. | 
| **G9.2** | Verify that any data saved in contracts is not considered secure or private (even private variables). | 
| **G9.3** | Verify that no confidential data is stored in the blockchain (passwords, personal data, token etc.). | 
| **G9.4** | Verify that contract does not use string literals as keys for mappings. Verify that global constants are used instead to prevent Homoglyph attack. | 
| **G9.5** | Verify that contract does not generate pseudorandom numbers trivially basing on the information from blockchain (e.g. seeding with the block number or block timestamp). | 
| **G9.6** | Don't rely on block hash `block.blockhash(uint blockNumber)` for blocks older than 256 from curent block, as they always will have 0 value. |


## References

For more information, see also:

* [eth2book Randomness](https://eth2book.info/altair/part2/building_blocks/randomness)
* [Chainlink VRF](https://docs.chain.link/vrf/v2/introduction/)
* [Unencrypted Private Data On-Chain](https://swcregistry.io/docs/SWC-136)
* [Homoglyph attack](https://github.com/Arachnid/uscc/tree/master/submissions-2017/marcogiglio)
