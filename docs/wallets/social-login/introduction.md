---
title: Introduction
sidebar_position: 1
---

# Introduction

Web3 users must own and use a wallet to sign blockchain transactions. Setting up a wallet, self-managing and securing private keys is complex and error-prone for novice Web3 users. 

Custodial wallets may simplify key management for the user but it takes away privacy and ownership as a third party gains access to the user's keys and wallet funds. 

Social login brings the best of both worlds - users can have the simplicity and ease of onboarding Web3 apps like Web2 without giving up privacy, security or dealing with Web3 onboarding complexities.

<img src="/img/arcana/social-login.png" alt="Send SHM via UI" width="85%"/>

## Using Social Login

With social login, users can onboard the Web3 apps using popular Web2 authentication providers such as Google, Twitter or via email in a passwordless manner. Once authenticated, the user gets immediate access to a Web3 wallet which can be used to sign blockchain transactions.

To use social login, users do not need to set up any wallet themselves or install a browser extension. They simply need to use the Web3 apps that are integrated with the Arcana Auth SDK. 

To enable social login and allow users to access the embedded, non-custodial Arcana wallet, the Web3 app developers must do the following:

* Register the app and configure the social providers as login options using the Arcana Developer Dashboard.
* Install the Arcana Auth SDK.
* Integrate the Web3 app with the SDK and add code for onboarding users, performing Web3 wallet operations for authenticated users. 

Users can choose one of the configured login options for the Web3 app and log into the application. Once authenticated, they can access the built-in Arcana Wallet UI from within the app context and sign blockchain transactions. 

If required, developers can disable the built-in Arcana Wallet UI and plug in a custom wallet UI and allow the authenticated users to perform Web3 wallet operations seamlessly. Use the white-labeled SDK feature to plug in a custom wallet UI.

## Key Security & Privacy

Arcana Auth SDK uses a state-of-the-art, asynchronous distributed key generation (ADKG) protocol which allows users to have full control over their wallets and abstracts the complexity of cryptography. The user's key is never generated within the Arcana subsystem. Only an authenticated user can fetch key shares and generate the key locally, within the app context, to sign blockchain transactions. Arcana's ADKG system is very robust and it takes care of refreshing and repairing the key shares making it extremely hard for malicious parties to gain access to user's key shares and generate keys.

## Pre-configured Shardeum Network

By default, Shardeum Sphinx 1.x network is already pre-configured for use in apps that integrate with the Arcana Auth SDK.  Users can simply select Shardeum network out of the box from the dropdown in the Arcana Wallet UI.

Developers can also configure additional flavors of the Shardeum networks using the Arcana Developer Dashboard.

## References

* [Arcana Auth SDK Developers Quick Start Guide ](https://docs.arcana.network/auth-quick-start.html)
* [Arcana Wallet Users Guide](https://docs.arcana.network/user-guides/wallet-ui/index.html)
* [Arcana ADKG](https://docs.arcana.network/concepts/adkg.html#using-adkg-for-web3-keys)
