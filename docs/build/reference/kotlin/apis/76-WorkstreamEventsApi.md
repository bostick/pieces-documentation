---
title: WorkstreamEvents API | Kotlin SDK
---

# WorkstreamEvents API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**workstreamEventsCreateNewWorkstreamEvent**](#workstreameventscreatenewworkstreamevent) | **POST** /workstream_events/create | /workstream_events/create [POST]
[**workstreamEventsDeleteSpecificWorkstreamEvent**](#workstreameventsdeletespecificworkstreamevent) | **POST** /workstream_events/\{workstream_event\}/delete | /workstream_events/\{workstream_event\}/delete [POST]
[**workstreamEventsSnapshot**](#workstreameventssnapshot) | **GET** /workstream_events | /workstream_events [GET]


## **workstreamEventsCreateNewWorkstreamEvent** {#workstreameventscreatenewworkstreamevent}
> WorkstreamEvent workstreamEventsCreateNewWorkstreamEvent(transferables, seededWorkstreamEvent)

/workstream_events/create [POST]

This will create a new WorkstreamEvent in the database.

### Example {#workstreameventscreatenewworkstreamevent-example}
```kotlin
// Import classes:
import app.pieces.pieces-os-client.infrastructure.*
import app.pieces.pieces-os-client.models.*

val apiInstance = WorkstreamEventsApi()
val transferables : kotlin.Boolean = true // kotlin.Boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
val seededWorkstreamEvent : SeededWorkstreamEvent =  // SeededWorkstreamEvent | 
try {
    val result : WorkstreamEvent = apiInstance.workstreamEventsCreateNewWorkstreamEvent(transferables, seededWorkstreamEvent)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkstreamEventsApi#workstreamEventsCreateNewWorkstreamEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkstreamEventsApi#workstreamEventsCreateNewWorkstreamEvent")
    e.printStackTrace()
}
```

### Parameters {#workstreameventscreatenewworkstreamevent-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **kotlin.Boolean**| This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional]
 **seededWorkstreamEvent** | [**SeededWorkstreamEvent**](../models/SeededWorkstreamEvent)|  | [optional]

### Return type {#workstreameventscreatenewworkstreamevent-return-type}

[**WorkstreamEvent**](../models/WorkstreamEvent)

### Authorization {#workstreameventscreatenewworkstreamevent-authorization}

No authorization required

### HTTP request headers {#workstreameventscreatenewworkstreamevent-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json

## **workstreamEventsDeleteSpecificWorkstreamEvent** {#workstreameventsdeletespecificworkstreamevent}
> workstreamEventsDeleteSpecificWorkstreamEvent(workstreamEvent)

/workstream_events/\{workstream_event\}/delete [POST]

This will delete a specific workstream_event from the database!

### Example {#workstreameventsdeletespecificworkstreamevent-example}
```kotlin
// Import classes:
import app.pieces.pieces-os-client.infrastructure.*
import app.pieces.pieces-os-client.models.*

val apiInstance = WorkstreamEventsApi()
val workstreamEvent : kotlin.String = workstreamEvent_example // kotlin.String | This is a identifier that is used to identify a specific workstream_event.
try {
    apiInstance.workstreamEventsDeleteSpecificWorkstreamEvent(workstreamEvent)
} catch (e: ClientException) {
    println("4xx response calling WorkstreamEventsApi#workstreamEventsDeleteSpecificWorkstreamEvent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkstreamEventsApi#workstreamEventsDeleteSpecificWorkstreamEvent")
    e.printStackTrace()
}
```

### Parameters {#workstreameventsdeletespecificworkstreamevent-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workstreamEvent** | **kotlin.String**| This is a identifier that is used to identify a specific workstream_event. |

### Return type {#workstreameventsdeletespecificworkstreamevent-return-type}

null (empty response body)

### Authorization {#workstreameventsdeletespecificworkstreamevent-authorization}

No authorization required

### HTTP request headers {#workstreameventsdeletespecificworkstreamevent-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: Not defined

## **workstreamEventsSnapshot** {#workstreameventssnapshot}
> WorkstreamEvents workstreamEventsSnapshot(transferables)

/workstream_events [GET]

This will get a snapshot of all your workstream events.

### Example {#workstreameventssnapshot-example}
```kotlin
// Import classes:
import app.pieces.pieces-os-client.infrastructure.*
import app.pieces.pieces-os-client.models.*

val apiInstance = WorkstreamEventsApi()
val transferables : kotlin.Boolean = true // kotlin.Boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
try {
    val result : WorkstreamEvents = apiInstance.workstreamEventsSnapshot(transferables)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WorkstreamEventsApi#workstreamEventsSnapshot")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WorkstreamEventsApi#workstreamEventsSnapshot")
    e.printStackTrace()
}
```

### Parameters {#workstreameventssnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **kotlin.Boolean**| This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional]

### Return type {#workstreameventssnapshot-return-type}

[**WorkstreamEvents**](../models/WorkstreamEvents)

### Authorization {#workstreameventssnapshot-authorization}

No authorization required

### HTTP request headers {#workstreameventssnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

