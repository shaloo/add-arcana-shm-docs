---
title: Arcana Auth Developer Guide
sidebar_position: 3
---

# Arcana Auth Developer Guide

Arcana Auth allows Web3 application developers to easily onboard users via Web2 login options and enable authenticated users to sign blockchain transactions and perform Web3 wallet operations from within the app's context. Users are not required to install a browser extension to access the wallet. 

Arcana offers a highly secure, non-custodial wallet solution that is based on the latest cryptographic techniques and cutting-edge asynchronous distributed key generation protocols. Users have full control of the wallet without bothering about the cryptographic complexities. Arcana Auth makes onboarding Web3 apps a breeze for the users.

To enable the Arcana wallet in a Web3 app, the developers must follow these steps:

* **Step 1**: Register the app with the Arcana Network using the Arcana Developer Dashboard and get a unique client identifier for the app. Configure the authentication providers to enable required user onboarding options.
* **Step 2**: Install the Arcana Auth SDK and integrate the app with it by creating an `AuthProvider` using the unique client identifier obtained during the registration earlier.
* **Step 3**: Initialize the SDK and then call functions to onboard users via the configured authentication providers. Call other SDK functions as required by the application logic. 

For more details, see the[Arcana Auth Developers Guide](https://docs.dev.arcana.network/auth-quick-start.html).