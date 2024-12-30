---
id: get-did-profile-info
title: Get DID Profile Info
sidebar_label: Get DID Profile Info
description: Get info about a DID we interacted with.
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

Get information about a connection betwen a DID and a service.

```dart
Future<Map<String, dynamic>> getDidProfileInfo({
  required String did,
  required String privateKey,
  required String interactedWithDid,
});
```

`did` is the DID we interacted with.

The `privateKey` is the key used to access all the sensitive information from the identity and also to realize operations like generating proofs.

`interactedWithDid` is the identifier of the service we have interacted with. This is used to be able to recognize/use it in another occasion.
