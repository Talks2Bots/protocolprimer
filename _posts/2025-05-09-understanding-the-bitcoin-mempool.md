---
title: "Understanding the Bitcoin Mempool"
date: 2025-05-08
categories:
  - node-basics
tags:
  - Consensus
  - Mempool
  - Miners
  - Difficulty Adjustment
pin: true
excerpt: "Every Bitcoin node has its own mempool—its own view of unconfirmed transactions—shaped by the transactions it sees and the rules it enforces."
header:
  teaser: /assets/images/posts/understanding-the-bitcoin-mempool/mempool-image.png
  overlay_filter: 0.5
  overlay_color: "#333"
---

# Understanding the Bitcoin Mempool

When someone sends a Bitcoin transaction, it doesn't get added to the blockchain right away. First, it enters what's known as the mempool, short for "memory pool." The mempool is a temporary holding area for valid, unconfirmed transactions waiting to be included in a block.

But there isn't just one mempool. Every Bitcoin node maintains its own version. That means the transactions you see on a public site like [mempool.space](https://mempool.space) are simply the ones visible to the node that powers that site. Your own Bitcoin node may see a slightly different set of transactions, depending on its peers and policies.

If you run your own node—using Bitcoin Core, Bitcoin Knots, or through a platform like Umbrel or Start9—your node independently validates incoming transactions. It checks that each transaction is properly signed, that the inputs haven't already been spent, and that the fee is sufficient. If the transaction passes all checks, your node accepts it into its local mempool.

Once accepted, your node usually shares the transaction with its peers through a process called transaction relay. Other nodes perform their own validation, and if they also find the transaction valid, it's added to their mempools as well. This decentralized relay process is how transactions propagate through the Bitcoin network.

## How Miners Choose Transactions

Miners build blocks using the unconfirmed transactions in their own mempools. They are financially motivated to maximize the value of each block they mine. That value includes the block subsidy—newly minted bitcoin—as well as the sum of the transaction fees.

To make the most of the limited space in each block, miners prioritize transactions by fee rate, which is the fee paid per byte of transaction data. Higher fee-rate transactions are more likely to be included quickly, while low-fee transactions may remain unconfirmed for hours or even days.

Some mining pools may choose to include specific types of transactions for reasons other than profit, but in general, the selection process is driven by economics.

## Viewing the Mempool on Your Node

If you're using a plug-and-play node platform like Umbrel or Start9, you can explore your node's mempool directly through its web interface. Both platforms offer apps that visualize the mempool in real time.

On Umbrel, the "Mempool" app can be installed from the built-in app store. It shows you a list of unconfirmed transactions, organized by fee rate, size, and other details. Start9 offers similar functionality through its "Mempool Explorer" app.

These interfaces show you what your node sees—not what some external service sees. That means you're working with first-hand data from your own node's perspective.

## Your Node and the Rhythm of the Bitcoin Network

The Bitcoin network is designed to produce a new block approximately every ten minutes. This timing is enforced through a system called difficulty adjustment. Roughly every 2,016 blocks, the network recalibrates mining difficulty so that blocks continue to be discovered at a predictable rate, regardless of changes in total mining power.

Your node isn't mining blocks unless you've joined a mining pool, but it still plays a vital role. When a new block is found and broadcast to the network, your node verifies it. It checks the proof-of-work, confirms that all transactions follow the rules, and ensures the block builds properly on the one before it. If the block is valid, your node adds it to its own copy of the blockchain.

Using your node's interface, you can see:

- Unconfirmed transactions in your mempool, often visualized as projected future blocks
- Confirmed transactions inside mined blocks that are already part of the blockchain
- The tip of the chain and how many confirmations any transaction has

Running a node gives you direct insight into the heartbeat of the Bitcoin network. You're not relying on a third party—you're part of the system, helping to enforce the rules and keep the network decentralized.
