# AsanaApiClient.Model.TimeTrackingEntryCompact
A generic Asana Resource, containing a globally unique identifier.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**DurationMinutes** | **int** | Time in minutes tracked by the entry. | [optional] 
**EnteredOn** | **DateOnly** | The day that this entry is logged on. | [optional] 
**AttributableTo** | [**TimeTrackingEntryCompactAttributableTo**](TimeTrackingEntryCompactAttributableTo.md) |  | [optional] 
**CreatedBy** | [**UserCompact**](UserCompact.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

