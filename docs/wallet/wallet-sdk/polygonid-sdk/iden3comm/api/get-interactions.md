---
id: get-interactions
title: Get Interactions
sidebar_label: Get Interactions
description: "Get a list of `InteractionEntity` associated to the identity previously stored
  in the Polygon ID Sdk."
keywords:
  - docs
  - polygon id
  - holder
  - issuer
  - verifier
  - wallet sdk
  - DID
  - Interaction Entity
---

Get a list of `InteractionEntity` associated to the identity previously stored in the Polygon ID SDK.

```dart
Future<List<InteractionBaseEntity>> getInteractions({
  String? genesisDid,
  BigInt? profileNonce,
  String? privateKey,
  List<InteractionType>? types,
  List<InteractionState>? states,
  List<FilterEntity>? filters,
});
```

The `genesisDid` is the unique ID of the identity.

The `profileNonce` is the nonce of the profile used from the identity to obtain the DID identifier.

The `privateKey` is the key used to access all the sensitive information from the identity and also to realize operations like generating proofs.
