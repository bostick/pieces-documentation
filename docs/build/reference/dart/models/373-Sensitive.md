---
title: Sensitive | Dart SDK
---

# Sensitive

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] 
**id** | **String** |  | 
**created** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**updated** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**deleted** | [**GroupedTimestamp**](GroupedTimestamp) |  | [optional] 
**asset** | [**FlattenedAsset**](FlattenedAsset) |  | 
**text** | **String** |  | 
**mechanism** | [**MechanismEnum**](MechanismEnum) |  | 
**category** | [**SensitiveCategoryEnum**](SensitiveCategoryEnum) |  | 
**severity** | [**SensitiveSeverityEnum**](SensitiveSeverityEnum) |  | 
**name** | **String** |  | 
**description** | **String** |  | 
**metadata** | [**SensitiveMetadata**](SensitiveMetadata) |  | [optional] 
**interactions** | **int** | This is an optional value that will keep track of the number of times this has been interacted with. | [optional] 
**score** | [**Score**](Score) |  | [optional] 


