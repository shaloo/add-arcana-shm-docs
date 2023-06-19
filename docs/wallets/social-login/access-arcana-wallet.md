---
title: Access Arcana Wallet
sidebar_position: 3
slug: /social-login-access-wallet
---

# Access Arcana Wallet

The Arcana Auth product enables social login for Web3 app users. They can easily onboard Web3 apps using the popular Web2 [social login](social-login-intro) mechanisms and sign blockchain transactions. For enabling authenticated users to sign blockchain transactions, the Web3 app developers must first [enable social login](social-login-enable) to onboard users and integrate with the Arcana Auth SDK.

Developers can enable the built-in Arcana Wallet UI (default) or configure the Auth SDK via the Arcana Developer Dashboard to use a Custom Wallet UI.

## Built-in Arcana Wallet UI

**To enable** the built-in Arcana Wallet UI, developers must choose the correct settings while registering the app. Developers can use the Arcana Developer Dashboard to register and make sure that the wallet UI mode in the newly registered app is set to Arcana Wallet (default) and **not** the Custom Wallet UI. After this, the app must be [integrated with the Arcana Auth SDK](https://docs.arcana.network/howto/integrate-app/index.html) and the appropriate code must be plugged in to onboard users via social login. For more details, see the [Arcana Auth SDK Quick Start Guide](https://docs.dev.arcana.network/auth-quick-start.html).

**To access** the built-in Arcana Wallet, the Web3 app users can simply log in to an app that is integrated with the Arcana Auth SDK. After successful authentication, users can instantly access Arcana Wallet and check the wallet balance, [send and receive tokens such as SHM](social-login-send-shm), send, receive and view NFTs, add and switch networks and initiate other supported Web3 wallet operations.

See [Arcana Wallet User Guide](https://docs.dev.arcana.network/user-guides/wallet-ui/index.html) to learn more about various supported Web3 wallet operations via the built-in Arcana Wallet UI.

<img src="/img/arcana/arcana-wallet.gif" alt="Login to access wallet" width="85%"/>

## Custom Wallet UI

The custom wallet UI option is a one-time setting during the Web3 app registration. Developers can use the Arcana Developer Dashboard to register the app and disable the Arcana Wallet UI by choosing the wallet UI setting as **Custom Wallet UI**. 

In addition to this, the developers must [integrate the app with the Arcana Auth SDK](https://docs.arcana.network/howto/integrate-app/index.html) and build a custom wallet UI that can handle user onboarding. Developers can plug in the custom UI with the appropriate Arcana Auth SDK functions to onboard users and perform Web3 wallet operations. For details, see [how to onboard users](https://docs.arcana.network/howto/onboard-users/custom-ui/index.html) and [how to plug in a custom wallet UI](https://docs.arcana.network/howto/arcana-wallet/custom-wallet-ui.html).

To use the custom wallet UI, the Web3 app users can simply log in to an app that is integrated with the Arcana Auth SDK. After successful authentication, the custom wallet UI is displayed. It is up to the Web3 app developer to provide notifications and take user approval before issuing any blockchain transactions through the Arcana Auth SDK functions. In the case of a custom wallet UI, the Arcana Auth SDK does not issue any notifications seeking user approval for blockchain transactions.