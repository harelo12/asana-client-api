# AsanaApiClient.Model.CustomFieldMembershipCompact
This object describes a user or team's membership to a custom field including their level of access (Admin, Editor, or User).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**ResourceSubtype** | **string** | Type of the membership. | [optional] 
**Parent** | [**CustomFieldCompact**](CustomFieldCompact.md) |  | [optional] 
**Member** | [**MemberCompact**](MemberCompact.md) |  | [optional] 
**AccessLevel** | **string** | Whether the member has admin, editor, or user access to the custom field. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

