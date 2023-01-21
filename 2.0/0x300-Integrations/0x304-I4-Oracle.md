# I4: Oracle

## Control Objective

TODO

Category “I4” lists requirements related to the Oracle smart contract as one of the components with which the project integrates.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **I4.1** | Verify that there are no vulnerabilities associated with Oracle integration. |
| **I4.2** | Verify that, when using Uniswap TWAP as price oracle, the time period is long enough to make its manipulation unprofitable for the attacker (compared to the funds at potential risk). |
| **I4.3** | Verify that Oracle data is up-to-date. |
| **I4.4** | Verify that, when using Uniswap V3 TWAP as price oracle, liquidity is high enough and is distributed widely accross most of the price range. |
| **I4.5** | Whenever possible, use decentralized offchain oracles unsucceptible to price manipulatino attacks (e.g. Chainlink), ideally adding a fallback onchain oracle. |

## References

For more information, see also:

* [The Dangers of Price Oracles in Smart Contracts](https://www.youtube.com/watch?v=YGO7nzpXCeA)
* [So you want to use a price oracle](https://samczsun.com/so-you-want-to-use-a-price-oracle/)
* [Pricing LP tokens | Warp Finance hack](https://cmichel.io/pricing-lp-tokens/)
* [Uniswap V3 tick price manipulation](https://medium.com/@hacxyk/we-rescued-4m-from-rari-capital-but-was-it-worth-it-39366d4d1812)