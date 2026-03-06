# AsanaApiClient.Model.AccessRequestResponse
A *access request* object represents a request to access a shareable resource within Asana. It includes the requester's information, approval status, and target resource details.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Message** | **string** | The message included in the access request, if any. | [optional] 
**ApprovalStatus** | **string** | The current approval status of the request. | [optional] 
**Requester** | [**UserCompact**](UserCompact.md) |  | [optional] 
**Target** | [**AccessRequestTargetIdCompact**](AccessRequestTargetIdCompact.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

