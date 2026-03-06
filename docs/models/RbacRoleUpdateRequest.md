# AsanaApiClient.Model.RbacRoleUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Name** | **string** | The name of the role. | [optional] 
**Description** | **string** | The description of the role. | [optional] 
**IsStandardRole** | **bool** | Whether the role is a standard role or a custom role. | [optional] 
**CreationTime** | **DateTime** | The time at which this role was created. | [optional] [readonly] 
**ModifiedAt** | **DateTime** | The time at which this role was last modified. | [optional] [readonly] 
**Workspace** | [**RbacRoleBaseAllOfWorkspace**](RbacRoleBaseAllOfWorkspace.md) |  | [optional] 
**BaseRoleType** | **string** | The base role type of the role. | [optional] 
**Permissions** | [**RbacRoleBaseAllOfPermissions**](RbacRoleBaseAllOfPermissions.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

