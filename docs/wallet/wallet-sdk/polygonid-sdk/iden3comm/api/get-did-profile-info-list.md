---
id: get-did-profile-info-list
title: Get DID Profile Info List
sidebar_label: Get DID Profile Info List
description: Get info about a list of DIDs we interacted with.
keywords:
  - docs
  - polygon id
  - holder
  - issuer
  - verifier
  - wallet sdk
  - DID
  - profile
---

Get information about a list of DIDs that connect with a service.

```dart
Future<List<Map<String, dynamic>>> getDidProfileInfoList({
  required String did,
  required String privateKey,
  required List<FilterEntity>? filters,
});
```

`did` is the DID we interacted with.

The `privateKey` is the key used to access all the sensitive information from the identity and also to realize operations like generating proofs.

`filters` are used to apply queries to the information saved.
