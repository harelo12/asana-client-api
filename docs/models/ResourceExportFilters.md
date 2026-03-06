# AsanaApiClient.Model.ResourceExportFilters
Filters to apply to a resource that will be exported. These filters can be used to narrow down the resources that are included in the export.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignedByAny** | **List&lt;string&gt;** | Filter by the users who assigned the resource. This array accepts a list of user GIDs. This is only applicable to tasks. | [optional] 
**AssigneeAny** | **List&lt;string&gt;** | Filter by the users who are assigned to the resource. This array accepts a list of user GIDs. This is only applicable to tasks. | [optional] 
**CommentedOnByAny** | **List&lt;string&gt;** | Filter by the users who commented on the resource. This array accepts a list of user GIDs. | [optional] 
**CreatedAtAfter** | **DateTime** | Filter results to resources created after a specified date and time. | [optional] 
**CreatedAtBefore** | **DateTime** | Filter results to resources created before a specified date and time. | [optional] 
**CreatedByAny** | **List&lt;string&gt;** | Filter by the users who created the resource. This array accepts a list of user GIDs. | [optional] 
**FollowersAny** | **List&lt;string&gt;** | Filter by the users who are following the resource. This array accepts a list of user GIDs. | [optional] 
**LikedByAny** | **List&lt;string&gt;** | Filter by the users who liked the resource. This array accepts a list of user GIDs. | [optional] 
**ModifiedAtAfter** | **DateTime** | Filter results to resources modified after a specified date and time. | [optional] 
**ModifiedAtBefore** | **DateTime** | Filter results to resources modified before a specified date and time. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

