---
title: Shares API | Dart SDK
---

# Shares API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**sharesCreateNewShare**](SharesApi#sharescreatenewshare) | **POST** /shares/create | /shares/create [POST]
[**sharesDeleteShare**](SharesApi#sharesdeleteshare) | **POST** /shares/\{share\}/delete | /shares/\{share\}/delete [POST]
[**sharesSnapshot**](SharesApi#sharessnapshot) | **GET** /shares | /shares [GET]
[**sharesSpecificShareSnapshot**](SharesApi#sharesspecificsharesnapshot) | **GET** /shares/\{share\} | /shares/\{share\} [GET]


## **sharesCreateNewShare** {#sharescreatenewshare}
> Shares sharesCreateNewShare(transferables, seededShare)

/shares/create [POST]

This endpoint will accept an asset. Response here will be a Share that was created.

### Example {#sharescreatenewshare-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = SharesApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
final seededShare = SeededShare(); // SeededShare | 

try {
    final result = api_instance.sharesCreateNewShare(transferables, seededShare);
    print(result);
} catch (e) {
    print('Exception when calling SharesApi->sharesCreateNewShare: $e\n');
}
```

### Parameters {#sharescreatenewshare-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 
 **seededShare** | [**SeededShare**](../models/SeededShare) |  | [optional] 

### Return type {#sharescreatenewshare-return-type}

[**Shares**](../models/Shares)

### Authorization {#sharescreatenewshare-authorization}

No authorization required

### HTTP request headers {#sharescreatenewshare-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json

## **sharesDeleteShare** {#sharesdeleteshare}
> String sharesDeleteShare(share)

/shares/\{share\}/delete [POST]

This endpoint will just take a share id(as a url param) to delete out of the shares table, will return the share id that was deleted.

### Example {#sharesdeleteshare-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = SharesApi();
final share = share_example; // String | Share id

try {
    final result = api_instance.sharesDeleteShare(share);
    print(result);
} catch (e) {
    print('Exception when calling SharesApi->sharesDeleteShare: $e\n');
}
```

### Parameters {#sharesdeleteshare-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **share** | **String** | Share id | 

### Return type {#sharesdeleteshare-return-type}

**String**

### Authorization {#sharesdeleteshare-authorization}

No authorization required

### HTTP request headers {#sharesdeleteshare-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **sharesSnapshot** {#sharessnapshot}
> Shares sharesSnapshot(transferables)

/shares [GET]

This will return all of your shares. A Share is an asset that you as a user decided to share with another user via link.

### Example {#sharessnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = SharesApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)

try {
    final result = api_instance.sharesSnapshot(transferables);
    print(result);
} catch (e) {
    print('Exception when calling SharesApi->sharesSnapshot: $e\n');
}
```

### Parameters {#sharessnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#sharessnapshot-return-type}

[**Shares**](../models/Shares)

### Authorization {#sharessnapshot-authorization}

No authorization required

### HTTP request headers {#sharessnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

## **sharesSpecificShareSnapshot** {#sharesspecificsharesnapshot}
> Share sharesSpecificShareSnapshot(share, transferables)

/shares/\{share\} [GET]

This is an endpoint to enable a client to access a specific share through a provided share id.

### Example {#sharesspecificsharesnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = SharesApi();
final share = share_example; // String | Share id
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)

try {
    final result = api_instance.sharesSpecificShareSnapshot(share, transferables);
    print(result);
} catch (e) {
    print('Exception when calling SharesApi->sharesSpecificShareSnapshot: $e\n');
}
```

### Parameters {#sharesspecificsharesnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **share** | **String** | Share id | 
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#sharesspecificsharesnapshot-return-type}

[**Share**](../models/Share)

### Authorization {#sharesspecificsharesnapshot-authorization}

No authorization required

### HTTP request headers {#sharesspecificsharesnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

