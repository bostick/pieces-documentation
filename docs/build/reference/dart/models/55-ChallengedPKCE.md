---
title: ChallengedPKCE | Dart SDK
---

# ChallengedPKCE

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] 
**state** | **String** | An opaque value the clients adds to the initial request that Auth0 includes when redirecting the back to the client. This value must be used by the client to prevent CSRF attacks. | 
**nonce** | **String** | A local key that is held as the comparator to state, thus they should be the same. | 
**challenge** | **String** | Generated challenge from the code_verifier. | 
**method** | **String** | Method used to generate the challenge. The PKCE spec defines two methods, S256 and plain, however, Auth0 supports only S256 since the latter is discouraged. | 
**verifier** | **String** | Cryptographically random key that was used to generate the code_challenge passed to /authorize. | 


