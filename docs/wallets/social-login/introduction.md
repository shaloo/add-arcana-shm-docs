---
title: Introduction
sidebar_position: 1
slug: /social-login-intro
---

# Introduction

Web3 app users are required to own and use a Web3 wallet to sign blockchain transactions. Setting up a self-managed wallet, securing private keys, and remembering cumbersome wallet addresses for different blockchain networks is complex, error-prone and very un-friendly for novice Web3 users.

Custodial wallet solutions may simplify the key management for a new Web3 user but it takes away privacy and ownership since a third party gains access to the user's keys and wallet funds.

**Social login** brings the best of both worlds together. The Web3 app users can experience the simplicity and ease of onboarding Web3 apps just like Web2 without giving up privacy, security or dealing with Web3 onboarding complexities.

<img src="/img/arcana/social-login.png" alt="Send SHM via UI" width="85%"/>

## Arcana Auth

The **Arcana Auth** product offers a seamless user onboarding experience with **social login** for Web3 apps. It enables developers to add user onboarding via popular Web2 authentication mechanisms (Google, Twitter, passwordless, etc.). Authenticated Web3 app users can securely access an embedded, non-custodial Web3 wallet from within the context of the app itself. 

Users of Web3 apps powered by Arcana Auth are **not required** to install a browser extension or generate and manage private keys or give up key ownership to a third party for signing blockchain transactions.

## Enable & Use Social Login

To **use** social login, users can simply log into the Web3 app that is already integrated with the Arcana Auth SDK. Once authenticated, users can access the Web3 wallet in the app's context.

To **enable** social login for onboarding users and allow authenticated users to easily access the embedded, non-custodial Arcana Wallet UI, the Web3 app developers must do the following:

* Register the app and configure the social providers as login options using the Arcana Developer Dashboard.
* Install the Arcana Auth SDK.
* Integrate the Web3 app with the SDK and add code for onboarding users, performing Web3 wallet operations for authenticated users. 

If required, developers can disable the built-in Arcana Wallet UI and plug in a custom wallet UI and allow the authenticated users to perform Web3 wallet operations seamlessly. Use the white-labeled SDK feature to plug in a custom wallet UI.

## Key Security & Privacy

Arcana Auth SDK uses a state-of-the-art, [asynchronous distributed key generation (ADKG)](https://docs.arcana.network/concepts/adkg.html) protocol which allows users to have full control over their wallets while abstracting the complexity of required cryptographic assets for Web3. The user's key is never generated within the Arcana subsystem. Only an authenticated user can fetch key shares from Arcana's ADKG system and generate the key locally, within the app context, to sign blockchain transactions. Arcana's ADKG system is very robust and it takes care of refreshing and repairing the key shares making it extremely hard for malicious parties to gain access to user's key shares and generate keys.

## Pre-configured Shardeum Network

By default, Shardeum Sphinx 1.x network is already pre-configured for use in apps that integrate with the Arcana Auth SDK.  Users can simply select the Shardeum network out of the box from the dropdown in the Arcana Wallet UI.

Developers can also configure additional flavors of the Shardeum networks using the Arcana Developer Dashboard.

<img src="/img/arcana/shm-chain-pre-config.gif" alt="Pre-configured chains" width="85%"/>

## References

* [Arcana Auth SDK Developers Quick Start Guide ](https://docs.arcana.network/auth-quick-start.html)
* [Arcana Wallet Users Guide](https://docs.arcana.network/user-guides/wallet-ui/index.html)
* [Arcana ADKG System](https://docs.arcana.network/concepts/adkg.html#using-adkg-for-web3-keys)
