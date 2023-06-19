---
title: Enable Social Login
sidebar_position: 2
slug: /social-login-enable
---

# Enable Social Login

Arcana Auth product offers social login for onboarding Web3 app users. The product consists of:

* Arcana Developer Dashboard
* Arcana Auth SDK
* Arcana Wallet UI

With Arcana Auth, the Web3 apps can enable a highly secure, embedded, non-custodial wallet solution that is based on the latest cryptographic techniques and cutting-edge asynchronous distributed key generation protocols.

To use [social login](social-login-intro), Web3 users do not need to install any browser extension or set up a wallet. They simply need to use the familiar Web2 login mechanisms and log into a Web3 app that has social login enabled by the developers. Once authenticated, users have immediate access to the embedded Web3 wallet within the app's context.

Developers can enable social login in Web3 apps by integrating with the Arcana Auth product using these simple steps:

* **Step 1**: Register the app with the Arcana Network using the Arcana Developer Dashboard and get a unique client identifier for the app. Configure the authentication providers to enable required user onboarding options. Add or modify the pre-configured supported blockchains and set the default chain.
* **Step 2**: Install the Arcana Auth SDK and integrate the app with it by using the unique client identifier obtained during the registration step.
* **Step 3**: Initialize the SDK and then call functions to onboard users via the configured authentication providers. Call other SDK functions as required by the application logic for performing Web3 wallet operations.

For more details, see the [Arcana Auth SDK Quick Start Guide](https://docs.dev.arcana.network/auth-quick-start.html).

## Supported Chains & Social Providers

Arcana Auth supports multiple Web2 authentication providers as well as the passwordless login option. A subset of the supported blockchains is pre-configured, including the **Shardeum Sphinx network**. The pre-configured chains list can be modified as per the app requirements via the Arcana Developer Dashboard.

For a list of supported blockchain networks, see [here](https://docs.arcana.network/state-of-the-arcana-auth.html#supported-blockchains). Refer to the supported user onboarding mechanisms supported by Arcana Auth [here](https://docs.arcana.network/state-of-the-arcana-auth.html#user-onboarding-options).

## References

* [Arcana Auth SDK Reference Guide](https://authsdk-ref-guide.netlify.app/)
* [Enabling Web3 Wallet Operations](https://docs.arcana.network/howto/arcana-wallet/index.html)