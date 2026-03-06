# AsanaApiClient.Api.AccessRequestsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ApproveAccessRequest**](AccessRequestsApi.md#approveaccessrequest) | **POST** /access_requests/{access_request_gid}/approve | Approve an access request |
| [**CreateAccessRequest**](AccessRequestsApi.md#createaccessrequest) | **POST** /access_requests | Create an access request |
| [**GetAccessRequests**](AccessRequestsApi.md#getaccessrequests) | **GET** /access_requests | Get access requests |
| [**RejectAccessRequest**](AccessRequestsApi.md#rejectaccessrequest) | **POST** /access_requests/{access_request_gid}/reject | Reject an access request |

<a id="approveaccessrequest"></a>
# **ApproveAccessRequest**
> ApproveAccessRequest200Response ApproveAccessRequest (string accessRequestGid)

Approve an access request

Approves an access request for a target object.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accessRequestGid** | **string** | Globally unique identifier for the access request. |  |

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
| **200** | Successfully approved an access request. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createaccessrequest"></a>
# **CreateAccessRequest**
> CreateAccessRequest201Response CreateAccessRequest (CreateAccessRequestRequest createAccessRequestRequest)

Create an access request

Submits a new access request for a private object. Currently supports projects and portfolios.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAccessRequestRequest** | [**CreateAccessRequestRequest**](CreateAccessRequestRequest.md) |  |  |

### Return type

[**CreateAccessRequest201Response**](CreateAccessRequest201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created a new access request. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getaccessrequests"></a>
# **GetAccessRequests**
> GetAccessRequests200Response GetAccessRequests (string target, string user = null, bool optPretty = null, List<string> optFields = null)

Get access requests

Returns the pending access requests for a target object or a target object filtered by user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **target** | **string** | Globally unique identifier for the target object. |  |
| **user** | **string** | A string identifying a user. This can either be the string \&quot;me\&quot;, an email, or the gid of a user. | [optional]  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetAccessRequests200Response**](GetAccessRequests200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved access requests. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="rejectaccessrequest"></a>
# **RejectAccessRequest**
> ApproveAccessRequest200Response RejectAccessRequest (string accessRequestGid)

Reject an access request

Rejects an access request for a target object.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accessRequestGid** | **string** | Globally unique identifier for the access request. |  |

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
| **200** | Successfully rejected an access request. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

