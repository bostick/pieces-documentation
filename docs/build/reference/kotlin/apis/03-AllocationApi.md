---
title: Allocation API | Kotlin SDK
---

# Allocation API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**allocationSnapshot**](#allocationsnapshot) | **GET** /allocation/\{allocation\} | /allocation/\{allocation\} [GET]
[**allocationUpdate**](#allocationupdate) | **POST** /allocation/update | /allocation/update [POST]


## **allocationSnapshot** {#allocationsnapshot}
> AllocationCloud allocationSnapshot(allocation)

/allocation/\{allocation\} [GET]

This will get a snapshot of a specific allocation.

### Example {#allocationsnapshot-example}
```kotlin
// Import classes:
import app.pieces.pieces-os-client.infrastructure.*
import app.pieces.pieces-os-client.models.*

val apiInstance = AllocationApi()
val allocation : kotlin.String = allocation_example // kotlin.String | 
try {
    val result : AllocationCloud = apiInstance.allocationSnapshot(allocation)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AllocationApi#allocationSnapshot")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AllocationApi#allocationSnapshot")
    e.printStackTrace()
}
```

### Parameters {#allocationsnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allocation** | **kotlin.String**|  |

### Return type {#allocationsnapshot-return-type}

[**AllocationCloud**](../models/AllocationCloud)

### Authorization {#allocationsnapshot-authorization}

No authorization required

### HTTP request headers {#allocationsnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

## **allocationUpdate** {#allocationupdate}
> AllocationCloud allocationUpdate(allocationCloud)

/allocation/update [POST]

This will update a specific allocation.

### Example {#allocationupdate-example}
```kotlin
// Import classes:
import app.pieces.pieces-os-client.infrastructure.*
import app.pieces.pieces-os-client.models.*

val apiInstance = AllocationApi()
val allocationCloud : AllocationCloud =  // AllocationCloud | 
try {
    val result : AllocationCloud = apiInstance.allocationUpdate(allocationCloud)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AllocationApi#allocationUpdate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AllocationApi#allocationUpdate")
    e.printStackTrace()
}
```

### Parameters {#allocationupdate-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allocationCloud** | [**AllocationCloud**](../models/AllocationCloud)|  | [optional]

### Return type {#allocationupdate-return-type}

[**AllocationCloud**](../models/AllocationCloud)

### Authorization {#allocationupdate-authorization}

No authorization required

### HTTP request headers {#allocationupdate-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json

