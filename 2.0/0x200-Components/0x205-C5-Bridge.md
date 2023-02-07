# C5: Bridge

## Control Objective

If a project contains a Bridge smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Bridge standard,
* It is impossible to abuse the signature verification logic,
* Potential threats related to bridges are taken into consideration.

Category “C5” lists requirements related to the Bridge smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C5.1** | Verify that bridge requires all necessary values to be included in the message and signed: chain ids, receiver, amount, nonce. |
| **C5.2** | Verify that used signatures are invalidated to protect the bridge from replay attacks. |
| **C5.3** | Verify that the message hash generation algorithm is resistant to collision attacks. |
| **C5.4** | Verify that bridge includes source and destination chain identifiers in the signed message and correctly verifies them. |
| **C5.5** | Verify that bridge does not allow spoofing chain identifiers. |
| **C5.6** | Verify that bridge uses a nonce parameter to allow the same operation (the same sender, receiver, and amount) to be executed multiple times. |
| **C5.7** | Verify that signed message cannot be used in a different context (use domain separator from EIP-712). |
| **C5.8** | Verify that the case of 0 being returned by ecrecover function is handled securely. |
| **C5.9** | Verify that privileged contracts are separated from cross-chain relay calls. Attacker should not be able to cross-call the privileged contract. |
| **C5.11** | Verify each supported blockchain's finality is taken into account when settling relay calls. |
| **C5.12** | Verify that bridge disregards calls originating from different function than designed. |
| **C5.13** | Verify that bridge requires adequate amount of fees to process the message. |
| **C5.14** | Verify that the maximum gas consumption for relayed messages is limited or fully backed by sender (e.g., in terms of fee). |

## References
For more information, see also:
* [EEA Crosschain Security Guidelines Version 1.0](https://entethalliance.github.io/crosschain-interoperability/crosschainsecurityguidelines.html)
* [Open problems in cross-chain protocols](https://arxiv.org/pdf/2101.12412.pdf)
* [Cross Chain Awareness](https://docs.openzeppelin.com/contracts/4.x/api/crosschain)
* [The Dark Side of DeFi: Cross-Chain Bridge Hacks](https://quantstamp.com/blog/the-dark-side-of-defi-cross-chain-bridge-hacks/)
* [What Are Cross-Chain Smart Contracts?](https://blog.chain.link/cross-chain-smart-contracts/)
* [Aurora Inflation Spend Bugfix Review](https://medium.com/immunefi/aurora-infinite-spend-bugfix-review-6m-payout-e635d24273d)
* [WORMHOLE - REKT](https://rekt.news/wormhole-rekt/)
* [RONIN NETWORK - REKT](https://rekt.news/ronin-rekt/)
* [EIP-712: Ethereum typed structured data hashing and signing](https://eips.ethereum.org/EIPS/eip-712)
* [Learn EVM attacks - Bridges](https://github.com/coinspect/learn-evm-attacks#bridges)
* [Awesome Interoperability - bridges](https://docs.nomad.xyz/resources/awesome-interoperability)
* [PolyNetwork hack - privilege escalation via cross-chain call](https://research.kudelskisecurity.com/2021/08/12/the-poly-network-hack-explained/)
