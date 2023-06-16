---
title: Access Arcana Wallet
sidebar_position: 3
---

# Access Arcana Wallet

The Arcana Auth product enables social login for Web3 app users. They can easily onboard Web3 apps using the popular Web2 [social login](/wallets/social-login/introduction/using-social-login) mechanisms and sign blockchain transactions. For enabling authenticated users to sign blockchain transactions, the Web3 app developers must first [enable social login](/wallets/social-login/enable-social-login) to onboard users and integrate with the Arcana Auth SDK.

Developers can enable the built-in Arcana Wallet UI (default) or configure the Auth SDK via the Arcana Developer Dashboard to use a Custom Wallet UI.

## Built-in Arcana Wallet UI

**To enable** the built-in Arcana Wallet UI, developers must choose the correct settings while registering the app. Developers can use the Arcana Developer Dashboard to register and make sure that the wallet UI mode in the newly registered app is set to Arcana Wallet (default) and **not** the Custom Wallet UI. After this, the app must be integrated with the Arcana Auth SDK and the appropriate code must be plugged in to onboard users via social login. For more details, see the [Arcana Auth SDK Quick Start Guide](https://docs.dev.arcana.network/auth-quick-start.html).

**To access** the built-in Arcana Wallet, the Web3 app users can simply log in to an app that is integrated with the Arcana Auth SDK. After successful authentication, users can instantly access Arcana Wallet and check the wallet balance, [send and receive tokens such as SHM](/wallets/social-login/sending-shm), send, receive and view NFTs, add and switch networks and initiate other supported Web3 wallet operations.

See [Arcana Wallet User Guide](https://docs.dev.arcana.network/user-guides/wallet-ui/index.html) to learn more about various supported Web3 wallet operations via the built-in Arcana Wallet UI.

## Custom Wallet UI

To enable a custom wallet UI, the Web3 app developers must disable the Arcana Wallet UI by choosing the wallet UI mode as **Custom Wallet UI** at the time of registering the application using the Arcana Developer dashboard. After integrating with the Arcana Auth SDK, the developers must build and plug in a custom wallet UI programmatically that can handle user onboarding and invoking of appropriate Arcana Auth SDK functions to perform Web3 wallet operations. For details, see [how to use a custom wallet UI](https://docs.arcana.network/howto/arcana-wallet/custom-wallet-ui.html).

To use the custom wallet UI, the Web3 app users can simply log in to an app that is integrated with the Arcana Auth SDK. After successful authentication, the custom wallet UI is displayed. It is up to the Web3 app developer to provide notifications and take user approval before issuing any blockchain transactions through the Arcana Auth SDK functions. The SDK does not issue any notifications seeking user approval for blockchain transactions in this case.