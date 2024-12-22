# Multichain Flashloans

Flash loans allow you to borrow any available amount of assets from the lending pool without providing any collateral. In our multichain implementation, flash loans are coordinated across chains but executed and repaid atomically within each individual chain.&#x20;

This powerful tool is ideal for advanced DeFi users seeking opportunities like arbitrage, refinancing, or liquidation strategies, all within a single transaction, while maintaining the protocol’s security and integrity.

## Key Features

1. **Decentralized Initiation**
   1. Users can trigger flash loans from any supported chain.
   2. Requests are propagated to the target chains using relayers, ensuring the protocol operates across multiple chains seamlessly.
2.  **Local Atomicity**

    1. Each chain ensures that the transaction is atomic locally—borrowed funds must be repaid within the same transaction on the lending chain.

    _**Note**: Transactions are validated independently on each chain for security and consistency, although they are not cross-chain atomic._
3. **Protocol as Lender**&#x20;
   1. RiftLend acts as the lender, eliminating the need for third-party providers.&#x20;
   2. Borrowers only pay a small premium if the flash loan is successfully executed.&#x20;
   3. If the loan is not repaid, the entire transaction is reverted, ensuring no risk to the protocol.

## Security Benefits

1.  **On-Chain Transparency**:

    Unlike private mempool flash loans, all transactions are visible on-chain, enhancing trust and transparency.
2.  **Monitoring and Safety Checks:**

    RiftLend implements real-time monitoring and safety mechanisms to protect the protocol.
3.  **Borrowing Caps**:

    Caps are enforced to manage market risk and prevent excessive borrowing that could destabilize liquidity pools.

Read more about Multichain Flashloans on our [GitHub](https://github.com/RiftLend/contracts-v1/blob/tabish/tests/packages/contracts/docs/MultichainFlashloans.md).
