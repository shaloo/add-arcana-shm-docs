---
title: Enable Social Login
sidebar_position: 2
---

# Enable Social Login

To use [social login](./introduction#using-social-login), the users do not need to install any browser extension or set up a wallet. They simply need to use the familiar Web2 login mechanisms and log into a Web3 app that has social login enabled by the developers. Once authenticated, users have immediate access to the embedded Web3 wallet within the app's context.

Arcana Auth product helps developers to enable social login in Web3 apps easily. To enable social login using the Arcana Auth product, the developers must follow these steps:

* **Step 1**: Register the app with the Arcana Network using the Arcana Developer Dashboard and get a unique client identifier for the app. Configure the authentication providers to enable required user onboarding options. Add or modify the pre-configured supported blockchains and set the default chain.
* **Step 2**: Install the Arcana Auth SDK and integrate the app with it by using the unique client identifier obtained during the registration step.
* **Step 3**: Initialize the SDK and then call functions to onboard users via the configured authentication providers. Call other SDK functions as required by the application logic for performing Web3 wallet operations.

Once the user authenticates, the built-in, embedded, non-custodial Arcana Wallet is immediately available to the Web3 app users and they can sign blockchain transactions.

For more details, see the [Arcana Auth SDK Quick Start Guide](https://docs.dev.arcana.network/auth-quick-start.html).

## Supported Chains & Social Providers

Arcana Auth product offers a highly secure, non-custodial wallet solution that is based on the latest cryptographic techniques and cutting-edge asynchronous distributed key generation protocols. Users have full control of the wallet without having to deal with cryptographic complexities. The Arcana Auth SDK supports multiple Web2 authentication providers and passwordless login. A subset of the supported blockchains is pre-configured, including the Shardeum network. The pre-configured list can be modified as per the app requirements.

For a list of supported blockchain networks, see [here](https://docs.arcana.network/state-of-the-arcana-auth.html#supported-blockchains). Refer to the supported user onboarding mechanisms supported by Arcana Auth [here](https://docs.arcana.network/state-of-the-arcana-auth.html#user-onboarding-options).

## References

* [Arcana Auth SDK Reference Guide](https://authsdk-ref-guide.netlify.app/)
* [Enabling Web3 Wallet Operations](https://docs.arcana.network/howto/arcana-wallet/index.html)