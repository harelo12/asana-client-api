# AsanaApiClient.Api.ReactionsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetReactionsOnObject**](ReactionsApi.md#getreactionsonobject) | **GET** /reactions | Get reactions with an emoji base on an object. |

<a id="getreactionsonobject"></a>
# **GetReactionsOnObject**
> GetReactionsOnObject200Response GetReactionsOnObject (string target, string emojiBase, bool optPretty = null, int limit = null, string offset = null)

Get reactions with an emoji base on an object.

Returns the reactions with a specified emoji base character on the object.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **target** | **string** | Globally unique identifier for object to fetch reactions from. Must be a GID for a status update or story. |  |
| **emojiBase** | **string** | Only return reactions with this emoji base character. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |

### Return type

[**GetReactionsOnObject200Response**](GetReactionsOnObject200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the specified object&#39;s reactions. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

