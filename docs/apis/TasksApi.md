# AsanaApiClient.Api.TasksApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddDependenciesForTask**](TasksApi.md#adddependenciesfortask) | **POST** /tasks/{task_gid}/addDependencies | Set dependencies for a task |
| [**AddDependentsForTask**](TasksApi.md#adddependentsfortask) | **POST** /tasks/{task_gid}/addDependents | Set dependents for a task |
| [**AddFollowersForTask**](TasksApi.md#addfollowersfortask) | **POST** /tasks/{task_gid}/addFollowers | Add followers to a task |
| [**AddProjectForTask**](TasksApi.md#addprojectfortask) | **POST** /tasks/{task_gid}/addProject | Add a project to a task |
| [**AddTagForTask**](TasksApi.md#addtagfortask) | **POST** /tasks/{task_gid}/addTag | Add a tag to a task |
| [**CreateSubtaskForTask**](TasksApi.md#createsubtaskfortask) | **POST** /tasks/{task_gid}/subtasks | Create a subtask |
| [**CreateTask**](TasksApi.md#createtask) | **POST** /tasks | Create a task |
| [**DeleteTask**](TasksApi.md#deletetask) | **DELETE** /tasks/{task_gid} | Delete a task |
| [**DuplicateTask**](TasksApi.md#duplicatetask) | **POST** /tasks/{task_gid}/duplicate | Duplicate a task |
| [**GetDependenciesForTask**](TasksApi.md#getdependenciesfortask) | **GET** /tasks/{task_gid}/dependencies | Get dependencies from a task |
| [**GetDependentsForTask**](TasksApi.md#getdependentsfortask) | **GET** /tasks/{task_gid}/dependents | Get dependents from a task |
| [**GetSubtasksForTask**](TasksApi.md#getsubtasksfortask) | **GET** /tasks/{task_gid}/subtasks | Get subtasks from a task |
| [**GetTask**](TasksApi.md#gettask) | **GET** /tasks/{task_gid} | Get a task |
| [**GetTaskForCustomID**](TasksApi.md#gettaskforcustomid) | **GET** /workspaces/{workspace_gid}/tasks/custom_id/{custom_id} | Get a task for a given custom ID |
| [**GetTasks**](TasksApi.md#gettasks) | **GET** /tasks | Get multiple tasks |
| [**GetTasksForProject**](TasksApi.md#gettasksforproject) | **GET** /projects/{project_gid}/tasks | Get tasks from a project |
| [**GetTasksForSection**](TasksApi.md#gettasksforsection) | **GET** /sections/{section_gid}/tasks | Get tasks from a section |
| [**GetTasksForTag**](TasksApi.md#gettasksfortag) | **GET** /tags/{tag_gid}/tasks | Get tasks from a tag |
| [**GetTasksForUserTaskList**](TasksApi.md#gettasksforusertasklist) | **GET** /user_task_lists/{user_task_list_gid}/tasks | Get tasks from a user task list |
| [**RemoveDependenciesForTask**](TasksApi.md#removedependenciesfortask) | **POST** /tasks/{task_gid}/removeDependencies | Unlink dependencies from a task |
| [**RemoveDependentsForTask**](TasksApi.md#removedependentsfortask) | **POST** /tasks/{task_gid}/removeDependents | Unlink dependents from a task |
| [**RemoveFollowerForTask**](TasksApi.md#removefollowerfortask) | **POST** /tasks/{task_gid}/removeFollowers | Remove followers from a task |
| [**RemoveProjectForTask**](TasksApi.md#removeprojectfortask) | **POST** /tasks/{task_gid}/removeProject | Remove a project from a task |
| [**RemoveTagForTask**](TasksApi.md#removetagfortask) | **POST** /tasks/{task_gid}/removeTag | Remove a tag from a task |
| [**SearchTasksForWorkspace**](TasksApi.md#searchtasksforworkspace) | **GET** /workspaces/{workspace_gid}/tasks/search | Search tasks in a workspace |
| [**SetParentForTask**](TasksApi.md#setparentfortask) | **POST** /tasks/{task_gid}/setParent | Set the parent of a task |
| [**UpdateTask**](TasksApi.md#updatetask) | **PUT** /tasks/{task_gid} | Update a task |

<a id="adddependenciesfortask"></a>
# **AddDependenciesForTask**
> ApproveAccessRequest200Response AddDependenciesForTask (string taskGid, AddDependenciesForTaskRequest addDependenciesForTaskRequest, bool optPretty = null)

Set dependencies for a task

<b>Required scope: </b><code>tasks:write</code>  Marks a set of tasks as dependencies of this task, if they are not already dependencies. *A task can have at most 30 dependents and dependencies combined*.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **addDependenciesForTaskRequest** | [**AddDependenciesForTaskRequest**](AddDependenciesForTaskRequest.md) | The list of tasks to set as dependencies. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully set the specified dependencies on the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="adddependentsfortask"></a>
# **AddDependentsForTask**
> ApproveAccessRequest200Response AddDependentsForTask (string taskGid, AddDependentsForTaskRequest addDependentsForTaskRequest, bool optPretty = null)

Set dependents for a task

<b>Required scope: </b><code>tasks:write</code>  Marks a set of tasks as dependents of this task, if they are not already dependents. *A task can have at most 30 dependents and dependencies combined*.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **addDependentsForTaskRequest** | [**AddDependentsForTaskRequest**](AddDependentsForTaskRequest.md) | The list of tasks to add as dependents. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully set the specified dependents on the given task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addfollowersfortask"></a>
# **AddFollowersForTask**
> CreateTask201Response AddFollowersForTask (string taskGid, AddFollowersRequest addFollowersRequest, bool optPretty = null, List<string> optFields = null)

Add followers to a task

<b>Required scope: </b><code>tasks:write</code>  Adds followers to a task. Returns an empty data block. Each task can be associated with zero or more followers in the system. Requests to add/remove followers, if successful, will return the complete updated task record, described above.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **addFollowersRequest** | [**AddFollowersRequest**](AddFollowersRequest.md) | The followers to add to the task. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully added the specified followers to the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addprojectfortask"></a>
# **AddProjectForTask**
> ApproveAccessRequest200Response AddProjectForTask (string taskGid, AddProjectForTaskRequest addProjectForTaskRequest, bool optPretty = null)

Add a project to a task

<b>Required scope: </b><code>tasks:write</code>  Adds the task to the specified project, in the optional location specified. If no location arguments are given, the task will be added to the end of the project.  `addProject` can also be used to reorder a task within a project or section that already contains it.  **Positioning the task:** - Use `insert_before` or `insert_after` with a task ID to position relative to another task - Use `section` alone to add the task to the end of a section - Use `section` with `insert_after: null` to add to the **beginning** of a section - Use `section` with `insert_before: null` to add to the **end** of a section - Use `section` with `insert_before` or `insert_after` (non-null) to position relative to a task within that section. The anchor task must be in the specified section.  At most one of `insert_before` or `insert_after` should be specified (both cannot be used together).  A task can have at most 20 projects multi-homed to it.  Returns an empty data block.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **addProjectForTaskRequest** | [**AddProjectForTaskRequest**](AddProjectForTaskRequest.md) | The project to add the task to. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully added the specified project to the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addtagfortask"></a>
# **AddTagForTask**
> ApproveAccessRequest200Response AddTagForTask (string taskGid, AddTagForTaskRequest addTagForTaskRequest, bool optPretty = null)

Add a tag to a task

<b>Required scope: </b><code>tasks:write</code>  Adds a tag to a task. Returns an empty data block.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **addTagForTaskRequest** | [**AddTagForTaskRequest**](AddTagForTaskRequest.md) | The tag to add to the task. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully added the specified tag to the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createsubtaskfortask"></a>
# **CreateSubtaskForTask**
> CreateTask201Response CreateSubtaskForTask (string taskGid, CreateTaskRequest createTaskRequest, bool optPretty = null, List<string> optFields = null)

Create a subtask

<b>Required scope: </b><code>tasks:write</code>  Creates a new subtask and adds it to the parent task. Returns the full record for the newly created subtask.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **createTaskRequest** | [**CreateTaskRequest**](CreateTaskRequest.md) | The new subtask to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created the specified subtask. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createtask"></a>
# **CreateTask**
> CreateTask201Response CreateTask (CreateTaskRequest createTaskRequest, bool optPretty = null, List<string> optFields = null)

Create a task

<b>Required scope: </b><code>tasks:write</code>  Creating a new task is as easy as POSTing to the `/tasks` endpoint with a data block containing the fields you’d like to set on the task. Any unspecified fields will take on default values.  Every task is required to be created in a specific workspace, and this workspace cannot be changed once set. The workspace need not be set explicitly if you specify `projects` or a `parent` task instead.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createTaskRequest** | [**CreateTaskRequest**](CreateTaskRequest.md) | The task to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created a new task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletetask"></a>
# **DeleteTask**
> ApproveAccessRequest200Response DeleteTask (string taskGid, bool optPretty = null)

Delete a task

<b>Required scope: </b><code>tasks:delete</code>  A specific, existing task can be deleted by making a DELETE request on the URL for that task. Deleted tasks go into the “trash” of the user making the delete request. Tasks can be recovered from the trash within a period of 30 days; afterward they are completely removed from the system.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully deleted the specified task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="duplicatetask"></a>
# **DuplicateTask**
> GetJob200Response DuplicateTask (string taskGid, DuplicateTaskRequest duplicateTaskRequest, bool optPretty = null, List<string> optFields = null)

Duplicate a task

<b>Required scope: </b><code>tasks:write</code>  Creates and returns a job that will asynchronously handle the duplication.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **duplicateTaskRequest** | [**DuplicateTaskRequest**](DuplicateTaskRequest.md) | Describes the duplicate&#39;s name and the fields that will be duplicated. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetJob200Response**](GetJob200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created the job to handle duplication. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getdependenciesfortask"></a>
# **GetDependenciesForTask**
> GetTasks200Response GetDependenciesForTask (string taskGid, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get dependencies from a task

<b>Required scope: </b><code>tasks:read</code>  Returns the compact representations of all of the dependencies of a task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the specified task&#39;s dependencies. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getdependentsfortask"></a>
# **GetDependentsForTask**
> GetTasks200Response GetDependentsForTask (string taskGid, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get dependents from a task

<b>Required scope: </b><code>tasks:read</code>  Returns the compact representations of all of the dependents of a task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the specified dependents of the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getsubtasksfortask"></a>
# **GetSubtasksForTask**
> GetTasks200Response GetSubtasksForTask (string taskGid, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get subtasks from a task

<b>Required scope: </b><code>tasks:read</code>  Returns a compact representation of all of the subtasks of a task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the specified task&#39;s subtasks. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettask"></a>
# **GetTask**
> CreateTask201Response GetTask (string taskGid, bool optPretty = null, List<string> optFields = null)

Get a task

<b>Required scope: </b><code>tasks:read</code>  <table>   <tr>     <th>Field</th>     <th>Required Scope</th>   </tr>   <tr>     <td><code>memberships</code></td>     <td><code>projects:read</code>, <code>project_sections:read</code></td>   </tr>   <tr>     <td><code>actual_time_minutes</code></td>     <td><code>time_tracking_entries:read</code></td>   </tr> </table>  Returns the complete task record for a single task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the specified task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettaskforcustomid"></a>
# **GetTaskForCustomID**
> CreateTask201Response GetTaskForCustomID (string workspaceGid, string customId)

Get a task for a given custom ID

<b>Required scope: </b><code>tasks:read</code>  <table>   <tr>     <th>Field</th>     <th>Required Scope</th>   </tr>   <tr>     <td><code>memberships</code></td>     <td><code>projects:read</code>, <code>project_sections:read</code></td>   </tr>   <tr>     <td><code>actual_time_minutes</code></td>     <td><code>time_tracking_entries:read</code></td>   </tr> </table>  Returns a task given a custom ID shortcode.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **customId** | **string** | Generated custom ID for a task. |  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved task for given custom ID. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettasks"></a>
# **GetTasks**
> GetTasks200Response GetTasks (bool optPretty = null, int limit = null, string offset = null, string assignee = null, string project = null, string section = null, string workspace = null, DateTime completedSince = null, DateTime modifiedSince = null, List<string> optFields = null)

Get multiple tasks

<b>Required scope: </b><code>tasks:read</code>  Returns the compact task records for some filtered set of tasks. Use one or more of the parameters provided to filter the tasks returned. You must specify a `project` or `tag` if you do not specify `assignee` and `workspace`.  For more complex task retrieval, use [workspaces/{workspace_gid}/tasks/search](/reference/searchtasksforworkspace).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **assignee** | **string** | The assignee to filter tasks on. If searching for unassigned tasks, assignee.any &#x3D; null can be specified. *Note: If you specify &#x60;assignee&#x60;, you must also specify the &#x60;workspace&#x60; to filter on.* | [optional]  |
| **project** | **string** | The project to filter tasks on. | [optional]  |
| **section** | **string** | The section to filter tasks on. | [optional]  |
| **workspace** | **string** | The workspace to filter tasks on. *Note: If you specify &#x60;workspace&#x60;, you must also specify the &#x60;assignee&#x60; to filter on.* | [optional]  |
| **completedSince** | **DateTime** | Only return tasks that are either incomplete or that have been completed since this time. | [optional]  |
| **modifiedSince** | **DateTime** | Only return tasks that have been modified since the given time.  *Note: A task is considered “modified” if any of its properties change, or associations between it and other objects are modified (e.g.  a task being added to a project). A task is not considered modified just because another object it is associated with (e.g. a subtask) is modified. Actions that count as modifying the task include assigning, renaming, completing, and adding stories.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved requested tasks. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettasksforproject"></a>
# **GetTasksForProject**
> GetTasks200Response GetTasksForProject (string projectGid, string completedSince = null, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get tasks from a project

<b>Required scope: </b><code>tasks:read</code>  Returns the compact task records for all tasks within the given project, ordered by their priority within the project. Tasks can exist in more than one project at a time.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **completedSince** | **string** | Only return tasks that are either incomplete or that have been completed since this time. Accepts a date-time string or the keyword *now*.  | [optional]  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested project&#39;s tasks. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettasksforsection"></a>
# **GetTasksForSection**
> GetTasks200Response GetTasksForSection (string sectionGid, bool optPretty = null, int limit = null, string offset = null, string completedSince = null, List<string> optFields = null)

Get tasks from a section

<b>Required scope: </b><code>tasks:read</code>  *Board view only*: Returns the compact section records for all tasks within the given section.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sectionGid** | **string** | The globally unique identifier for the section. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **completedSince** | **string** | Only return tasks that are either incomplete or that have been completed since this time. Accepts a date-time string or the keyword *now*.  | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the section&#39;s tasks. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettasksfortag"></a>
# **GetTasksForTag**
> GetTasks200Response GetTasksForTag (string tagGid, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get tasks from a tag

<b>Required scope: </b><code>tasks:read</code>  Returns the compact task records for all tasks with the given tag. Tasks can have more than one tag at a time.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tagGid** | **string** | Globally unique identifier for the tag. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the tasks associated with the specified tag. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettasksforusertasklist"></a>
# **GetTasksForUserTaskList**
> GetTasks200Response GetTasksForUserTaskList (string userTaskListGid, string completedSince = null, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get tasks from a user task list

<b>Required scope: </b><code>tasks:read</code>  Returns the compact list of tasks in a user’s My Tasks list. *Note: Access control is enforced for this endpoint as with all Asana API endpoints, meaning a user’s private tasks will be filtered out if the API-authenticated user does not have access to them.* *Note: Both complete and incomplete tasks are returned by default unless they are filtered out (for example, setting `completed_since=now` will return only incomplete tasks, which is the default view for “My Tasks” in Asana.)*


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userTaskListGid** | **string** | Globally unique identifier for the user task list. |  |
| **completedSince** | **string** | Only return tasks that are either incomplete or that have been completed since this time. Accepts a date-time string or the keyword *now*.  | [optional]  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTasks200Response**](GetTasks200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the user task list&#39;s tasks. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removedependenciesfortask"></a>
# **RemoveDependenciesForTask**
> ApproveAccessRequest200Response RemoveDependenciesForTask (string taskGid, AddDependenciesForTaskRequest addDependenciesForTaskRequest, bool optPretty = null)

Unlink dependencies from a task

<b>Required scope: </b><code>tasks:write</code>  Unlinks a set of dependencies from this task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **addDependenciesForTaskRequest** | [**AddDependenciesForTaskRequest**](AddDependenciesForTaskRequest.md) | The list of tasks to unlink as dependencies. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully unlinked the dependencies from the specified task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removedependentsfortask"></a>
# **RemoveDependentsForTask**
> ApproveAccessRequest200Response RemoveDependentsForTask (string taskGid, AddDependentsForTaskRequest addDependentsForTaskRequest, bool optPretty = null)

Unlink dependents from a task

<b>Required scope: </b><code>tasks:write</code>  Unlinks a set of dependents from this task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **addDependentsForTaskRequest** | [**AddDependentsForTaskRequest**](AddDependentsForTaskRequest.md) | The list of tasks to remove as dependents. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully unlinked the specified tasks as dependents. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removefollowerfortask"></a>
# **RemoveFollowerForTask**
> CreateTask201Response RemoveFollowerForTask (string taskGid, RemoveFollowerForTaskRequest removeFollowerForTaskRequest, bool optPretty = null, List<string> optFields = null)

Remove followers from a task

<b>Required scope: </b><code>tasks:write</code>  Removes each of the specified followers from the task if they are following. Returns the complete, updated record for the affected task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **removeFollowerForTaskRequest** | [**RemoveFollowerForTaskRequest**](RemoveFollowerForTaskRequest.md) | The followers to remove from the task. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully removed the specified followers from the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removeprojectfortask"></a>
# **RemoveProjectForTask**
> ApproveAccessRequest200Response RemoveProjectForTask (string taskGid, RemoveProjectForTaskRequest removeProjectForTaskRequest, bool optPretty = null)

Remove a project from a task

<b>Required scope: </b><code>tasks:write</code>  Removes the task from the specified project. The task will still exist in the system, but it will not be in the project anymore.  Returns an empty data block.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **removeProjectForTaskRequest** | [**RemoveProjectForTaskRequest**](RemoveProjectForTaskRequest.md) | The project to remove the task from. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully removed the specified project from the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removetagfortask"></a>
# **RemoveTagForTask**
> ApproveAccessRequest200Response RemoveTagForTask (string taskGid, RemoveTagForTaskRequest removeTagForTaskRequest, bool optPretty = null)

Remove a tag from a task

<b>Required scope: </b><code>tasks:write</code>  Removes a tag from a task. Returns an empty data block.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **removeTagForTaskRequest** | [**RemoveTagForTaskRequest**](RemoveTagForTaskRequest.md) | The tag to remove from the task. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**ApproveAccessRequest200Response**](ApproveAccessRequest200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully removed the specified tag from the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchtasksforworkspace"></a>
# **SearchTasksForWorkspace**
> SearchTasksForWorkspace200Response SearchTasksForWorkspace (string workspaceGid, bool optPretty = null, string text = null, string resourceSubtype = null, string assigneeAny = null, string assigneeNot = null, string portfoliosAny = null, string projectsAny = null, string projectsNot = null, string projectsAll = null, string sectionsAny = null, string sectionsNot = null, string sectionsAll = null, string tagsAny = null, string tagsNot = null, string tagsAll = null, string teamsAny = null, string followersAny = null, string followersNot = null, string createdByAny = null, string createdByNot = null, string assignedByAny = null, string assignedByNot = null, string likedByNot = null, string commentedOnByNot = null, DateOnly dueOnBefore = null, DateOnly dueOnAfter = null, DateOnly dueOn = null, DateTime dueAtBefore = null, DateTime dueAtAfter = null, DateOnly startOnBefore = null, DateOnly startOnAfter = null, DateOnly startOn = null, DateOnly createdOnBefore = null, DateOnly createdOnAfter = null, DateOnly createdOn = null, DateTime createdAtBefore = null, DateTime createdAtAfter = null, DateOnly completedOnBefore = null, DateOnly completedOnAfter = null, DateOnly completedOn = null, DateTime completedAtBefore = null, DateTime completedAtAfter = null, DateOnly modifiedOnBefore = null, DateOnly modifiedOnAfter = null, DateOnly modifiedOn = null, DateTime modifiedAtBefore = null, DateTime modifiedAtAfter = null, bool isBlocking = null, bool isBlocked = null, bool hasAttachment = null, bool completed = null, bool isSubtask = null, string sortBy = null, bool sortAscending = null, List<string> optFields = null)

Search tasks in a workspace

<b>Required scope: </b><code>tasks:read</code>  To mirror the functionality of the Asana web app's advanced search feature, the Asana API has a task search endpoint that allows you to build complex filters to find and retrieve the exact data you need. #### Premium access Like the Asana web product's advance search feature, this search endpoint will only be available to premium Asana users. A user is premium if any of the following is true:  - The workspace in which the search is being performed is a premium workspace - The user is a member of a premium team inside the workspace  Even if a user is only a member of a premium team inside a non-premium workspace, search will allow them to find data anywhere in the workspace, not just inside the premium team. Making a search request using credentials of a non-premium user will result in a `402 Payment Required` error. #### Pagination Search results are not stable; repeating the same query multiple times may return the data in a different order, even if the data do not change. Because of this, the traditional [pagination](https://developers.asana.com/docs/#pagination) available elsewhere in the Asana API is not available here. However, you can paginate manually by sorting the search results by their creation time and then modifying each subsequent query to exclude data you have already seen. Page sizes are limited to a maximum of 100 items, and can be specified by the `limit` query parameter. #### Eventual consistency Changes in Asana (regardless of whether they’re made though the web product or the API) are forwarded to our search infrastructure to be indexed. This process can take between 10 and 60 seconds to complete under normal operation, and longer during some production incidents. Making a change to a task that would alter its presence in a particular search query will not be reflected immediately. This is also true of the advanced search feature in the web product. Because of this delay, the search endpoint is not suited for use cases that require immediate consistency after writes. If you need read-your-write behavior or strongly consistent results, we recommend using [Get multiple tasks](/reference/gettasks) instead. #### Rate limits You may receive a `429 Too Many Requests` response if you hit any of our [rate limits](https://developers.asana.com/docs/#rate-limits). #### Custom field parameters | Parameter name | Custom field type | Accepted type | |- --|- --|- --| | custom_fields.{gid}.is_set | All | Boolean | | custom_fields.{gid}.value | Text | String | | custom_fields.{gid}.value | Number | Number | | custom_fields.{gid}.value | Enum | Enum option ID | | custom_fields.{gid}.starts_with | Text only | String | | custom_fields.{gid}.ends_with | Text only | String | | custom_fields.{gid}.contains | Text only | String | | custom_fields.{gid}.less_than | Number only | Number | | custom_fields.{gid}.greater_than | Number only | Number |   For example, if the gid of the custom field is 12345, these query parameter to find tasks where it is set would be `custom_fields.12345.is_set=true`. To match an exact value for an enum custom field, use the gid of the desired enum option and not the name of the enum option: `custom_fields.12345.value=67890`.  **Not Supported**: searching for multiple exact matches of a custom field, searching for multi-enum custom field  *Note: If you specify `projects.any` and `sections.any`, you will receive tasks for the project **and** tasks for the section. If you're looking for only tasks in a section, omit the `projects.any` from the request.*


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **text** | **string** | Performs full-text search on both task name and description | [optional]  |
| **resourceSubtype** | **string** | Filters results by the task&#39;s resource_subtype | [optional] [default to milestone] |
| **assigneeAny** | **string** | Comma-separated list of user identifiers | [optional]  |
| **assigneeNot** | **string** | Comma-separated list of user identifiers | [optional]  |
| **portfoliosAny** | **string** | Comma-separated list of portfolio IDs | [optional]  |
| **projectsAny** | **string** | Comma-separated list of project IDs | [optional]  |
| **projectsNot** | **string** | Comma-separated list of project IDs | [optional]  |
| **projectsAll** | **string** | Comma-separated list of project IDs | [optional]  |
| **sectionsAny** | **string** | Comma-separated list of section or column IDs | [optional]  |
| **sectionsNot** | **string** | Comma-separated list of section or column IDs | [optional]  |
| **sectionsAll** | **string** | Comma-separated list of section or column IDs | [optional]  |
| **tagsAny** | **string** | Comma-separated list of tag IDs | [optional]  |
| **tagsNot** | **string** | Comma-separated list of tag IDs | [optional]  |
| **tagsAll** | **string** | Comma-separated list of tag IDs | [optional]  |
| **teamsAny** | **string** | Comma-separated list of team IDs | [optional]  |
| **followersAny** | **string** | Comma-separated list of user identifiers | [optional]  |
| **followersNot** | **string** | Comma-separated list of user identifiers | [optional]  |
| **createdByAny** | **string** | Comma-separated list of user identifiers | [optional]  |
| **createdByNot** | **string** | Comma-separated list of user identifiers | [optional]  |
| **assignedByAny** | **string** | Comma-separated list of user identifiers | [optional]  |
| **assignedByNot** | **string** | Comma-separated list of user identifiers | [optional]  |
| **likedByNot** | **string** | Comma-separated list of user identifiers | [optional]  |
| **commentedOnByNot** | **string** | Comma-separated list of user identifiers | [optional]  |
| **dueOnBefore** | **DateOnly** | ISO 8601 date string | [optional]  |
| **dueOnAfter** | **DateOnly** | ISO 8601 date string | [optional]  |
| **dueOn** | **DateOnly** | ISO 8601 date string or &#x60;null&#x60; | [optional]  |
| **dueAtBefore** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **dueAtAfter** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **startOnBefore** | **DateOnly** | ISO 8601 date string | [optional]  |
| **startOnAfter** | **DateOnly** | ISO 8601 date string | [optional]  |
| **startOn** | **DateOnly** | ISO 8601 date string or &#x60;null&#x60; | [optional]  |
| **createdOnBefore** | **DateOnly** | ISO 8601 date string | [optional]  |
| **createdOnAfter** | **DateOnly** | ISO 8601 date string | [optional]  |
| **createdOn** | **DateOnly** | ISO 8601 date string or &#x60;null&#x60; | [optional]  |
| **createdAtBefore** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **createdAtAfter** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **completedOnBefore** | **DateOnly** | ISO 8601 date string | [optional]  |
| **completedOnAfter** | **DateOnly** | ISO 8601 date string | [optional]  |
| **completedOn** | **DateOnly** | ISO 8601 date string or &#x60;null&#x60; | [optional]  |
| **completedAtBefore** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **completedAtAfter** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **modifiedOnBefore** | **DateOnly** | ISO 8601 date string | [optional]  |
| **modifiedOnAfter** | **DateOnly** | ISO 8601 date string | [optional]  |
| **modifiedOn** | **DateOnly** | ISO 8601 date string or &#x60;null&#x60; | [optional]  |
| **modifiedAtBefore** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **modifiedAtAfter** | **DateTime** | ISO 8601 datetime string | [optional]  |
| **isBlocking** | **bool** | Filter to incomplete tasks with dependents | [optional]  |
| **isBlocked** | **bool** | Filter to tasks with incomplete dependencies | [optional]  |
| **hasAttachment** | **bool** | Filter to tasks with attachments | [optional]  |
| **completed** | **bool** | Filter to completed tasks | [optional]  |
| **isSubtask** | **bool** | Filter to subtasks | [optional]  |
| **sortBy** | **string** | One of &#x60;due_date&#x60;, &#x60;created_at&#x60;, &#x60;completed_at&#x60;, &#x60;likes&#x60;, or &#x60;modified_at&#x60;, defaults to &#x60;modified_at&#x60; | [optional] [default to modified_at] |
| **sortAscending** | **bool** | Default &#x60;false&#x60; | [optional] [default to false] |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**SearchTasksForWorkspace200Response**](SearchTasksForWorkspace200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the section&#39;s tasks. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setparentfortask"></a>
# **SetParentForTask**
> CreateTask201Response SetParentForTask (string taskGid, SetParentForTaskRequest setParentForTaskRequest, bool optPretty = null, List<string> optFields = null)

Set the parent of a task

<b>Required scope: </b><code>tasks:write</code>  Updates the parent of a given task. This endpoint can be used to make a task a subtask of another task, or to remove its existing parent. When using `insert_before` and `insert_after`, at most one of those two options can be specified, and they must already be subtasks of the parent. Returns the complete, updated record of the affected [task](/reference/tasks#/task).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **setParentForTaskRequest** | [**SetParentForTaskRequest**](SetParentForTaskRequest.md) | The new parent of the subtask. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully changed the parent of the specified subtask. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatetask"></a>
# **UpdateTask**
> CreateTask201Response UpdateTask (string taskGid, CreateTaskRequest createTaskRequest, bool optPretty = null, List<string> optFields = null)

Update a task

<b>Required scope: </b><code>tasks:write</code>  A specific, existing task can be updated by making a PUT request on the URL for that task. Only the fields provided in the `data` block will be updated; any unspecified fields will remain unchanged.  When using this method, it is best to specify only those fields you wish to change, or else you may overwrite changes made by another user since you last retrieved the task.  Returns the complete updated task record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **createTaskRequest** | [**CreateTaskRequest**](CreateTaskRequest.md) | The task to update. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the specified task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

