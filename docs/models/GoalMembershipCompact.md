# AsanaApiClient.Model.GoalMembershipCompact

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] 
**ResourceSubtype** | **string** | The type of membership. | [optional] [readonly] 
**Member** | [**MemberCompact**](MemberCompact.md) |  | [optional] 
**Parent** | [**GoalMembershipBaseParent**](GoalMembershipBaseParent.md) |  | [optional] 
**Role** | **string** | *Deprecated: Describes if the member is a commenter or editor in goal.* | [optional] 
**AccessLevel** | **string** | \&quot;Describes the membership access level for the goal. This is preferred over role.\&quot; | [optional] 
**Goal** | [**GoalMembershipBaseGoal**](GoalMembershipBaseGoal.md) |  | [optional] 
**IsCommenter** | **bool** | *Deprecated: new integrations should prefer the &#x60;access_level&#x60; field.* Describes if the member is comment only in goal. This field is deprecated and will always be null. | [optional] [readonly] 
**IsEditor** | **bool** | *Deprecated: new integrations should prefer the &#x60;access_level&#x60; field.* Describes if the member is editor in goal. This field is deprecated and will always be null. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

