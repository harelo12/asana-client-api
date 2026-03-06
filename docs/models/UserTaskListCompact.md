# AsanaApiClient.Model.UserTaskListCompact
A user task list represents the tasks assigned to a particular user. It provides API access to a user’s [My tasks](https://asana.com/guide/help/fundamentals/my-tasks) view in Asana.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Name** | **string** | The name of the user task list. | [optional] 
**Owner** | [**UserCompact**](UserCompact.md) | The owner of the user task list, i.e. the person whose My Tasks is represented by this resource. | [optional] [readonly] 
**Workspace** | [**WorkspaceCompact**](WorkspaceCompact.md) | The workspace in which the user task list is located. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

