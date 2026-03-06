# AsanaApiClient.Model.AllocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**StartDate** | **DateOnly** | The localized day on which the allocation starts. | [optional] 
**EndDate** | **DateOnly** | The localized day on which the allocation ends. | [optional] 
**Effort** | [**AllocationBaseEffort**](AllocationBaseEffort.md) |  | [optional] 
**Assignee** | **string** | Globally unique identifier for the user or placeholder assigned to the allocation. | [optional] 
**Parent** | **string** | Globally unique identifier for the project the allocation is on. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

