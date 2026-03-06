# AsanaApiClient.Api.AttachmentsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAttachmentForObject**](AttachmentsApi.md#createattachmentforobject) | **POST** /attachments | Upload an attachment |
| [**DeleteAttachment**](AttachmentsApi.md#deleteattachment) | **DELETE** /attachments/{attachment_gid} | Delete an attachment |
| [**GetAttachment**](AttachmentsApi.md#getattachment) | **GET** /attachments/{attachment_gid} | Get an attachment |
| [**GetAttachmentsForObject**](AttachmentsApi.md#getattachmentsforobject) | **GET** /attachments | Get attachments from an object |

<a id="createattachmentforobject"></a>
# **CreateAttachmentForObject**
> GetAttachment200Response CreateAttachmentForObject (string parent, bool optPretty = null, List<string> optFields = null, string resourceSubtype = null, System.IO.Stream file = null, string url = null, string name = null, bool connectToApp = null)

Upload an attachment

<b>Required scope: </b><code>attachments:write</code>  Upload an attachment.  This method uploads an attachment on an object and returns the compact record for the created attachment object. This is possible by either:  - Providing the URL of the external resource being attached, or - Downloading the file content first and then uploading it as any other attachment. Note that it is not possible to attach files from third party services such as Dropbox, Box, Vimeo & Google Drive via the API  The 100MB size limit on attachments in Asana is enforced on this endpoint.  This endpoint expects a multipart/form-data encoded request containing the full contents of the file to be uploaded.  Requests made should follow the HTTP/1.1 specification that line terminators are of the form `CRLF` or `\\r\\n` outlined [here](http://www.w3.org/Protocols/HTTP/1.1/draft-ietf-http-v11-spec-01#Basic-Rules) in order for the server to reliably and properly handle the request.  For file names that contain non-ASCII characters, the file name should be URL-encoded. For example, a file named `résumé.pdf` should be encoded as `r%C3%A9sum%C3%A9.pdf` and the `filename` parameter in the `Content-Disposition` header should be set to the encoded file name.  Below is an example of a cURL request with the `Content-Disposition` header:  ``` export ASANA_PAT=\"<YOUR_ASANA_PERSONAL_ACCESS_TOKEN>\" export PARENT_ID=\"<PARENT_GID>\" export ENCODED_NAME=\"r%C3%A9sum%C3%A9.pdf\" curl - -location 'https://app.asana.com/api/1.0/attachments' \\   - -header 'Content-Type: multipart/form-data' \\   - -header 'Accept: application/json' \\   - -header \"Authorization: Bearer $ASANA_PAT\" \\   - -form \"parent=$PARENT_ID\" \\   - -form \"file=@/Users/exampleUser/Downloads/résumé.pdf;headers=\\\"Content-Disposition: form-data; name=\"file\"; filename=\"$ENCODED_NAME.pdf\"; filename*=UTF-8''$ENCODED_NAME.pdf\\\"\" ```


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **parent** | **string** | Required identifier of the parent task, project, or project_brief, as a string.  |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |
| **resourceSubtype** | **string** | The type of the attachment. Must be one of the given values. If not specified, a file attachment of type &#x60;asana&#x60; will be assumed. Note that if the value of &#x60;resource_subtype&#x60; is &#x60;external&#x60;, a &#x60;parent&#x60;, &#x60;name&#x60;, and &#x60;url&#x60; must also be provided.  | [optional]  |
| **file** | **System.IO.Stream****System.IO.Stream** | Required for &#x60;asana&#x60; attachments.  | [optional]  |
| **url** | **string** | The URL of the external resource being attached. Required for attachments of type &#x60;external&#x60;.  | [optional]  |
| **name** | **string** | The name of the external resource being attached. Required for attachments of type &#x60;external&#x60;.  | [optional]  |
| **connectToApp** | **bool** | *Optional*. Only relevant for external attachments with a parent task. A boolean indicating whether the current app should be connected with the attachment for the purposes of showing an app components widget. Requires the app to have been added to a project the parent task is in. This property can only be set if an OAuth token is used to authenticate the request.  Criteria for displaying app widget: 1. An OAuth token must be used to authenticate the request 2. The app needs to have its &#x60;widget_metadata_url&#x60; configured in the developer console 3. The task the attachment is being attached to must be in a project with the app installed | [optional]  |

### Return type

[**GetAttachment200Response**](GetAttachment200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully uploaded the attachment to the parent object. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteattachment"></a>
# **DeleteAttachment**
> ApproveAccessRequest200Response DeleteAttachment (string attachmentGid, bool optPretty = null)

Delete an attachment

<b>Required scope: </b><code>attachments:delete</code>  Deletes a specific, existing attachment.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **attachmentGid** | **string** | Globally unique identifier for the attachment. |  |
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
| **200** | Successfully deleted the specified attachment. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getattachment"></a>
# **GetAttachment**
> GetAttachment200Response GetAttachment (string attachmentGid, bool optPretty = null, List<string> optFields = null)

Get an attachment

<b>Required scope: </b><code>attachments:read</code>  Get the full record for a single attachment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **attachmentGid** | **string** | Globally unique identifier for the attachment. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetAttachment200Response**](GetAttachment200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the record for a single attachment. |  -  |
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

<a id="getattachmentsforobject"></a>
# **GetAttachmentsForObject**
> GetAttachmentsForObject200Response GetAttachmentsForObject (string parent, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get attachments from an object

<b>Required scope: </b><code>attachments:read</code>  Returns the compact records for all attachments on the object. There are three possible `parent` values for this request: `project`, `project_brief`, and `task`. For a project, an attachment refers to a file uploaded to the \"Key resources\" section in the project Overview. For a project brief, an attachment refers to inline files in the project brief itself. For a task, an attachment refers to a file directly associated to that task.  Note that within the Asana app, inline images in the task description do not appear in the index of image thumbnails nor as stories in the task. However, requests made to `GET /attachments` for a task will return all of the images in the task, including inline images.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **parent** | **string** | Globally unique identifier for object to fetch statuses from. Must be a GID for a &#x60;project&#x60;, &#x60;project_brief&#x60;, or &#x60;task&#x60;. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetAttachmentsForObject200Response**](GetAttachmentsForObject200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the specified object&#39;s attachments. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

