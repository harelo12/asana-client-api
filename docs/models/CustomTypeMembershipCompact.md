# AsanaApiClient.Model.CustomTypeMembershipCompact
This object describes a user or team's membership to a custom type including their level of access (Admin, Editor, User, or Viewer).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**ResourceSubtype** | **string** | Type of the membership. | [optional] 
**Parent** | [**CustomTypeCompact**](CustomTypeCompact.md) |  | [optional] 
**Member** | [**MemberCompact**](MemberCompact.md) |  | [optional] 
**AccessLevel** | **string** | Whether the member has admin, editor, user, or viewer access to the custom type. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

