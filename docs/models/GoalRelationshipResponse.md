# AsanaApiClient.Model.GoalRelationshipResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**ResourceSubtype** | **string** | The subtype of this resource. Different subtypes retain many of the same fields and behavior, but may render differently in Asana or represent resources with different semantic meaning. | [optional] [readonly] 
**SupportingResource** | [**GoalRelationshipCompactSupportingResource**](GoalRelationshipCompactSupportingResource.md) |  | [optional] 
**ContributionWeight** | **decimal** | The weight that the supporting resource&#39;s progress contributes to the supported goal&#39;s progress. This can be 0, 1, or any value in between. | [optional] 
**SupportedGoal** | [**GoalRelationshipBaseAllOfSupportedGoal**](GoalRelationshipBaseAllOfSupportedGoal.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

