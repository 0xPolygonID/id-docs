---
id: add-did-profile-info
title: Add DID Profile Info
sidebar_label: Add DID Profile Info
description: Add info about a DID we interacted with.
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

Add information of a connection between a DID and a service.

```dart
Future<void> addDidProfileInfo({
  required String did,
  required String privateKey,
  required String interactedWithDid,
  required Map<String, dynamic> info,
});
```

`did` is the DID we interacted with.

The `privateKey` is the key used to access all the sensitive information from the identity and also to realize operations like generating proofs.

`interactedWithDid` is the identifier of the service we have interacted with. This is used to be able to recognize/use it in another occasion.

`info` represents the information saved within the service.
