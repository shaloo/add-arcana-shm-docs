---
title: Send SHM
sidebar_position: 5
---

# Send SHM

Wallet users can send SHM by selecting the appropriate blockchain network and using the `Assets` tab of the Arcana wallet to specify the SHM token amount and the gas fees. 

Web3 app developers can choose to programmatically initiate the send transactions to transfer SHM. A transaction notification will pop up for every blockchain transaction and the user will be required to approve or reject it.

## Send with Wallet UI

App users can simply use the Arcana wallet to send SHM.

<img src="/img/arcana/send_shm.gif" alt="Send SHM via UI" width="35%"/>>

## Send Programmatically

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
For details, see [Arcana Wallet Web3 Operations Guide](https://docs.arcana.network/howto/arcana-wallet/web3-ops/index.html).