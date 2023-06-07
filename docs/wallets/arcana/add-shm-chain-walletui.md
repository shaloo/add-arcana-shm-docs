---
title: Add Shardeum Network
sidebar_position: 4
---

# Add Shardeum Network

By default, Arcana Wallet supports Sphinx 1.x Shardeum blockchain. In this guide, you will learn how users can add another Shardeum blockchain to the Arcana Wallet. 

There are two ways to add a new Shardeum network. The wallet user can use the UI to add the network.  The app developer can choose to programmatically add a new Shardeum network by calling the appropriate functions supported by the Arcana Auth SDK.

> **Note: Chains Added by User**

> Only the chains configured by the app developer persist across the user's login session. If a user manually adds any supported EVM-compatible chain through the wallet UI, it will be available only during the current user login session.

## Add Network using Wallet UI

Users can use the Arcana wallet UI to add any supported EVM network that does not show up automatically in the wallet UI.

### Step 1: Log In

To access the Arcana Wallet, log in to the Web3 app that is integrated with the Arcana Auth SDK. After a successful login, the Arcana wallet is displayed in the App's context. 

### Step 2: Add Network

Click on the `Network` dropdown and choose `New` to add the new blockchain network details. The figure below shows how to add Shardeum Liberty 2.x network details. The newly added network shows up as the default blockchain network in the wallet.

<img src="/img/arcana/add_shm_ntwk.gif" alt="Add Liberty Network via UI" width="35%"/>>

## Add Network Programmatically

Developers must follow these instructions to programmatically add network such that authenticated users see it automatically when the Arcana wallet is displayed in the app's context.

### Step 1: Register and Configure App

[Register the app](https://docs.arcana.network/howto/configure-auth.html) and obtain a unique client identifier required later while integrating the app with the Arcana Auth SDK. 

See [how to configure user onboarding options](https://docs.arcana.network/howto/configure-auth/index.html). By default, if no authentication providers are configured, the user can onboard the app in a passwordless manner via email/magic link.

### Step 2: Install SDK

**`npm`**

```bash
npm install --save @arcana/auth
```

**`yarn`**

```bash
yarn add @arcana/auth
```

### Step 3: Integrate App

Use the unique client identifier obtained after registering the app with Arcana Network to integrate with the Arcana Auth SDK.

```js
import { AuthProvider } from "@arcana/auth";

let provider;
const auth = new AuthProvider('xar_test_19b21f9a536c80303f56b229601de1c3ade08366', {
  network: "testnet",
  alwaysVisible: true,
  setWindowProvider: true,
  position: "right",
  theme: "dark"
});
provider = auth.provider;
```

For details, see [how to integrate with the Arcana Auth SDK](https://docs.arcana.network/howto/integrate-app/index.html).

### Step 4: Onboard Users

Use the built-in plug-and-play login UI to onboard users. By default, all the configured authentication options will be displayed and the user can choose one to log in to the app.

```js

await auth.connect();

```

Developers can also use a custom login UI to onboard users.  See [onboarding users](https://docs.arcana.network/howto/onboard-users/index.html) for details.

### Step 5: Add Network

After making sure that a user has logged in, call `wallet_addEthereumChain` method specified by [EIP-3085](https://eips.ethereum.org/EIPS/eip-3085) as shown below. 

```ts
try {
  await provider.request({
    method: 'wallet_addEthereumChain',
    params: [{
      chainId: '0xABCDEF',
      chainName: 'My Custom Chain',
      rpcUrls: ['...']
    }]
  })
} catch(error) {
  ...
}

// Parameters
// wallet_addEthereumChain accepts a single object parameter, 
// specified by the AddEthereumChainParameter TypeScript interface

interface AddEthereumChainParameter {
  chainId: string; // A 0x-prefixed hexadecimal string
  chainName: string;
  nativeCurrency: {
    name: string;
    symbol: string; // 2-6 characters long
    decimals: 18;
  };
  rpcUrls: string[];
  blockExplorerUrls?: string[];
}

```

Developers can control which chains are displayed in the Arcana wallet dropdown list. They can also manage whether the wallet UI is displayed once the user logs in or only when a blockchain transaction is triggered. For more details, refer to the [Arcana Wallet Developer's Guide](https://docs.dev.arcana.network/howto/arcana-wallet/index.html).

