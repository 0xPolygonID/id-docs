---
id: mumbai-to-amoy-migration
title: Guide for Amoy testnet migration from Mumbai testnet
sidebar_label: Introduction 2
keywords:
  - polygon id
  - amoy
  - migration
---

Welcome to the guide for migrating your projects and solutions built using PolygonID from the Mumbai testnet to the new Amoy testnet which is the new Sepolia-anchored testnet for Polygon PoS. With the deprecation of Goerli and Mumbai testnets, it's crucial to transition to Amoy for seamless development and testing. This guide aims to assist developers in understanding the changes required for integrating and using PolygonID on the Amoy testnet, ensuring a smooth transition.

:::note
These changes would only affect your project or solution on the testnet. Things on the Mainnet stay as it is. Most providers will shut down the Mumbai testnet RPC Nodes, so we request you to migrate to Amoy testnet for your solution to work as expected.
:::

## Issuer

To migrate to the Amoy testnet, developers must set up a new Issuer node configured for Amoy. The migration involves two steps:

1. Setting up a new Issuer node using the latest configuration guidelines.

   - To set up a new issuer node, please refer to [this installation guide](https://github.com/0xPolygonID/issuer-node/tree/develop). It includes the latest configuration for the Amoy testnet.
   - An Issuer will need to create a new identity for Amoy, through the core API specifying the proper "network": "amoy". If you do it with the make generate-issuer-did command, then the program will get the variables from the .env files that must be properly filled. (.env-samples are available at [Issuer Node GitHub repository](https://github.com/0xPolygonID/issuer-node/tree/main)).
   - Here you can find more details about issuer configuration ([advanced Issuer Node configuration](https://devs.polygonid.com/docs/issuer/issuer-configuration)).

2. Deprecating and shutting down existing Issuer nodes configured for the Mumbai testnet.

:::note
The identities and the states won’t be migrated from Mumbai to Amoy.
:::

:::note
Latest Issuer Node version: https://github.com/0xPolygonID/issuer-node/releases/tag/v2.5.0
:::

## Verifier

To ensure compatibility with the Amoy testnet, you need to install the latest version of Verifier SDK. For instances where the Verifier SDK is already integrated into existing systems, you should proceed by updating it to the latest version. Tools:

- JS-SDK ([v1.10.0](https://github.com/0xPolygonID/js-sdk/releases/tag/v1.10.0) or greater) is updated and compatible with the Amoy testnet.
- [Query Builder](https://schema-builder.polygonid.me/query-builder) is updated and compatible with the Amoy testnet.

## Wallet

Integrating with the Amoy testnet requires installing and updating to the latest version of the Wallet (2.3.4). This version provides support for Amoy testnet.

## Smart contracts

The Polygon ID smart contracts have been deployed to Amoy testnet. You can find the address of the contracts [here](https://devs.polygonid.com/docs/smart-contracts) and use them accordingly.

## Affected tools status

Here is the status for all the Tools with respect to support for the Amoy testnet:

- [Smart Contracts](https://devs.polygonid.com/docs/smart-contracts): Deployed on Amoy ✅
- [Query Builder](https://schema-builder.polygonid.me/query-builder): Updated and compatible with the Amoy testnet ✅
- [Issuer Node Demo](https://issuer-ui.polygonid.me): Updated and compatible with the Amoy testnet (for testing purposes only) ✅
- Mobile apps: Updated and compatible with the Amoy testnet ✅
  - [iOS latest](https://apps.apple.com/in/app/polygon-id/id1629870183) (version 2.3.4)
  - [Android latest](https://play.google.com/store/apps/details?id=com.polygonid.wallet&hl=en&gl=US) (version 2.3.4)

---
