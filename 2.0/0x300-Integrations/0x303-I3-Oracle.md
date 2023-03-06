# I3: Oracle

## Control Objective

If a project integrates with external Oracle smart contracts, it is necessary to approach them with limited trust and check that they do not introduce unexpected behavior into our system.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Oracle standard,
* The values transferred are additionally verified,
* Vulnerabilities identified in various Oracle implementations have been taken into account during implementation.

Category “I3” lists requirements related to the Oracle smart contract as one of the components with which the project integrates.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **I3.1** | Verify that there are no vulnerabilities associated with Oracle integration. |
| **I3.2** | Verify that, when using Uniswap TWAP as a price oracle, the period is long enough to make its manipulation unprofitable for the attacker (compared to the funds at potential risk). |
| **I3.3** | Verify that Oracle data is up-to-date. |
| **I3.4** | Verify that no spot oracle is used (e.g. spot price from Uniswap pool). |
| **I4.4** | Verify that, when using Uniswap V3 TWAP as price oracle, liquidity is high enough and is distributed widely across most of the price range. |
| **I4.5** | Verify that, the use a decentralized off-chain oracles unsusceptible to on-chain price manipulation attacks (e.g. Chainlink) is considered for low liquidity asset, ideally combining it with on-chain oracles to detect malicious values. |

## References

For more information, see also:

* [The Dangers of Price Oracles in Smart Contracts](https://www.youtube.com/watch?v=YGO7nzpXCeA)
* [TWAP Oracle Manipulation Risks, Mudit Gupta - DeFi Security Summit 2022](https://www.youtube.com/watch?v=Mu8ytTyStOU)
* [TWAP Oracles After the Merge, Mark Toda - DeFi Security Summit 2022](https://www.youtube.com/watch?v=mqrCvNgBXUk)
* [So you want to use a price oracle](https://samczsun.com/so-you-want-to-use-a-price-oracle/)
* [Pricing LP tokens | Warp Finance hack](https://cmichel.io/pricing-lp-tokens/)
* [Uniswap V3 tick price manipulation](https://medium.com/@hacxyk/we-rescued-4m-from-rari-capital-but-was-it-worth-it-39366d4d1812)
