# AsanaApiClient.Model.WorkspaceMembershipResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**User** | [**UserCompact**](UserCompact.md) |  | [optional] 
**Workspace** | [**WorkspaceCompact**](WorkspaceCompact.md) |  | [optional] 
**UserTaskList** | [**UserTaskListCompact**](UserTaskListCompact.md) |  | [optional] 
**IsActive** | **bool** | Indicates whether the user is currently associated with the workspace. Returns &#x60;true&#x60; for users who have joined the workspace or have been invited but not yet accepted. | [optional] [readonly] 
**IsAdmin** | **bool** | Reflects if this user is an admin of the workspace. | [optional] [readonly] 
**IsGuest** | **bool** | Reflects if this user is a guest of the workspace. | [optional] [readonly] 
**IsViewOnly** | **bool** | Reflects if this user has view only license in the workspace. | [optional] [readonly] 
**VacationDates** | [**WorkspaceMembershipResponseAllOfVacationDates**](WorkspaceMembershipResponseAllOfVacationDates.md) |  | [optional] 
**CreatedAt** | **DateTime** | The time at which this resource was created. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

