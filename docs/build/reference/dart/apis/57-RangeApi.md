---
title: Range API | Dart SDK
---

# Range API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**rangeAssociateConversationGroundingTemporalRangeWorkstreams**](RangeApi#rangeassociateconversationgroundingtemporalrangeworkstreams) | **POST** /range/\{range\}/conversations/grounding/temporal_range/workstreams/associate/\{conversation\} | /range/\{range\}/conversations/grounding/temporal_range/workstreams/associate/\{conversation\} [POST]
[**rangeAssociateWorkstreamSummary**](RangeApi#rangeassociateworkstreamsummary) | **POST** /range/\{range\}/workstream_summaries/associate/\{workstream_summary\} | /range/\{range\}/workstream_summaries/associate/\{workstream_summary\} [POST]
[**rangeDisassociateConversationGroundingTemporalRangeWorkstreams**](RangeApi#rangedisassociateconversationgroundingtemporalrangeworkstreams) | **POST** /range/\{range\}/conversations/grounding/temporal_range/workstreams/disassociate/\{conversation\} | /range/\{range\}/conversations/grounding/temporal_range/workstreams/disassociate/\{conversation\} [POST]
[**rangeDisassociateWorkstreamSummary**](RangeApi#rangedisassociateworkstreamsummary) | **POST** /range/\{range\}/workstream_summaries/disassociate/\{workstream_summary\} | /range/\{range\}/workstream_summaries/disassociate/\{workstream_summary\} [POST]
[**rangeScoresIncrement**](RangeApi#rangescoresincrement) | **POST** /range/\{range\}/scores/increment | '/range/\{range\}/scores/increment' [POST]
[**rangeUpdate**](RangeApi#rangeupdate) | **POST** /range/update | /range/update [POST]
[**rangesSpecificRangeSnapshot**](RangeApi#rangesspecificrangesnapshot) | **GET** /range/\{range\} | /range/\{range\} [GET]


## **rangeAssociateConversationGroundingTemporalRangeWorkstreams** {#rangeassociateconversationgroundingtemporalrangeworkstreams}
> rangeAssociateConversationGroundingTemporalRangeWorkstreams(range, conversation)

/range/\{range\}/conversations/grounding/temporal_range/workstreams/associate/\{conversation\} [POST]

This will associate a range with a conversation(grounding.temporal.workstreams). This will do the same thing as the conversation equivalent.

### Example {#rangeassociateconversationgroundingtemporalrangeworkstreams-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = RangeApi();
final range = range_example; // String | This is a identifier that is used to identify a specific range.
final conversation = conversation_example; // String | This is the uuid of a conversation.

try {
    api_instance.rangeAssociateConversationGroundingTemporalRangeWorkstreams(range, conversation);
} catch (e) {
    print('Exception when calling RangeApi->rangeAssociateConversationGroundingTemporalRangeWorkstreams: $e\n');
}
```

### Parameters {#rangeassociateconversationgroundingtemporalrangeworkstreams-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **range** | **String** | This is a identifier that is used to identify a specific range. | 
 **conversation** | **String** | This is the uuid of a conversation. | 

### Return type {#rangeassociateconversationgroundingtemporalrangeworkstreams-return-type}

void (empty response body)

### Authorization {#rangeassociateconversationgroundingtemporalrangeworkstreams-authorization}

No authorization required

### HTTP request headers {#rangeassociateconversationgroundingtemporalrangeworkstreams-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **rangeAssociateWorkstreamSummary** {#rangeassociateworkstreamsummary}
> rangeAssociateWorkstreamSummary(range, workstreamSummary)

/range/\{range\}/workstream_summaries/associate/\{workstream_summary\} [POST]

This will associate a range with a workstream summary. This will do the same thing as the workstreamSummary equivalent.

### Example {#rangeassociateworkstreamsummary-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = RangeApi();
final range = range_example; // String | This is a identifier that is used to identify a specific range.
final workstreamSummary = workstreamSummary_example; // String | This is a identifier that is used to identify a specific workstream_summary.

try {
    api_instance.rangeAssociateWorkstreamSummary(range, workstreamSummary);
} catch (e) {
    print('Exception when calling RangeApi->rangeAssociateWorkstreamSummary: $e\n');
}
```

### Parameters {#rangeassociateworkstreamsummary-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **range** | **String** | This is a identifier that is used to identify a specific range. | 
 **workstreamSummary** | **String** | This is a identifier that is used to identify a specific workstream_summary. | 

### Return type {#rangeassociateworkstreamsummary-return-type}

void (empty response body)

### Authorization {#rangeassociateworkstreamsummary-authorization}

No authorization required

### HTTP request headers {#rangeassociateworkstreamsummary-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **rangeDisassociateConversationGroundingTemporalRangeWorkstreams** {#rangedisassociateconversationgroundingtemporalrangeworkstreams}
> rangeDisassociateConversationGroundingTemporalRangeWorkstreams(range, conversation)

/range/\{range\}/conversations/grounding/temporal_range/workstreams/disassociate/\{conversation\} [POST]

This will enable us to disassociate a range from a conversation(grounding.temporal.workstreams). This will do the same thing as the conversation equivalent.

### Example {#rangedisassociateconversationgroundingtemporalrangeworkstreams-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = RangeApi();
final range = range_example; // String | This is a identifier that is used to identify a specific range.
final conversation = conversation_example; // String | This is the uuid of a conversation.

try {
    api_instance.rangeDisassociateConversationGroundingTemporalRangeWorkstreams(range, conversation);
} catch (e) {
    print('Exception when calling RangeApi->rangeDisassociateConversationGroundingTemporalRangeWorkstreams: $e\n');
}
```

### Parameters {#rangedisassociateconversationgroundingtemporalrangeworkstreams-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **range** | **String** | This is a identifier that is used to identify a specific range. | 
 **conversation** | **String** | This is the uuid of a conversation. | 

### Return type {#rangedisassociateconversationgroundingtemporalrangeworkstreams-return-type}

void (empty response body)

### Authorization {#rangedisassociateconversationgroundingtemporalrangeworkstreams-authorization}

No authorization required

### HTTP request headers {#rangedisassociateconversationgroundingtemporalrangeworkstreams-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **rangeDisassociateWorkstreamSummary** {#rangedisassociateworkstreamsummary}
> rangeDisassociateWorkstreamSummary(range, workstreamSummary)

/range/\{range\}/workstream_summaries/disassociate/\{workstream_summary\} [POST]

This will enable us to disassociate a range from a workstream summary. This will do the same thing as the workstreamSummary equivalent.

### Example {#rangedisassociateworkstreamsummary-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = RangeApi();
final range = range_example; // String | This is a identifier that is used to identify a specific range.
final workstreamSummary = workstreamSummary_example; // String | This is a identifier that is used to identify a specific workstream_summary.

try {
    api_instance.rangeDisassociateWorkstreamSummary(range, workstreamSummary);
} catch (e) {
    print('Exception when calling RangeApi->rangeDisassociateWorkstreamSummary: $e\n');
}
```

### Parameters {#rangedisassociateworkstreamsummary-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **range** | **String** | This is a identifier that is used to identify a specific range. | 
 **workstreamSummary** | **String** | This is a identifier that is used to identify a specific workstream_summary. | 

### Return type {#rangedisassociateworkstreamsummary-return-type}

void (empty response body)

### Authorization {#rangedisassociateworkstreamsummary-authorization}

No authorization required

### HTTP request headers {#rangedisassociateworkstreamsummary-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **rangeScoresIncrement** {#rangescoresincrement}
> rangeScoresIncrement(range, seededScoreIncrement)

'/range/\{range\}/scores/increment' [POST]

This will take in a SeededScoreIncrement and will increment the material relative to the incoming body.

### Example {#rangescoresincrement-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = RangeApi();
final range = range_example; // String | This is a identifier that is used to identify a specific range.
final seededScoreIncrement = SeededScoreIncrement(); // SeededScoreIncrement | 

try {
    api_instance.rangeScoresIncrement(range, seededScoreIncrement);
} catch (e) {
    print('Exception when calling RangeApi->rangeScoresIncrement: $e\n');
}
```

### Parameters {#rangescoresincrement-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **range** | **String** | This is a identifier that is used to identify a specific range. | 
 **seededScoreIncrement** | [**SeededScoreIncrement**](../models/SeededScoreIncrement) |  | [optional] 

### Return type {#rangescoresincrement-return-type}

void (empty response body)

### Authorization {#rangescoresincrement-authorization}

No authorization required

### HTTP request headers {#rangescoresincrement-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain

## **rangeUpdate** {#rangeupdate}
> Range rangeUpdate(range)

/range/update [POST]

This will update a specific range.

### Example {#rangeupdate-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = RangeApi();
final range = Range(); // Range | 

try {
    final result = api_instance.rangeUpdate(range);
    print(result);
} catch (e) {
    print('Exception when calling RangeApi->rangeUpdate: $e\n');
}
```

### Parameters {#rangeupdate-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **range** | [**Range**](../models/Range) |  | [optional] 

### Return type {#rangeupdate-return-type}

[**Range**](../models/Range)

### Authorization {#rangeupdate-authorization}

No authorization required

### HTTP request headers {#rangeupdate-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **rangesSpecificRangeSnapshot** {#rangesspecificrangesnapshot}
> Range rangesSpecificRangeSnapshot(range)

/range/\{range\} [GET]

This will get a snapshot of a single range.

### Example {#rangesspecificrangesnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = RangeApi();
final range = range_example; // String | This is a identifier that is used to identify a specific range.

try {
    final result = api_instance.rangesSpecificRangeSnapshot(range);
    print(result);
} catch (e) {
    print('Exception when calling RangeApi->rangesSpecificRangeSnapshot: $e\n');
}
```

### Parameters {#rangesspecificrangesnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **range** | **String** | This is a identifier that is used to identify a specific range. | 

### Return type {#rangesspecificrangesnapshot-return-type}

[**Range**](../models/Range)

### Authorization {#rangesspecificrangesnapshot-authorization}

No authorization required

### HTTP request headers {#rangesspecificrangesnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain

