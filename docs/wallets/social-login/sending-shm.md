---
title: Send SHM
sidebar_position: 4
slug: /social-login-send-shm
---

# Send SHM

Web3 apps that are [integrated with the Arcana Auth product](social-login-enable) can allow users to easily onboard via [social login](social-login-intro) like the Web2 apps. Once onboard, the authenticated users can instantly access [the built-in, embedded, non-custodial Arcana Wallet UI](social-login-access-wallet) and initiate blockchain transactions to send SHM or respond to the app request for sending SHM and sign blockchain transactions.

A send SHM transaction can either be initiated by a Web3 app user through the wallet UI or it can be initiated through the app logic, programmatically by the developer.

Arcana Auth product is pre-configured for Shardeum Network. There is no need to manually configure the network for sending SHM. Also, there are options to add other flavors of Shardeum Network, besides the one that is pre-configured.

## Pre-requisites

To allow Web3 app users to initiate a send SHM transaction via the Arcana Wallet UI, or programmatically, the developers must ensure that the app is [integrated with the Arcana Auth product](https://docs.arcana.network/howto/integrate-app/index.html) and that social login is configured to onboard users. 

The following must be addressed before sending SHM:

* Register and configure the Web3 app using the Arcana Developer Dashboard.
* Configure user onboarding options for social login.
* Make sure that Shardeum Network is set as the default in the dashboard. This will display Shardeum as the default selected network once the wallet is enabled after the user authenticates.
* Install the Arcana Auth SDK.
* Integrate the app with the Arcana Auth SDK and plug in the code to onboard users and enable Web3 wallet operations.
* Deploy the app on Arcana Testnet/Mainnet.

For details on how to register, configure and integrate with the Arcana Auth, see the [Arcana Auth SDK Quick Start Guide](https://docs.dev.arcana.network/auth-quick-start.html).

Irrespective of whether the user initiates SHM send operation via the wallet UI or if it is initiated programmatically, make sure that:

1. the default blockchain network is selected as Shardeum.
2. the user is authenticated and has some SHM balance in the associated wallet address.

## User-initiated: Send SHM

Once the app is deployed, users can log in, access the Arcana Wallet UI and issue send SHM transactions by clicking the 'Token Assets' tab of the wallet UI, then select 'Send' and specify the token amount and other details before confirming the transaction.

<img src="/img/arcana/send_shm.gif" alt="Send SHM via UI" width="35%"/>>

## Developer-initiated: Send SHM

In addition to the wallet UI option to send SHM, the developers can also programmatically plug in the appropriate code in the app and initiate a request to send SHM tokens. This will bring up a send transaction notification pop-up in the Web3 app's context displaying all the transaction details. The user can review them and choose to confirm or reject the request.

By default, `Ethereum` is set as the default network for blockchain transactions.  The developer can configure Shardeum as the default network using the Arcana Developer Dashboard at the time of setting up the app. If the built-in Arcana Wallet is enabled, then the wallet UI is accessible to the authenticated user. The user can change the default network by clicking on the network icon in the top right of the wallet. Before issuing a send SHM transaction programmatically, it is recommended that the developer first check the network selected in the wallet by the user and then if required, switch the network explicitly to Sharedeum before issuing the send transaction request, as displayed in the sample code below.

Use `wallet_switchEthereumChain` to switch to the appropriate SHM network before calling the `eth_sendTransaction` function to send SHM tokens.

```js
try {
  await provider.request({
    method: 'wallet_switchEthereumChain',
    params: [{ chainId: '8082' }],
  });
} catch(error) {
  ...
}

...

async function sendTransaction() {
  setRequest('eth_sendTransaction')
  const hash = await provider.request({
    method: 'eth_sendTransaction',
      params: [{
      from,
      gasPrice: 0,
      to: '0xE28F01Cf69f27Ee17e552bFDFB7ff301ca07e780',
      value: '0x0de0b6b3a7640000',
    },],
  })
  console.log({ hash })
}
...

```
For more details, see [Arcana Wallet Web3 Operations Guide](https://docs.arcana.network/howto/arcana-wallet/web3-ops/index.html).