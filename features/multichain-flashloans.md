---
description: RiftLend - your stress-free lending and borrowing experience
---

# Multichain Flashloans

**Core Concept**

A multichain flash loan allows users to borrow assets across multiple chains without collateral, as long as the borrowed amounts are repaid within the same transaction on each respective chain.

**Key Features**

* Decentralized Initiation
* User can trigger flash loans from any chain
* Request propagates to target chains via relayers
* Local Atomicity
* Each chain maintains atomic execution
* Funds must be repaid within same transaction on lending chain
* Not cross-chain atomic, but secured by per-chain validation
* Protocol as Lender
* Protocol itself acts as the lender
* Only requires small premium payment upon successful execution
* Failed repayments revert the entire transaction
* Security Benefits
* Transactions visible on-chain (vs private mempool flash loans)
* Protocol can implement monitoring and safety checks
* Can enforce borrowing caps to manage market risk

**Future Improvements**

* SuperchainAsset Integration
* Could eliminate need for underlying asset transfers
* Enable direct SuperchainAsset transfers for flash loans
* Simplify cross-chain flash loan targeting
* Bridge Integration
* Potential to integrate with bridge protocols
* Could enhance liquidity management
* Requires careful consideration of asset availability
