# AsanaApiClient.Model.AllocationBase
A generic Asana Resource, containing a globally unique identifier.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**StartDate** | **DateOnly** | The localized day on which the allocation starts. | [optional] 
**EndDate** | **DateOnly** | The localized day on which the allocation ends. | [optional] 
**Effort** | [**AllocationBaseEffort**](AllocationBaseEffort.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

