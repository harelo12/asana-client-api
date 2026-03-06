# AsanaApiClient.Model.TaskAddProjectRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Project** | **string** | The project to add the task to. | 
**InsertAfter** | **string** | A task in the project to insert the task after, or &#x60;null&#x60; to insert at the beginning of the list. When used with &#x60;section&#x60;, &#x60;null&#x60; will insert at the beginning of the specified section, otherwise the task must be in the specified section. | [optional] 
**InsertBefore** | **string** | A task in the project to insert the task before, or &#x60;null&#x60; to insert at the end of the list. When used with &#x60;section&#x60;, &#x60;null&#x60; will insert at the end of the specified section, otherwise the task must be in the specified section. | [optional] 
**Section** | **string** | A section in the project to insert the task into. The task will be inserted at the bottom of the section unless combined with &#x60;insert_before: null&#x60; (end of section) or &#x60;insert_after: null&#x60; (beginning of section). Can also be combined with non-null &#x60;insert_before&#x60; or &#x60;insert_after&#x60; to position relative to a task within the section. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

