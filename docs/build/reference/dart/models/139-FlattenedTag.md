---
title: FlattenedTag | Dart SDK
---

# FlattenedTag

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] 
**id** | **String** |  | 
**text** | **String** |  | 
**mechanisms** | [**Map\<String, MechanismEnum\>**](MechanismEnum) | This is a Map\<String, MechanismEnum\>** where the the key is an asset id. | [optional] [default to const {}]
**assets** | [**FlattenedAssets**](FlattenedAssets) |  | [optional] 
**created** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**updated** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**deleted** | [**GroupedTimestamp**](GroupedTimestamp) |  | [optional] 
**category** | [**TagCategoryEnum**](TagCategoryEnum) |  | 
**relationship** | [**Relationship**](Relationship) |  | [optional] 
**interactions** | **int** | This is an optional value that will keep track of the number of times this has been interacted with. | [optional] 
**persons** | [**FlattenedPersons**](FlattenedPersons) |  | [optional] 
**score** | [**Score**](Score) |  | [optional] 


