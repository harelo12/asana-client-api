# AsanaApiClient.Model.ProjectDuplicateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | The name of the new project. | 
**Team** | **string** | Sets the team of the new project. If team is not defined, the new project will be in the same team as the the original project. | [optional] 
**Include** | **string** | A comma-separated list of elements to include when duplicating a project. Some elements are automatically included and cannot be excluded, while others are **optional** and must be explicitly specified in this field.  **Auto-included fields (non-configurable)** - Tasks - [Project Views](https://asana.com/features/project-management/project-views) (i.e., tabs in a project such as List, Board, Dashboard, etc.) - [Rules](https://help.asana.com/s/article/rules)  *Note: The Owner of the Rules copied to the new project is the user who performs the API call. If the duplication is performed using a [Service Account](/docs/authentication#/service-account), note that Service Accounts cannot access the UI to modify or pause Rules. To prevent unwanted automation behavior, consider pausing Rules in the source project before duplication — their active/paused state is preserved in the new project.*  **Optional fields (configurable)** - allocations - forms - members - notes - permissions - task_assignee - task_attachments - task_dates - task_dependencies - task_followers - task_notes - task_projects - task_subtasks - task_tags - task_templates - task_type_default | [optional] 
**ScheduleDates** | [**ProjectDuplicateRequestScheduleDates**](ProjectDuplicateRequestScheduleDates.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

