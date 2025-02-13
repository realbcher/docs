# Farm Allocation Algorithm

---

## What is a Farm Allocation Algorithm?

Most DEX's use a developer selected multiplier on yield farms to reward in a native token. TangoSwap has decided to do something else, and make this choice mathematical in a way to optimize amount of volume and ensure fairness of the platform. In essence, this means that the rewards from yield farming on TangoSwap are determined by the properties of the trading pairs and how they compare to each other.

## How does TangoSwap's algorithm work?

First, the top 30 pairs by volume are selected. We set an allocation floor of 0.25% (Currently 0.25 TANGO per block out of 100 total TANGO issuance per block) for each. The total volume of the pair over the preceeding month is multiplied by the volatility of the pair over the preceeding month.

[You can view the algorithm here](https://github.com/tangoswap-cash/tangoswap-analytics/blob/master/src/pages/pools/upcoming.js)

## Why was this algorithm selected?

We want to have an algorithm that closely matches risk-adjusted return of an asset to encourage maximum volume for TangoSwap.

The focus on volume over just liquidity is to ensure that xTANGO stakers are rewarded and that farm allocation cannot simply be due to unrealistically highly priced liquidity.

## How can my token get a farm?

Simply ensure your token has enough volume on TangoSwap to be in the top 30 pairs.
