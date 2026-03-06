# AsanaApiClient.Model.TimeTrackingEntryBase

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**DurationMinutes** | **int** | Time in minutes tracked by the entry. | [optional] 
**EnteredOn** | **DateOnly** | The day that this entry is logged on. | [optional] 
**AttributableTo** | [**TimeTrackingEntryCompactAttributableTo**](TimeTrackingEntryCompactAttributableTo.md) |  | [optional] 
**CreatedBy** | [**UserCompact**](UserCompact.md) |  | [optional] 
**Task** | [**TaskCompact**](TaskCompact.md) |  | [optional] 
**CreatedAt** | **DateTime** | The time at which this resource was created. | [optional] [readonly] 
**ApprovalStatus** | **string** | *Optional*. The current approval status of the entry. | [optional] [readonly] 
**BillableStatus** | **string** | *Optional*. The current billable status of the entry. | [optional] [readonly] 
**Description** | **string** | *Optional*. The description of the entry. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

