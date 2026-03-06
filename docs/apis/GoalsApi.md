# AsanaApiClient.Api.GoalsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddCustomFieldSettingForGoal**](GoalsApi.md#addcustomfieldsettingforgoal) | **POST** /goals/{goal_gid}/addCustomFieldSetting | Add a custom field to a goal |
| [**AddFollowers**](GoalsApi.md#addfollowers) | **POST** /goals/{goal_gid}/addFollowers | Add a collaborator to a goal |
| [**CreateGoal**](GoalsApi.md#creategoal) | **POST** /goals | Create a goal |
| [**CreateGoalMetric**](GoalsApi.md#creategoalmetric) | **POST** /goals/{goal_gid}/setMetric | Create a goal metric |
| [**DeleteGoal**](GoalsApi.md#deletegoal) | **DELETE** /goals/{goal_gid} | Delete a goal |
| [**GetGoal**](GoalsApi.md#getgoal) | **GET** /goals/{goal_gid} | Get a goal |
| [**GetGoals**](GoalsApi.md#getgoals) | **GET** /goals | Get goals |
| [**GetParentGoalsForGoal**](GoalsApi.md#getparentgoalsforgoal) | **GET** /goals/{goal_gid}/parentGoals | Get parent goals from a goal |
| [**RemoveCustomFieldSettingForGoal**](GoalsApi.md#removecustomfieldsettingforgoal) | **POST** /goals/{goal_gid}/removeCustomFieldSetting | Remove a custom field from a goal |
| [**RemoveFollowers**](GoalsApi.md#removefollowers) | **POST** /goals/{goal_gid}/removeFollowers | Remove a collaborator from a goal |
| [**UpdateGoal**](GoalsApi.md#updategoal) | **PUT** /goals/{goal_gid} | Update a goal |
| [**UpdateGoalMetric**](GoalsApi.md#updategoalmetric) | **POST** /goals/{goal_gid}/setMetricCurrentValue | Update a goal metric |

<a id="addcustomfieldsettingforgoal"></a>
# **AddCustomFieldSettingForGoal**
> AddCustomFieldSettingForGoal200Response AddCustomFieldSettingForGoal (string goalGid, AddCustomFieldSettingForGoalRequest addCustomFieldSettingForGoalRequest, bool optPretty = null)

Add a custom field to a goal

<b>Required scope: </b><code>goals:write</code>  Custom fields are associated with goals by way of custom field settings.  This method creates a setting for the goal.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **addCustomFieldSettingForGoalRequest** | [**AddCustomFieldSettingForGoalRequest**](AddCustomFieldSettingForGoalRequest.md) | Information about the custom field setting. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

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
| **200** | Successfully added the custom field to the goal. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addfollowers"></a>
# **AddFollowers**
> GetGoal200Response AddFollowers (string goalGid, AddFollowersRequest addFollowersRequest, bool optPretty = null, List<string> optFields = null)

Add a collaborator to a goal

Adds followers to a goal. Returns the goal the followers were added to. Each goal can be associated with zero or more followers in the system. Requests to add/remove followers, if successful, will return the complete updated goal record, described above.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **addFollowersRequest** | [**AddFollowersRequest**](AddFollowersRequest.md) | The followers to be added as collaborators |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoal200Response**](GetGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully added users as collaborators. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="creategoal"></a>
# **CreateGoal**
> GetGoal200Response CreateGoal (CreateGoalRequest createGoalRequest, bool optPretty = null, List<string> optFields = null)

Create a goal

Creates a new goal in a workspace or team.  Returns the full record of the newly created goal.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createGoalRequest** | [**CreateGoalRequest**](CreateGoalRequest.md) | The goal to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoal200Response**](GetGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created a new goal. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="creategoalmetric"></a>
# **CreateGoalMetric**
> GetGoal200Response CreateGoalMetric (string goalGid, CreateGoalMetricRequest createGoalMetricRequest, bool optPretty = null, List<string> optFields = null)

Create a goal metric

Creates and adds a goal metric to a specified goal. Note that this replaces an existing goal metric if one already exists.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **createGoalMetricRequest** | [**CreateGoalMetricRequest**](CreateGoalMetricRequest.md) | The goal metric to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoal200Response**](GetGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully created a new goal metric. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletegoal"></a>
# **DeleteGoal**
> ApproveAccessRequest200Response DeleteGoal (string goalGid, bool optPretty = null)

Delete a goal

A specific, existing goal can be deleted by making a DELETE request on the URL for that goal.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
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
| **200** | Successfully deleted the specified goal. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getgoal"></a>
# **GetGoal**
> GetGoal200Response GetGoal (string goalGid, bool optPretty = null, List<string> optFields = null)

Get a goal

<b>Required scope: </b><code>goals:read</code>  <table>   <tr>     <th>Field</th>     <th>Required Scope</th>   </tr>   <tr>     <td><code>time_period</code></td>     <td><code>time_periods:read</code></td>   </tr> </table>  Returns the complete goal record for a single goal.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoal200Response**](GetGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the record for a single goal. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getgoals"></a>
# **GetGoals**
> GetGoals200Response GetGoals (bool optPretty = null, string portfolio = null, string project = null, string task = null, bool isWorkspaceLevel = null, string team = null, string workspace = null, List<string> timePeriods = null, int limit = null, string offset = null, List<string> optFields = null)

Get goals

<b>Required scope: </b><code>goals:read</code>  Returns compact goal records.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **portfolio** | **string** | Globally unique identifier for supporting portfolio. | [optional]  |
| **project** | **string** | Globally unique identifier for supporting project. | [optional]  |
| **task** | **string** | Globally unique identifier for supporting task. | [optional]  |
| **isWorkspaceLevel** | **bool** | Filter to goals with is_workspace_level set to query value. Must be used with the workspace parameter. | [optional]  |
| **team** | **string** | Globally unique identifier for the team. | [optional]  |
| **workspace** | **string** | Globally unique identifier for the workspace. | [optional]  |
| **timePeriods** | [**List&lt;string&gt;**](string.md) | Globally unique identifiers for the time periods. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoals200Response**](GetGoals200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested goals. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getparentgoalsforgoal"></a>
# **GetParentGoalsForGoal**
> GetParentGoalsForGoal200Response GetParentGoalsForGoal (string goalGid, bool optPretty = null, List<string> optFields = null)

Get parent goals from a goal

<b>Required scope: </b><code>goals:read</code>  Returns a compact representation of all of the parent goals of a goal.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetParentGoalsForGoal200Response**](GetParentGoalsForGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the specified goal&#39;s parent goals. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removecustomfieldsettingforgoal"></a>
# **RemoveCustomFieldSettingForGoal**
> ApproveAccessRequest200Response RemoveCustomFieldSettingForGoal (string goalGid, RemoveCustomFieldSettingForGoalRequest removeCustomFieldSettingForGoalRequest, bool optPretty = null)

Remove a custom field from a goal

<b>Required scope: </b><code>goals:write</code>  Removes a custom field setting from a goal.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
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
| **200** | Successfully removed the custom field from the goal. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removefollowers"></a>
# **RemoveFollowers**
> GetGoal200Response RemoveFollowers (string goalGid, AddFollowersRequest addFollowersRequest, bool optPretty = null, List<string> optFields = null)

Remove a collaborator from a goal

Removes followers from a goal. Returns the goal the followers were removed from. Each goal can be associated with zero or more followers in the system. Requests to add/remove followers, if successful, will return the complete updated goal record, described above.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **addFollowersRequest** | [**AddFollowersRequest**](AddFollowersRequest.md) | The followers to be removed as collaborators |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoal200Response**](GetGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully removed users as collaborators. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updategoal"></a>
# **UpdateGoal**
> GetGoal200Response UpdateGoal (string goalGid, UpdateGoalRequest updateGoalRequest, bool optPretty = null, List<string> optFields = null)

Update a goal

An existing goal can be updated by making a PUT request on the URL for that goal. Only the fields provided in the `data` block will be updated; any unspecified fields will remain unchanged.  Returns the complete updated goal record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **updateGoalRequest** | [**UpdateGoalRequest**](UpdateGoalRequest.md) | The updated fields for the goal. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoal200Response**](GetGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the goal. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updategoalmetric"></a>
# **UpdateGoalMetric**
> GetGoal200Response UpdateGoalMetric (string goalGid, UpdateGoalMetricRequest updateGoalMetricRequest, bool optPretty = null, List<string> optFields = null)

Update a goal metric

Updates a goal's existing metric's `current_number_value` if one exists, otherwise responds with a 400 status code.  Returns the complete updated goal metric record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goalGid** | **string** | Globally unique identifier for the goal. |  |
| **updateGoalMetricRequest** | [**UpdateGoalMetricRequest**](UpdateGoalMetricRequest.md) | The updated fields for the goal metric. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetGoal200Response**](GetGoal200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the goal metric. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

