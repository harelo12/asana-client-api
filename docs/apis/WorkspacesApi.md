# AsanaApiClient.Api.WorkspacesApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUserForWorkspace**](WorkspacesApi.md#adduserforworkspace) | **POST** /workspaces/{workspace_gid}/addUser | Add a user to a workspace or organization |
| [**GetWorkspace**](WorkspacesApi.md#getworkspace) | **GET** /workspaces/{workspace_gid} | Get a workspace |
| [**GetWorkspaceEvents**](WorkspacesApi.md#getworkspaceevents) | **GET** /workspaces/{workspace_gid}/events | Get workspace events |
| [**GetWorkspaces**](WorkspacesApi.md#getworkspaces) | **GET** /workspaces | Get multiple workspaces |
| [**RemoveUserForWorkspace**](WorkspacesApi.md#removeuserforworkspace) | **POST** /workspaces/{workspace_gid}/removeUser | Remove a user from a workspace or organization |
| [**UpdateWorkspace**](WorkspacesApi.md#updateworkspace) | **PUT** /workspaces/{workspace_gid} | Update a workspace |

<a id="adduserforworkspace"></a>
# **AddUserForWorkspace**
> AddUserForWorkspace200Response AddUserForWorkspace (string workspaceGid, AddUserForWorkspaceRequest addUserForWorkspaceRequest, bool optPretty = null, List<string> optFields = null)

Add a user to a workspace or organization

Add a user to a workspace or organization. The user can be referenced by their globally unique user ID or their email address. Returns the full user record for the invited user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **addUserForWorkspaceRequest** | [**AddUserForWorkspaceRequest**](AddUserForWorkspaceRequest.md) | The user to add to the workspace. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**AddUserForWorkspace200Response**](AddUserForWorkspace200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The user was added successfully to the workspace or organization. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getworkspace"></a>
# **GetWorkspace**
> GetWorkspace200Response GetWorkspace (string workspaceGid, bool optPretty = null, List<string> optFields = null)

Get a workspace

<b>Required scope: </b><code>workspaces:read</code>  Returns the full workspace record for a single workspace.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetWorkspace200Response**](GetWorkspace200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return the full workspace record. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getworkspaceevents"></a>
# **GetWorkspaceEvents**
> GetEvents200Response GetWorkspaceEvents (string workspaceGid, bool optPretty = null, string sync = null)

Get workspace events

Returns the full record for all events that have occurred since the sync token was created. The response is a list of events and the schema of each event is as described [here](/reference/events). Asana limits a single sync token to 1000 events. If more than 1000 events exist for a given domain, `has_more: true` will be returned in the response, indicating that there are more events to pull.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **sync** | **string** | A sync token received from the last request, or none on first sync. Events will be returned from the point in time that the sync token was generated. *Note: On your first request, omit the sync token. The response will be the same as for an expired sync token, and will include a new valid sync token. If the sync token is too old (which may happen from time to time) the API will return a &#x60;412 Precondition Failed&#x60; error, and include a fresh sync token in the response.* | [optional]  |

### Return type

[**GetEvents200Response**](GetEvents200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved events. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getworkspaces"></a>
# **GetWorkspaces**
> GetWorkspaces200Response GetWorkspaces (bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get multiple workspaces

<b>Required scope: </b><code>workspaces:read</code>  Returns the compact records for all workspaces visible to the authorized user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetWorkspaces200Response**](GetWorkspaces200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return all workspaces visible to the authorized user. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removeuserforworkspace"></a>
# **RemoveUserForWorkspace**
> ApproveAccessRequest200Response RemoveUserForWorkspace (string workspaceGid, RemoveUserForWorkspaceRequest removeUserForWorkspaceRequest, bool optPretty = null)

Remove a user from a workspace or organization

Remove a user from a workspace or organization.  The user making this call must be an admin in the workspace. The user can be referenced by their globally unique user ID or their email address.  When invoked using a **Service Account Token (SAT)**, this endpoint follows the same behavior as the [SCIM API Delete endpoint](/docs/scim). To learn more about how Asana handles user deprovisioning, refer to our [Help Center article on deprovisioning users](https://help.asana.com/s/article/user-deprovisioning).  When invoked using a **Personal Access Token (PAT)**, the endpoint behaves similarly, except that ownership of the user’s resources is transferred to the **PAT owner** instead of the admin [specified in the Admin Console](https://help.asana.com/s/article/user-deprovisioning#gl-deprovisioning).  **Note:** If you wish to retain access to a user’s private resources (i.e., those visible only to that user), you have to make them public manually (or ask the user to do so) before removal.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **removeUserForWorkspaceRequest** | [**RemoveUserForWorkspaceRequest**](RemoveUserForWorkspaceRequest.md) | The user to remove from the workspace. |  |
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
| **200** | The user was removed successfully to the workspace or organization. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateworkspace"></a>
# **UpdateWorkspace**
> GetWorkspace200Response UpdateWorkspace (string workspaceGid, UpdateWorkspaceRequest updateWorkspaceRequest, bool optPretty = null, List<string> optFields = null)

Update a workspace

A specific, existing workspace can be updated by making a PUT request on the URL for that workspace. Only the fields provided in the data block will be updated; any unspecified fields will remain unchanged. Currently the only field that can be modified for a workspace is its name. Returns the complete, updated workspace record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **updateWorkspaceRequest** | [**UpdateWorkspaceRequest**](UpdateWorkspaceRequest.md) | The workspace object with all updated properties. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetWorkspace200Response**](GetWorkspace200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Update for the workspace was successful. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

