# Conjure
[![Twitter Follow](https://img.shields.io/twitter/follow/ConjureFi?label=Conjure.Finance&style=social)](https://twitter.com/ConjureFi/)
CURRENTLY IN ALPHA WIP // DOCS SOON TO FOLLOW

Permissionless, flexible and robust framework for Oracle deployment with multifeed support, subscriptions and instant deployment.

## What is Open Oracle Framework (OOF)?

Open Oracle Framework’s a framework for permissionless oracle deployment and robust and flexible on-chain oracle feeds. Oracles are simply multi-party median value feeds, but you can even implement your own price logic through a dedicated proxy owner, which itself has it’s own price logic. The median value model takes the value for n signers, uses the median value submitted, makes sure that m signers for the m/n threshold has been met and returns the value. The oracle can require a small fee for subscriptions to feeds to cover gas fees, and are able to provide many feeds from 1 contract, allowing for highly efficient feed submission and retrieval. Oracles can set at the feed level if feeds are public, per feed subscription based (with unique pricing) or subscription pass based, allowing for adaptive models for revenue and use cases.

## Creating an Oracle and Feeds

### Step 1. Go to the factory at 
https://polygonscan.com/address/0x00f0fEED50926c27261dF37f7bCcC519d87525D0#writeContract
https://etherscan.com/address/0x00f0fEED50926c27261dF37f7bCcC519d87525D0#writeContract

### 2. Call oofMint
signers_ (address[]) - The singners for the oracle, these are responsible for feed updates, proposals and contract updates and earn fees

signerThreshold_ (uint256) - The minimum signers needed to submit a feed and takes the medium value submitted to authenticate a feed to update

payoutAddress_ (address) - Can be 0x0, in which case the fees will be split accross all signers or can be a set address to take all feeds, usable for cold wallets or gnosis/other contracts to handle the fees

subscriptionPassPrice_ (uint256) - The price to purchase a subscription for 28 days to all oracle feeds

### 3. https://github.com/ConjureFi/OOFNode to setup the node

### 4. You're all done, you're now providing onchain feeds using your own custom oracle!
