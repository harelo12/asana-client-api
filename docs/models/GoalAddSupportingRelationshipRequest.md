# AsanaApiClient.Model.GoalAddSupportingRelationshipRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SupportingResource** | **string** | The gid of the supporting resource to add to the parent goal. Must be the gid of a goal, project, task, or portfolio. | 
**InsertBefore** | **string** | An id of a subgoal of this parent goal. The new subgoal will be added before the one specified here. &#x60;insert_before&#x60; and &#x60;insert_after&#x60; parameters cannot both be specified. Currently only supported when adding a subgoal. | [optional] 
**InsertAfter** | **string** | An id of a subgoal of this parent goal. The new subgoal will be added after the one specified here. &#x60;insert_before&#x60; and &#x60;insert_after&#x60; parameters cannot both be specified. Currently only supported when adding a subgoal. | [optional] 
**ContributionWeight** | **decimal** | Defines how much the supporting goal’s progress contributes to the parent goal’s overall progress. When used with automatically calculated [Goal Metrics](/reference/creategoalmetric) (such as &#x60;progress_source &#x3D; subgoal_progress&#x60;), this value must be greater than 0 for the subgoal to count toward the parent goal’s progress. Accepts a number between 0 and 1 (inclusive). Defaults to &#x60;0&#x60;. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

