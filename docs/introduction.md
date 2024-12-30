---
id: introduction
title: Introduction to Privado ID (prev. Polygon ID)
sidebar_label: Introduction
description: Privado ID main concepts.
keywords:
  - docs
  - privado id
  - holder
  - issuer
  - verifier
  - wallet sdk
  - triangle of trust
---

import useBaseUrl from '@docusaurus/useBaseUrl';


Privado ID’s identity infrastructure facilitates trusted and secure relationships between apps and users, following the principles of self-sovereign identity and privacy by default. Privado ID enables organizations on one side to issue verifiable credentials about users, and organizations, on the other side, to verify those claims via a suite of tools created for each member of the SSI ecosystem.

## Why Privado ID?

Privado ID, with the help of zero-knowledge proofs, lets users prove their identity without the need of exposing their private information. This ensures both the **Freedom of Expression** and **Privacy by Default** (user's identities are secured by zero-knowledge cryptography).

## Core Concepts of Privado ID: Verifiable Credentials, Identity Holder, Issuer and Verifier

Every identity is identified by a unique identifier called [DID (Decentralized Identifier)](https://www.w3.org/TR/did-core/). Every identity-based information is represented via [Verifiable Credentials (VCs)](https://www.w3.org/TR/vc-data-model/). In the simplest terms, a VC represents any type of information related to an individual/enterprise/object. The VC could be as simple as the age of the entity or the highest degree held by it. It could also be a membership certificate issued by a DAO, for instance.

:::note

The toolset made available by Privado ID (prev. Polygon ID) is fully compliant with the W3C standards. We have a [<ins>definition spec. for the Polygon ID DID method</ins>](https://github.com/0xPolygonID/did-polygonid).

:::

The architecture of the framework is composed of three modules: Identity Holder, Issuer, and Verifier. These three, together, form what we call the **Triangle of Trust**. Let us see what role each entity plays in Privado ID.

1. **Identity Holder**: An entity that holds claims in its [Wallet](./wallet/wallet-overview.md). A VC, as mentioned above, is issued by an Issuer to the Holder. The Identity Holder generates zero-knowledge proofs of the VCs issued and presents these proofs to the Verifier, which verifies that the proof is authentic and matches specific criteria.

2. [**Issuer**](./issuer/issuer-overview.md): An entity (person, organization, or thing) that issues VCs to the Holders. VCs are cryptographically signed by the Issuer. Every VC comes from an Issuer.

3. [**Verifier**](./verifier/verifier-overview.md): A Verifier verifies the proof presented by a Holder. It requests the Holder to send a proof based on the VCs they hold in their wallet. While verifying a proof, the Verifier performs a set of checks, for example that the VC was signed by the expected Issuer and that the VC matches the criteria requested by the Verifier. This verification process can happen either off-chain or on-chain.

The simplest example of a Verifier is a bar that wants to verify if a client is over 18. In the real world, the Identity Holder would need to provide an ID and show all their personal information. With Privado ID, they only need to pass a proof.

A core concept here is the _trust_ that must exist between a Verifier and an Issuer: the fact that the information contained inside a VC is cryptographically verifiable doesn't guarantee it's true. The Issuer must be a trusted and reputable party so that Verifier can consume the VCs originated by that Issuer.

<div align="center">
<img src= {useBaseUrl('/img/triangle-of-trust-simple.png')} align="center" width="700"/>
</div>

## Role of a Wallet

A [Wallet](./wallet/wallet-overview.md) plays a crucial role in the seamless exchange of VCs with the Issuer, on one hand, and proofs with the Verifier, on the other. As stated above, an Identity Holder carries their personal data, in the form of VC, within their wallet. At its core, the wallet stores the private key of a user, fetch VCs from the Issuer, and create zero-knowledge proofs to be presented to the Verifier. Being the carrier of the sensitive information, the Wallet has been designed to ensure that the identity of its Holder is protected and preserved, and no sensitive data can be revealed to the third party without the consent of the Holder.

## What Can you Achieve Using Privado ID?

1. **Privacy using Zero-Knowledge Proofs**: An Identity Holder, using zero-knowledge proofs, can keep their personal data private. During the process of VC verification, it just needs to show a proof that they are the owner of a VC that matches certain criteria without letting the Verifier know of the actual VC. For example, an Identity Holder can prove to a Verifier authority that they are above 18 years of age by presenting the proof without revealing their actual age. This ensures minimum data exposure and hence confirms the safety of any sensitive data.
   Another aspect of privacy comes from the fact that the Issuer would not be able to track the usage of VCs by an individual once it has been issued.

2. **Off-Chain and On-Chain Verification**: Verification of proofs can be done either off-chain or on-chain via Smart Contracts. For example, developers can set up a contract that airdrops tokens only to users that meet certain criteria based on their VCs.

3. **Self-Sovereignty**: Privado ID renders self-sovereignty in the hands of the user. The user is the only custodian of their private keys; user-controlled data can be shared with third parties without taking any permission from the Issuer that has issued the VCs to the user.

4. **Transitive Trust**: A transitive trust between the actors of the triangle means that the trust between two entities in one domain or context can be easily extended to other domains or contexts. For instance, the information generated by an Issuer can be conveniently used by more than one Verifier without asking for permission. Along similar lines, an Identity Holder can build up their trust by collecting multiple credentials from different Issuers in one digital wallet.

## Privado ID and Iden3

<a href="https://iden3.io/" target="_blank">Iden3</a> is the open-source protocol at the basis of Privado ID. The protocol defines on a low-level how the parties listed above communicate and interact with each other. Privado ID is an abstraction layer to enable developers to build applications leveraging the Iden3 protocol.

## Further Resources On Privado ID (prev. Polygon ID)

- [Privado ID Youtube Playlists](https://www.youtube.com/@PrivadoID/playlists?view=50&sort=dd&shelf_id=5)
- [Polygon ID DID Method Overview at SSI Meetup (April 2023)](https://ssimeetup.org/polygonid-zero-knowledge-identity-web2-web3-otto-mora-webinar-62/)
- [Adding Verifiable Credentials to your crypto wallet - Eth CC July 2023](https://www.youtube.com/watch?v=5fv8e-k8t98)
- [The Future of Identity is Self-Sovereign: Build a dapp with Polygon ID - ETH Global - November 2022](https://youtu.be/utpazrLrSbY)
- [A Deep Dive into Polygon ID - ETH Vietnam - November 2022](https://youtu.be/fQ9DiGUnvwA)
- [Identity Layer for Web3 - Paris - July 2022](https://youtu.be/bmRvQNmxFkM)

## Further Resources On Verifiable Credentials

- [Verifiable Credentials: The Ultimate Guide](https://www.dock.io/post/verifiable-credentials)
- [Understanding and Using Verifiable Credentials](https://www.youtube.com/watch?v=BxLSSH_EHjo)
- [Polygon ID DID Method Specification](https://github.com/0xPolygonID/did-polygonid)

---
