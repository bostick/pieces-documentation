---
title: Connector API | Dart SDK
---

# Connector API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**connect**](ConnectorApi#connect) | **POST** /connect | /connect [POST]
[**intention**](ConnectorApi#intention) | **POST** /\{application\}/intention | /\{application\}/intention [POST]
[**onboarded**](ConnectorApi#onboarded) | **POST** /\{application\}/onboarded | /onboarded [POST]
[**react**](ConnectorApi#react) | **POST** /\{application\}/reaction | /\{application\}/reaction [POST]
[**suggest**](ConnectorApi#suggest) | **POST** /\{application\}/suggestion | /\{application\}/suggestion [POST]
[**track**](ConnectorApi#track) | **POST** /\{application\}/track | /\{application\}/track [POST]


## **connect** {#connect}
> Context connect(seededConnectorConnection)

/connect [POST]

Abstracts a bootup/connection for a specific context.

### Example {#connect-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConnectorApi();
final seededConnectorConnection = SeededConnectorConnection(); // SeededConnectorConnection | 

try {
    final result = api_instance.connect(seededConnectorConnection);
    print(result);
} catch (e) {
    print('Exception when calling ConnectorApi->connect: $e\n');
}
```

### Parameters {#connect-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededConnectorConnection** | [**SeededConnectorConnection**](../models/SeededConnectorConnection) |  | [optional] 

### Return type {#connect-return-type}

[**Context**](../models/Context)

### Authorization {#connect-authorization}

No authorization required

### HTTP request headers {#connect-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **intention** {#intention}
> String intention(application, seededConnectorAsset)

/\{application\}/intention [POST]

Allows you to send a SeededAsset for future comparison.

### Example {#intention-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConnectorApi();
final application = application_example; // String | 
final seededConnectorAsset = SeededConnectorAsset(); // SeededConnectorAsset | 

try {
    final result = api_instance.intention(application, seededConnectorAsset);
    print(result);
} catch (e) {
    print('Exception when calling ConnectorApi->intention: $e\n');
}
```

### Parameters {#intention-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **String** |  | 
 **seededConnectorAsset** | [**SeededConnectorAsset**](../models/SeededConnectorAsset) |  | [optional] 

### Return type {#intention-return-type}

**String**

### Authorization {#intention-authorization}

No authorization required

### HTTP request headers {#intention-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain

## **onboarded** {#onboarded}
> String onboarded(application, body)

/onboarded [POST]

A central endpoint to manage updates to the onboarding process.

### Example {#onboarded-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConnectorApi();
final application = application_example; // String | This is a uuid that represents an application
final body = bool(); // bool | Whether or not that application has been onboarded.

try {
    final result = api_instance.onboarded(application, body);
    print(result);
} catch (e) {
    print('Exception when calling ConnectorApi->onboarded: $e\n');
}
```

### Parameters {#onboarded-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **String** | This is a uuid that represents an application | 
 **body** | **bool** | Whether or not that application has been onboarded. | [optional] 

### Return type {#onboarded-return-type}

**String**

### Authorization {#onboarded-authorization}

No authorization required

### HTTP request headers {#onboarded-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain

## **react** {#react}
> String react(application, reaction)

/\{application\}/reaction [POST]

This will respond to the output generated by the /suggest endpoint.

### Example {#react-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConnectorApi();
final application = application_example; // String | 
final reaction = Reaction(); // Reaction | ** This body will need to be modified.

try {
    final result = api_instance.react(application, reaction);
    print(result);
} catch (e) {
    print('Exception when calling ConnectorApi->react: $e\n');
}
```

### Parameters {#react-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **String** |  | 
 **reaction** | [**Reaction**](../models/Reaction) | ** This body will need to be modified. | [optional] 

### Return type {#react-return-type}

**String**

### Authorization {#react-authorization}

No authorization required

### HTTP request headers {#react-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain

## **suggest** {#suggest}
> Suggestion suggest(application, seededConnectorCreation)

/\{application\}/suggestion [POST]

Invoked whenever a code snippet is copied from an integration. For instance, if a JetBrains user copies code, this endpoint can be called to assess whether to suggest reusing a piece (if reuse is true, the endpoint provides assets that the user may consider using), saving the code snippet, or taking no action.   **Note: This endpoint could potentially accept a SeededFormat for the request body if required.

### Example {#suggest-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConnectorApi();
final application = application_example; // String | 
final seededConnectorCreation = SeededConnectorCreation(); // SeededConnectorCreation | This is the Snippet that we will compare to all the saved assets to determine what we want to do with it!

try {
    final result = api_instance.suggest(application, seededConnectorCreation);
    print(result);
} catch (e) {
    print('Exception when calling ConnectorApi->suggest: $e\n');
}
```

### Parameters {#suggest-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **String** |  | 
 **seededConnectorCreation** | [**SeededConnectorCreation**](../models/SeededConnectorCreation) | This is the Snippet that we will compare to all the saved assets to determine what we want to do with it! | [optional] 

### Return type {#suggest-return-type}

[**Suggestion**](../models/Suggestion)

### Authorization {#suggest-authorization}

No authorization required

### HTTP request headers {#suggest-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **track** {#track}
> String track(application, seededConnectorTracking)

/\{application\}/track [POST]

Abstracts the process of packaging segments on a per-context basis.

### Example {#track-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConnectorApi();
final application = application_example; // String | This is a uuid that represents an application
final seededConnectorTracking = SeededConnectorTracking(); // SeededConnectorTracking | The body is able to take in several properties 

try {
    final result = api_instance.track(application, seededConnectorTracking);
    print(result);
} catch (e) {
    print('Exception when calling ConnectorApi->track: $e\n');
}
```

### Parameters {#track-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **String** | This is a uuid that represents an application | 
 **seededConnectorTracking** | [**SeededConnectorTracking**](../models/SeededConnectorTracking) | The body is able to take in several properties  | [optional] 

### Return type {#track-return-type}

**String**

### Authorization {#track-authorization}

No authorization required

### HTTP request headers {#track-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain

