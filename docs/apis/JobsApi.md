# AsanaApiClient.Api.JobsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetJob**](JobsApi.md#getjob) | **GET** /jobs/{job_gid} | Get a job by id |

<a id="getjob"></a>
# **GetJob**
> GetJob200Response GetJob (string jobGid, bool optPretty = null, List<string> optFields = null)

Get a job by id

<b>Required scope: </b><code>jobs:read</code>  <table>   <tr>     <th>Field</th>     <th>Required Scope</th>   </tr>   <tr>     <td><code>new_task_template</code></td>     <td><code>task_templates:read</code></td>   </tr>   <tr>     <td><code>new_portfolio</code></td>     <td><code>portfolios:read</code></td>   </tr>   <tr>     <td><code>new_project</code></td>     <td><code>projects:read</code></td>   </tr>   <tr>     <td><code>new_task</code></td>     <td><code>tasks:read</code></td>   </tr>   <tr>     <td><code>new_project_template</code></td>     <td><code>project_templates:read</code></td>   </tr> </table>  Returns the full record for a job.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **jobGid** | **string** | Globally unique identifier for the job. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetJob200Response**](GetJob200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved Job. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

