# C6: Bridge

## Control Objective

If a project contains an Bridge smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Bridge standard,
* It is impossible to abuse the signature verification logic,
* Potential threats related to bridges are taken into consideration.

Category “C6” lists requirements related to the Bridge smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C6.1** | Verify that bridge requires all necessary values to be included in the message and signed: chain ids, receiver, amount, nonce. |
| **C6.2** | Verify that used signatures are invalidated to protect bridge from replay attacks. |
| **C6.3** | Verify that message hash generation algorithm is resistant to collision attacks. |
| **C6.4** | Verify that bridge includes source and destination chains identifiers in the signed message and correctly verifies them. |
| **C6.5** | Verify that bridge does not allow to spoof chain identifier. |
| **C6.6** | Verify that bridge uses a nonce parameter to allow the same operation (the same sender, receiver and amount) to be executed multiple times. |

