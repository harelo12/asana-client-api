# AsanaApiClient.Model.AllocationResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**StartDate** | **DateOnly** | The localized day on which the allocation starts. | [optional] 
**EndDate** | **DateOnly** | The localized day on which the allocation ends. | [optional] 
**Effort** | [**AllocationBaseEffort**](AllocationBaseEffort.md) |  | [optional] 
**Assignee** | [**AllocationResponseAllOfAssignee**](AllocationResponseAllOfAssignee.md) |  | [optional] 
**CreatedBy** | **Object** |  | [optional] 
**Parent** | **Object** |  | [optional] 
**ResourceSubtype** | **string** | The subtype of the allocation. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

