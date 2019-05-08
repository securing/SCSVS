# V9: Denial of service

## Control Objective

Ensure that a verified contract satisfies the following high level requirements:
* Contracts logic prevents influencing the availability of contracts.

Category “V9” lists requirements related to the possible denial of service of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **9.1** | Verify that selfdestruct functionality is used only if neccessary. | 1.0 |
| **9.2** | Verify that the business logic does not block its flows when any of the participants is absent forever.  | 1.0 |
| **9.3** | Verify that the contract logic does not disincentivize users to use contracts (e.g. the cost of transaction is higher that the profit). | 1.0 |
| **9.4** | Verify that expressions of functions *assert* or *require* have a passing variant. | 1.0 |
| **9.5** | Verify that if fallback function is not callable by anyone, it is not blocking the functionalities of contract and the contract is not vulnerable to Denial of Service attacks. | 1.0 |
| **9.6** | Verify that the function calls to external contracts (e.g. *send*, *call*) are not the arguments of *require* and *assert* functions. | 1.0 |


## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
