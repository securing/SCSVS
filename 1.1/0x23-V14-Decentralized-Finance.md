# V14: Decentralized Finance

## Control Objective

The Decentralized Finance (DeFi) is a concept with various financial applications deployed on blockchain using smart contracts. This category covers the security requirements for the constructions used by the DeFi applications such as lending pools, flash loans, governance, on-chain oracles, etc.  

Ensure that a verified contract satisfies the following high-level requirements:
* The assets controlled by decentralized finance are safe and cannot be withdrawed by an unauthorized person,
* The data sources for decentralized finance (e.g. oracles) cannot be manipulated.

Category “V14” lists requirements related to the contructions used by the decentralized finance solutions.

## Security Verification Requirements

| # | Description | 
| --- | --- |
| **14.1** | Verify that the lender's contract does not assume its balance (used to confirm loan repayment) to be changed only with its own functions.  
| **14.2** | Verify that the functions which change lender's balance and lend cryptocurrency are non-re-entrant if the smart contract allows to borrow the main platform's cryptocurrency (e.g. Ethereum). It blocks the attacks that update the borrower's balance during the flash loan execution. |
| **14.3** | Verify that the flash loan function can call only a predefined function on the receiver contract. If it is possible, define a trusted subset of contracts to be called. Usually, the sender (borrower) contract is the one to be called back. |
| **14.4** | Verify that the receiver's function that handles borrowed ETH or tokens can be called only by the pool and within a process initiated by the receiver's owner or other trusted source (e.g. multisig), if it includes potentially dangerous operations (e.g. sending back more ETH/tokens than borrowed). |
| **14.5** | Verify that the calculations of the share in a liquidity pool are performed with the highest possible precision (e.g. if the contribution is calculated for ETH it should be done with 18 decimals precision - for Wei, not Ether). The dividend must be multiplied by the 10 to the power of the number of decimals (e.g. dividend * 10**18 / divisor). |
| **14.6** | Verify that the rewards cannot be calculated and distributed within the same function call that deposits tokens (it should also be defined as non-re-entrant). That protects from the momentary fluctuations in shares. |
| **14.7** | Verify that the governance contracts are protected from the attacks that use flash loans. One possible security is to require the process of depositing governance tokens and proposing a change to be executed in different transactions included in different blocks. |
| **14.8** | Verify that, when using an on-chain oracles, the smart contract is able to pause the operations based on the oracle's result (in case of oracle has been compromised). |
| **14.9** | Verify that the external contracts (even trusted) that are allowed to change the attributes of the smart contract (e.g. token price) have the following limitations implemented: a thresholds for the change (e.g. no more/less than 5%) and a limit of updates (e.g. one update per day). |
| **14.10** | Verify that the smart contract attributes that can be updated by the external contracts (even trusted) are monitored (e.g. using events) and the procedure of incident response is implemented (e.g. the response to an ongoing attack). |
| **14.11** | Verify that the complex math operations that consist of both multiplication and division operations firstly perform the multiplications and then division. |
| **14.12** | Verify that, when calculating conversion price (e.g. price in ETH for selling a token), the numerator and denominator are multiplied by the reserves (see the *getInputPrice* function in *UniswapExchange* contract as an example). |

## References

For more information, see also:

* [Damn Vulnerable #DeFi](https://damnvulnerabledefi.xyz)
* [Damn vulnerable #DeFi Write-ups & lessons learned](https://drdr-zz.medium.com/write-ups-and-lessons-learned-from-damn-vulnerable-defi-caa95d2678ec)
* [Uniswap's getInputPrice function](https://github.com/Uniswap/uniswap-v1/blob/master/contracts/uniswap_exchange.vy#L106)
