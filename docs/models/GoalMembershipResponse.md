# AsanaApiClient.Model.GoalMembershipResponse

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
**User** | [**GoalMembershipResponseAllOfUser**](GoalMembershipResponseAllOfUser.md) |  | [optional] 
**Workspace** | [**GoalMembershipResponseAllOfWorkspace**](GoalMembershipResponseAllOfWorkspace.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

