---
title: Quickstart
sidebar_position: 1
slug: /
---

# Quickstart

## Shardeum Overview

Shardeum is a blockchain that supports EVM smart contracts.

For more general information on Shardeum:

[What is Shardeum?](/introduction/what-is-shardeum)

## Cross Shard Composability with Linear Scaling

Shardeum is sharded, allowing the network to scale linearly with more nodes.
Horizontally scaling in this fashion allows for high transactions per second at low gas prices.

Find out more about Shardeum nodes:

[Shardeum Node Types](/node/types)

Running nodes:

[How to run a validator node](/Node/Run/Validator)

## Wallet Setup For Using Shardeum

You will need an EVM wallet like Metamask or use [Social Login](/wallets/social-login/introduction) to:

      -pay for transaction gas fees
      -transfer tokens
      -interact with smart contracts

For more info on Metamask, see [Metamask Introduction](/wallets/MetaMask/introduction).

>> **Social Login** allows users to onboard Web3 apps using popular Web2 authentication mechanisms and instantly, securely access an embedded, non-custodial Web3 wallet from within the context of a Web3 app. The user is **not required** to install a browser extension or generate and manage private keys to sign blockchain transactions. To enable the social login feature, Web3 app developers need to integrate the app with the Arcana Auth SDK. [Learn more...](/wallets/social-login/introduction)

## Fund Your Wallet With SHM On Shardeum

Find out how to get testnet tokens from our faucets here:

[Claim LIberty 100 SHM From Shardeum Faucets](/faucet/claim)

## Connect Wallet To Shardeum

Connect to Shardeum using the following network endpoints found here:

[Shardeum Endpoints](/network/endpoints)

Note: you can quickly connect your Metamask to Shardeum with:

[https://chainlist.org/?testnets=true&search=Shardeum](https://chainlist.org/?testnets=true&search=Shardeum)

## Reading Shardeum Transactions

View transactions on Shardeum using the Shardeum Explorer:

[Shardeum Explorer](/network/explorer)

## Deploy Contracts to Shardeum

Since Shardeum is EVM compatible, you can use the following frameworks to deploy to Shardeum:

[Remix IDE](/smart-contracts/deploy/remix)

[Foundry](/smart-contracts/deploy/foundry)

[Hardhat](/smart-contracts/deploy/hardhat)

[Truffle](/smart-contracts/deploy/truffle)

To deploy contracts at the same address cross chain:

[Same Address Cross Chain](/smart-contracts/deploy/same-address)

## Deploying Tokens To Shardeum

All EVM based token standards are supported on Shardeum (since Shardeum is EVM compatible).
Popular tokens supported on Shardeum:

[ERC-20 (Fungible Tokens)](/smart-contracts/tokens/ERC-20)

[ERC-721 (NFTs)](/smart-contracts/tokens/ERC-721)

[ERC-1155 (Token Emulator)](/smart-contracts/tokens/ERC-1155)

## Cross Shard Composability Communication With EIP-2930

Smart contract addresses that don't have the same prefix are deployed to different shards.
The EIP-2930 accessList is used for shard routing contracts on different shards and is automated inside Shardeum nodes. 

For more info on how the EIP-2930 accessList works on Shardeum:

[EIP-2930 Overview](/smart-contracts/eip-2930/multicall-contract)

## Integrate File Storage Into Shardeum

We recommend users to use decentralized file storage standards like IPFS and Filecoin.

Files stored on IPFS can be used in contracts to deploy contracts with CID values as shown in this example:

[IPFS and Filecoin](/storage/ipfs-and-filecoin)

## Oracles on Shardeum

Get off chain data securely on Shardeum using oracle providers.

[SupraOracles](/oracles/supraoracles)