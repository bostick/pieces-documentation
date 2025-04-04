---
title: ConversationMessages API | Dart SDK
---

# ConversationMessages API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**messagesCreateSpecificMessage**](ConversationMessagesApi#messagescreatespecificmessage) | **POST** /messages/create | /messages/create [POST]
[**messagesDeleteSpecificMessage**](ConversationMessagesApi#messagesdeletespecificmessage) | **POST** /messages/\{message\}/delete | /messages/\{message\}/delete [POST]
[**messagesSnapshot**](ConversationMessagesApi#messagessnapshot) | **GET** /messages | /messages [GET]


## **messagesCreateSpecificMessage** {#messagescreatespecificmessage}
> ConversationMessage messagesCreateSpecificMessage(transferables, seededConversationMessage)

/messages/create [POST]

This will create a Message on a specific conversation.

### Example {#messagescreatespecificmessage-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessagesApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
final seededConversationMessage = SeededConversationMessage(); // SeededConversationMessage | 

try {
    final result = api_instance.messagesCreateSpecificMessage(transferables, seededConversationMessage);
    print(result);
} catch (e) {
    print('Exception when calling ConversationMessagesApi->messagesCreateSpecificMessage: $e\n');
}
```

### Parameters {#messagescreatespecificmessage-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 
 **seededConversationMessage** | [**SeededConversationMessage**](../models/SeededConversationMessage) |  | [optional] 

### Return type {#messagescreatespecificmessage-return-type}

[**ConversationMessage**](../models/ConversationMessage)

### Authorization {#messagescreatespecificmessage-authorization}

No authorization required

### HTTP request headers {#messagescreatespecificmessage-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **messagesDeleteSpecificMessage** {#messagesdeletespecificmessage}
> messagesDeleteSpecificMessage(message)

/messages/\{message\}/delete [POST]

This will delete a specific message.

### Example {#messagesdeletespecificmessage-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessagesApi();
final message = message_example; // String | This is the uuid of a message.

try {
    api_instance.messagesDeleteSpecificMessage(message);
} catch (e) {
    print('Exception when calling ConversationMessagesApi->messagesDeleteSpecificMessage: $e\n');
}
```

### Parameters {#messagesdeletespecificmessage-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message** | **String** | This is the uuid of a message. | 

### Return type {#messagesdeletespecificmessage-return-type}

void (empty response body)

### Authorization {#messagesdeletespecificmessage-authorization}

No authorization required

### HTTP request headers {#messagesdeletespecificmessage-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **messagesSnapshot** {#messagessnapshot}
> ConversationMessages messagesSnapshot(transferables)

/messages [GET]

This will get all the messages.

### Example {#messagessnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessagesApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)

try {
    final result = api_instance.messagesSnapshot(transferables);
    print(result);
} catch (e) {
    print('Exception when calling ConversationMessagesApi->messagesSnapshot: $e\n');
}
```

### Parameters {#messagessnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#messagessnapshot-return-type}

[**ConversationMessages**](../models/ConversationMessages)

### Authorization {#messagessnapshot-authorization}

No authorization required

### HTTP request headers {#messagessnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain

