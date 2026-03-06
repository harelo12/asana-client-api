# AsanaApiClient.Api.ProjectBriefsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateProjectBrief**](ProjectBriefsApi.md#createprojectbrief) | **POST** /projects/{project_gid}/project_briefs | Create a project brief |
| [**DeleteProjectBrief**](ProjectBriefsApi.md#deleteprojectbrief) | **DELETE** /project_briefs/{project_brief_gid} | Delete a project brief |
| [**GetProjectBrief**](ProjectBriefsApi.md#getprojectbrief) | **GET** /project_briefs/{project_brief_gid} | Get a project brief |
| [**UpdateProjectBrief**](ProjectBriefsApi.md#updateprojectbrief) | **PUT** /project_briefs/{project_brief_gid} | Update a project brief |

<a id="createprojectbrief"></a>
# **CreateProjectBrief**
> GetProjectBrief200Response CreateProjectBrief (string projectGid, UpdateProjectBriefRequest updateProjectBriefRequest, bool optPretty = null, List<string> optFields = null)

Create a project brief

Creates a new project brief.  Returns the full record of the newly created project brief.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectGid** | **string** | Globally unique identifier for the project. |  |
| **updateProjectBriefRequest** | [**UpdateProjectBriefRequest**](UpdateProjectBriefRequest.md) | The project brief to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetProjectBrief200Response**](GetProjectBrief200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created a new project brief. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteprojectbrief"></a>
# **DeleteProjectBrief**
> ApproveAccessRequest200Response DeleteProjectBrief (string projectBriefGid, bool optPretty = null)

Delete a project brief

Deletes a specific, existing project brief.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectBriefGid** | **string** | Globally unique identifier for the project brief. |  |
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
| **200** | Successfully deleted the specified project brief. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprojectbrief"></a>
# **GetProjectBrief**
> GetProjectBrief200Response GetProjectBrief (string projectBriefGid, bool optPretty = null, List<string> optFields = null)

Get a project brief

Get the full record for a project brief.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectBriefGid** | **string** | Globally unique identifier for the project brief. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetProjectBrief200Response**](GetProjectBrief200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the record for a project brief. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **424** | You have exceeded one of the enforced rate limits in the API. See the [documentation on rate limiting](https://developers.asana.com/docs/#rate-limits) for more information. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |
| **501** | There is an issue between the load balancers and Asana&#39;s API. |  -  |
| **503** | Either the upstream service is unavailable to the API, or the API has been intentionally shut off. |  -  |
| **504** | This request took too long to complete. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateprojectbrief"></a>
# **UpdateProjectBrief**
> GetProjectBrief200Response UpdateProjectBrief (string projectBriefGid, UpdateProjectBriefRequest updateProjectBriefRequest, bool optPretty = null, List<string> optFields = null)

Update a project brief

An existing project brief can be updated by making a PUT request on the URL for that project brief. Only the fields provided in the `data` block will be updated; any unspecified fields will remain unchanged.  Returns the complete updated project brief record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **projectBriefGid** | **string** | Globally unique identifier for the project brief. |  |
| **updateProjectBriefRequest** | [**UpdateProjectBriefRequest**](UpdateProjectBriefRequest.md) | The updated fields for the project brief. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetProjectBrief200Response**](GetProjectBrief200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the project brief. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

