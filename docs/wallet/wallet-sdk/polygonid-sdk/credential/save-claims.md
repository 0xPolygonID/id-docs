---
id: save-claims
title: Save credentials
sidebar_label: Save Credentials
description: Store a list of ClaimEntity associated with an identity in the Polygon ID Sdk.
keywords:
  - docs
  - polygon id
  - holder
  - issuer
  - verifier
  - wallet sdk
  - save
  - credential
---

Store a list of `ClaimEntity` in the Polygon ID SDK associated to an identity.

```dart
Future<List<ClaimEntity>> saveClaims(
    {required List<ClaimEntity> claims,
    required String genesisDid,
    required String privateKey});
```

The `claims` is the list of `ClaimEntity` to store associated to an identity.

The `genesisDid` is the unique ID of the identity.

The `privateKey` is the key used to access all the sensitive information from the identity and also to realize operations like generating proofs.
