# AsanaApiClient.Api.ProjectsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddCustomFieldSettingForProject**](ProjectsApi.md#addcustomfieldsettingforproject) | **POST** /projects/{project_gid}/addCustomFieldSetting | Add a custom field to a project |
| [**AddFollowersForProject**](ProjectsApi.md#addfollowersforproject) | **POST** /projects/{project_gid}/addFollowers | Add followers to a project |
| [**AddMembersForProject**](ProjectsApi.md#addmembersforproject) | **POST** /projects/{project_gid}/addMembers | Add users to a project |
| [**CreateProject**](ProjectsApi.md#createproject) | **POST** /projects | Create a project |
| [**CreateProjectForTeam**](ProjectsApi.md#createprojectforteam) | **POST** /teams/{team_gid}/projects | Create a project in a team |
| [**CreateProjectForWorkspace**](ProjectsApi.md#createprojectforworkspace) | **POST** /workspaces/{workspace_gid}/projects | Create a project in a workspace |
| [**DeleteProject**](ProjectsApi.md#deleteproject) | **DELETE** /projects/{project_gid} | Delete a project |
| [**DuplicateProject**](ProjectsApi.md#duplicateproject) | **POST** /projects/{project_gid}/duplicate | Duplicate a project |
| [**GetProject**](ProjectsApi.md#getproject) | **GET** /projects/{project_gid} | Get a project |
| [**GetProjects**](ProjectsApi.md#getprojects) | **GET** /projects | Get multiple projects |
| [**GetProjectsForTask**](ProjectsApi.md#getprojectsfortask) | **GET** /tasks/{task_gid}/projects | Get projects a task is in |
| [**GetProjectsForTeam**](ProjectsApi.md#getprojectsforteam) | **GET** /teams/{team_gid}/projects | Get a team&#39;s projects |
| [**GetProjectsForWorkspace**](ProjectsApi.md#getprojectsforworkspace) | **GET** /workspaces/{workspace_gid}/projects | Get all projects in a workspace |
| [**GetTaskCountsForProject**](ProjectsApi.md#gettaskcountsforproject) | **GET** /projects/{project_gid}/task_counts | Get task count of a project |
| [**ProjectSaveAsTemplate**](ProjectsApi.md#projectsaveastemplate) | **POST** /projects/{project_gid}/saveAsTemplate | Create a project template from a project |
| [**RemoveCustomFieldSettingForProject**](ProjectsApi.md#removecustomfieldsettingforproject) | **POST** /projects/{project_gid}/removeCustomFieldSetting | Remove a custom field from a project |
| [**RemoveFollowersForProject**](ProjectsApi.md#removefollowersforproject) | **POST** /projects/{project_gid}/removeFollowers | Remove followers from a project |
| [**RemoveMembersForProject**](ProjectsApi.md#removemembersforproject) | **POST** /projects/{project_gid}/removeMembers | Remove users from a project |
| [**UpdateProject**](ProjectsApi.md#updateproject) | **PUT** /projects/{project_gid} | Update a project |

<a id="addcustomfieldsettingforproject"></a>
# **AddCustomFieldSettingForProject**
> AddCustomFieldSettingForGoal200Response AddCustomFieldSettingForProject (string projectGid, AddCustomFieldSettingForGoalRequest addCustomFieldSettingForGoalRequest, bool optPretty = null, List<string> optFields = null)

Add a custom field to a project

<b>Required scope: </b><code>projects:write</code>  Custom fields are associated with projects by way of custom field settings.  This method creates a setting for the project.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **addCustomFieldSettingForGoalRequest** | [**AddCustomFieldSettingForGoalRequest**](AddCustomFieldSettingForGoalRequest.md) | Information about the custom field setting. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**AddCustomFieldSettingForGoal200Response**](AddCustomFieldSettingForGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully added the custom field to the project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addfollowersforproject"></a>
# **AddFollowersForProject**
> CreateProject201Response AddFollowersForProject (string projectGid, AddFollowersForProjectRequest addFollowersForProjectRequest, bool optPretty = null, List<string> optFields = null)

Add followers to a project

Adds the specified list of users as followers to the project. Followers are a subset of members who have opted in to receive \"tasks added\" notifications for a project. Therefore, if the users are not already members of the project, they will also become members as a result of this operation. Returns the updated project record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **addFollowersForProjectRequest** | [**AddFollowersForProjectRequest**](AddFollowersForProjectRequest.md) | Information about the followers being added. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully added followers to the project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addmembersforproject"></a>
# **AddMembersForProject**
> CreateProject201Response AddMembersForProject (string projectGid, AddMembersForPortfolioRequest addMembersForPortfolioRequest, bool optPretty = null, List<string> optFields = null)

Add users to a project

Adds the specified list of users as members of the project. Note that a user being added as a member may also be added as a *follower* as a result of this operation. This is because the user's default notification settings (i.e., in the \"Notifications\" tab of \"My Profile Settings\") will override this endpoint's default behavior of setting \"Tasks added\" notifications to `false`. Returns the updated project record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **addMembersForPortfolioRequest** | [**AddMembersForPortfolioRequest**](AddMembersForPortfolioRequest.md) | Information about the members being added. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully added members to the project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createproject"></a>
# **CreateProject**
> CreateProject201Response CreateProject (CreateProjectRequest createProjectRequest, bool optPretty = null, List<string> optFields = null)

Create a project

<b>Required scope: </b><code>projects:write</code>  Create a new project in a workspace or team.  Every project is required to be created in a specific workspace or organization, and this cannot be changed once set. Note that you can use the `workspace` parameter regardless of whether or not it is an organization.  If the workspace for your project is an organization, you must also supply a `team` to share the project with.  Returns the full record of the newly created project.  **Deprecation notice:** The `team` parameter and the `private_to_team` value for `privacy_setting` are deprecated. When either is included in the request, the `Asana-Change` response header will indicate an affected deprecation. Clients should switch to using `POST /memberships` with `{ parent: project, member: team }` to share a project with a team after creation.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createProjectRequest** | [**CreateProjectRequest**](CreateProjectRequest.md) | The project to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully retrieved projects. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createprojectforteam"></a>
# **CreateProjectForTeam**
> CreateProject201Response CreateProjectForTeam (string teamGid, CreateProjectRequest createProjectRequest, bool optPretty = null, List<string> optFields = null)

Create a project in a team

<b>Required scope: </b><code>projects:write</code>  Creates a project shared with the given team.  Returns the full record of the newly created project.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **teamGid** | **string** | Globally unique identifier for the team. |  |
| **createProjectRequest** | [**CreateProjectRequest**](CreateProjectRequest.md) | The new project to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created the specified project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createprojectforworkspace"></a>
# **CreateProjectForWorkspace**
> CreateProject201Response CreateProjectForWorkspace (string workspaceGid, CreateProjectRequest createProjectRequest, bool optPretty = null, List<string> optFields = null)

Create a project in a workspace

<b>Required scope: </b><code>projects:write</code>  Creates a project in the workspace.  If the workspace for your project is an organization, you must also supply a team to share the project with.  Returns the full record of the newly created project.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **createProjectRequest** | [**CreateProjectRequest**](CreateProjectRequest.md) | The new project to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created a new project in the specified workspace. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteproject"></a>
# **DeleteProject**
> ApproveAccessRequest200Response DeleteProject (string projectGid, bool optPretty = null)

Delete a project

<b>Required scope: </b><code>projects:delete</code>  A specific, existing project can be deleted by making a DELETE request on the URL for that project.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
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
| **200** | Successfully deleted the specified project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="duplicateproject"></a>
# **DuplicateProject**
> GetJob200Response DuplicateProject (string projectGid, bool optPretty = null, List<string> optFields = null, DuplicateProjectRequest duplicateProjectRequest = null)

Duplicate a project

<b>Required scope: </b><code>projects:write</code>  Creates and returns a job that will asynchronously handle the duplication.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |
| **duplicateProjectRequest** | [**DuplicateProjectRequest**](DuplicateProjectRequest.md) | Describes the duplicate&#39;s name and the elements that will be duplicated. | [optional]  |

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

<a id="getproject"></a>
# **GetProject**
> CreateProject201Response GetProject (string projectGid, bool optPretty = null, List<string> optFields = null)

Get a project

<b>Required scope: </b><code>projects:read</code>  <table>   <tr>     <th>Field</th>     <th>Required Scope</th>   </tr>   <tr>     <td><code>team</code></td>     <td><code>teams:read</code></td>   </tr> </table>  Returns the complete project record for a single project.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprojects"></a>
# **GetProjects**
> GetItemsForPortfolio200Response GetProjects (bool optPretty = null, int limit = null, string offset = null, string workspace = null, string team = null, bool archived = null, List<string> optFields = null)

Get multiple projects

<b>Required scope: </b><code>projects:read</code>  Returns the compact project records for some filtered set of projects. Use one or more of the parameters provided to filter the projects returned. *Note: This endpoint may timeout for large domains. Try filtering by team!* **The `team` filter is deprecated.** Please use `GET /memberships` with `{ member: team, resource_subtype: project_membership }` to find projects shared with a team.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **workspace** | **string** | The workspace or organization to filter projects on. | [optional]  |
| **team** | **string** | **Deprecated.** The team to filter projects on. Please use &#x60;GET /memberships&#x60; with &#x60;{ member: team, resource_subtype: project_membership }&#x60; instead. | [optional]  |
| **archived** | **bool** | Only return projects whose &#x60;archived&#x60; field takes on the value of this parameter. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetItemsForPortfolio200Response**](GetItemsForPortfolio200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved projects. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprojectsfortask"></a>
# **GetProjectsForTask**
> GetItemsForPortfolio200Response GetProjectsForTask (string taskGid, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get projects a task is in

<b>Required scope: </b><code>projects:read</code>  Returns a compact representation of all of the projects the task is in.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetItemsForPortfolio200Response**](GetItemsForPortfolio200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the projects for the given task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprojectsforteam"></a>
# **GetProjectsForTeam**
> GetItemsForPortfolio200Response GetProjectsForTeam (string teamGid, bool optPretty = null, int limit = null, string offset = null, bool archived = null, List<string> optFields = null)

Get a team's projects

<b>Required scope: </b><code>projects:read</code>  Returns the compact project records for all projects in the team. *Deprecated: This endpoint is deprecated. Use `GET /memberships` with `member` set to the team GID and `resource_subtype` set to `project_membership` to fetch projects shared with a team.*


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **teamGid** | **string** | Globally unique identifier for the team. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **archived** | **bool** | Only return projects whose &#x60;archived&#x60; field takes on the value of this parameter. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetItemsForPortfolio200Response**](GetItemsForPortfolio200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested team&#39;s projects. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprojectsforworkspace"></a>
# **GetProjectsForWorkspace**
> GetItemsForPortfolio200Response GetProjectsForWorkspace (string workspaceGid, bool optPretty = null, int limit = null, string offset = null, bool archived = null, List<string> optFields = null)

Get all projects in a workspace

<b>Required scope: </b><code>projects:read</code>  Returns the compact project records for all projects in the workspace. *Note: This endpoint may timeout for large domains. To fetch projects shared with a specific team, use `GET /memberships` with `member` set to the team GID and `resource_subtype` set to `project_membership`.*


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **archived** | **bool** | Only return projects whose &#x60;archived&#x60; field takes on the value of this parameter. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetItemsForPortfolio200Response**](GetItemsForPortfolio200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested workspace&#39;s projects. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettaskcountsforproject"></a>
# **GetTaskCountsForProject**
> GetTaskCountsForProject200Response GetTaskCountsForProject (string projectGid, bool optPretty = null, List<string> optFields = null)

Get task count of a project

<b>Required scope: </b><code>projects:read</code>  <table>   <tr>     <th>Field</th>     <th>Required Scope</th>   </tr>   <tr>     <td><code>team</code></td>     <td><code>teams:read</code></td>   </tr> </table>  Get an object that holds task count fields. **All fields are excluded by default**. You must [opt in](/docs/inputoutput-options) using `opt_fields` to get any information from this endpoint.  This endpoint has an additional [rate limit](/docs/rate-limits) and each field counts especially high against our [cost limits](/docs/rate-limits#cost-limits).  Milestones are just tasks, so they are included in the `num_tasks`, `num_incomplete_tasks`, and `num_completed_tasks` counts.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTaskCountsForProject200Response**](GetTaskCountsForProject200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested project&#39;s task counts. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="projectsaveastemplate"></a>
# **ProjectSaveAsTemplate**
> GetJob200Response ProjectSaveAsTemplate (string projectGid, ProjectSaveAsTemplateRequest projectSaveAsTemplateRequest, bool optPretty = null, List<string> optFields = null)

Create a project template from a project

Creates and returns a job that will asynchronously handle the project template creation.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **projectSaveAsTemplateRequest** | [**ProjectSaveAsTemplateRequest**](ProjectSaveAsTemplateRequest.md) | Describes the inputs used for creating a project template, such as the resulting project template&#39;s name, which team it should be created in. |  |
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
| **201** | Successfully created the job to handle project template creation. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removecustomfieldsettingforproject"></a>
# **RemoveCustomFieldSettingForProject**
> ApproveAccessRequest200Response RemoveCustomFieldSettingForProject (string projectGid, RemoveCustomFieldSettingForGoalRequest removeCustomFieldSettingForGoalRequest, bool optPretty = null)

Remove a custom field from a project

<b>Required scope: </b><code>projects:write</code>  Removes a custom field setting from a project.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **removeCustomFieldSettingForGoalRequest** | [**RemoveCustomFieldSettingForGoalRequest**](RemoveCustomFieldSettingForGoalRequest.md) | Information about the custom field setting being removed. |  |
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
| **200** | Successfully removed the custom field from the project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removefollowersforproject"></a>
# **RemoveFollowersForProject**
> CreateProject201Response RemoveFollowersForProject (string projectGid, RemoveFollowersForProjectRequest removeFollowersForProjectRequest, bool optPretty = null, List<string> optFields = null)

Remove followers from a project

Removes the specified list of users from following the project, this will not affect project membership status. Returns the updated project record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **removeFollowersForProjectRequest** | [**RemoveFollowersForProjectRequest**](RemoveFollowersForProjectRequest.md) | Information about the followers being removed. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully removed followers from the project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removemembersforproject"></a>
# **RemoveMembersForProject**
> CreateProject201Response RemoveMembersForProject (string projectGid, RemoveMembersForPortfolioRequest removeMembersForPortfolioRequest, bool optPretty = null, List<string> optFields = null)

Remove users from a project

Removes the specified list of users from members of the project. Returns the updated project record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **removeMembersForPortfolioRequest** | [**RemoveMembersForPortfolioRequest**](RemoveMembersForPortfolioRequest.md) | Information about the members being removed. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully removed the members from the project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateproject"></a>
# **UpdateProject**
> CreateProject201Response UpdateProject (string projectGid, UpdateProjectRequest updateProjectRequest, bool optPretty = null, List<string> optFields = null)

Update a project

<b>Required scope: </b><code>projects:write</code>  A specific, existing project can be updated by making a PUT request on the URL for that project. Only the fields provided in the `data` block will be updated; any unspecified fields will remain unchanged.  When using this method, it is best to specify only those fields you wish to change, or else you may overwrite changes made by another user since you last retrieved the task.  Returns the complete updated project record.  **Deprecation notice:** Updating the `team` field is deprecated. When this field is included in the request, the `Asana-Change` response header will indicate an affected deprecation. Clients should switch to using `POST /memberships` with `{ parent: project, member: team }` to share a project with a team.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **updateProjectRequest** | [**UpdateProjectRequest**](UpdateProjectRequest.md) | The updated fields for the project. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the project. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

