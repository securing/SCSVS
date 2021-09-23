# V3: Blockchain data

## Control Objective

Smart contracts in public blockchains have no built-in mechanism to store secret data securely. It is important to protect sensitive data from reading by an untrusted actor.

Ensure that a verified contract satisfies the following high-level requirements:
* Data stored in smart contract is identified and protected,
* Secret data is not kept in blockchain as plaintext,
* Smart contract is not vulnerable due to data misrepresentation.

Category “V3” lists requirements related to the blockchain data of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **3.1** | Verify that any data saved in the contracts is not considered safe or private (even private variables). | 
| **3.2** | Verify that no confidential data is stored in the blockchain (passwords, personal data, token etc.). | 
| **3.3** | Verify that the list of sensitive data processed by the smart contract is identified, and that there is an explicit policy for how access to this data must be controlled and enforced under relevant data protection directives. | 
| **3.4** | Verify that there is a component that monitors access to sensitive contract data using events. | 
| **3.5** | Verify that contract does not use string literals as keys for mappings. Verify that global constants are used instead to prevent Homoglyph attack. | 
| **3.6** | Verify that there are no vulnerabilities associated with blockchain data. | 


## References

For more information, see also:

* [Homoglyph attack](https://github.com/Arachnid/uscc/tree/master/submissions-2017/marcogiglio)
