# AsanaApiClient.Api.CustomFieldsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCustomField**](CustomFieldsApi.md#createcustomfield) | **POST** /custom_fields | Create a custom field |
| [**CreateEnumOptionForCustomField**](CustomFieldsApi.md#createenumoptionforcustomfield) | **POST** /custom_fields/{custom_field_gid}/enum_options | Create an enum option |
| [**DeleteCustomField**](CustomFieldsApi.md#deletecustomfield) | **DELETE** /custom_fields/{custom_field_gid} | Delete a custom field |
| [**GetCustomField**](CustomFieldsApi.md#getcustomfield) | **GET** /custom_fields/{custom_field_gid} | Get a custom field |
| [**GetCustomFieldsForWorkspace**](CustomFieldsApi.md#getcustomfieldsforworkspace) | **GET** /workspaces/{workspace_gid}/custom_fields | Get a workspace&#39;s custom fields |
| [**InsertEnumOptionForCustomField**](CustomFieldsApi.md#insertenumoptionforcustomfield) | **POST** /custom_fields/{custom_field_gid}/enum_options/insert | Reorder a custom field&#39;s enum |
| [**UpdateCustomField**](CustomFieldsApi.md#updatecustomfield) | **PUT** /custom_fields/{custom_field_gid} | Update a custom field |
| [**UpdateEnumOption**](CustomFieldsApi.md#updateenumoption) | **PUT** /enum_options/{enum_option_gid} | Update an enum option |

<a id="createcustomfield"></a>
# **CreateCustomField**
> CreateCustomField201Response CreateCustomField (CreateCustomFieldRequest createCustomFieldRequest, bool optPretty = null, List<string> optFields = null)

Create a custom field

<b>Required scope: </b><code>custom_fields:write</code>  Creates a new custom field in a workspace. Every custom field is required to be created in a specific workspace, and this workspace cannot be changed once set.  A custom field’s name must be unique within a workspace and not conflict with names of existing task properties such as `Due Date` or `Assignee`. A custom field’s type must be one of `text`, `enum`, `multi_enum`, `number`, `date`, or `people`.  Returns the full record of the newly created custom field.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCustomFieldRequest** | [**CreateCustomFieldRequest**](CreateCustomFieldRequest.md) | The custom field object to create. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateCustomField201Response**](CreateCustomField201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Custom field successfully created. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createenumoptionforcustomfield"></a>
# **CreateEnumOptionForCustomField**
> CreateEnumOptionForCustomField201Response CreateEnumOptionForCustomField (string customFieldGid, bool optPretty = null, List<string> optFields = null, CreateEnumOptionForCustomFieldRequest createEnumOptionForCustomFieldRequest = null)

Create an enum option

<b>Required scope: </b><code>custom_fields:write</code>  Creates an enum option and adds it to this custom field’s list of enum options. A custom field can have at most 500 enum options (including disabled options). By default new enum options are inserted at the end of a custom field’s list. Locked custom fields can only have enum options added by the user who locked the field. Returns the full record of the newly created enum option.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customFieldGid** | **string** | Globally unique identifier for the custom field. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |
| **createEnumOptionForCustomFieldRequest** | [**CreateEnumOptionForCustomFieldRequest**](CreateEnumOptionForCustomFieldRequest.md) | The enum option object to create. | [optional]  |

### Return type

[**CreateEnumOptionForCustomField201Response**](CreateEnumOptionForCustomField201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Custom field enum option successfully created. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletecustomfield"></a>
# **DeleteCustomField**
> ApproveAccessRequest200Response DeleteCustomField (string customFieldGid, bool optPretty = null)

Delete a custom field

A specific, existing custom field can be deleted by making a DELETE request on the URL for that custom field. Locked custom fields can only be deleted by the user who locked the field. Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customFieldGid** | **string** | Globally unique identifier for the custom field. |  |
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
| **200** | The custom field was successfully deleted. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcustomfield"></a>
# **GetCustomField**
> CreateCustomField201Response GetCustomField (string customFieldGid, bool optPretty = null, List<string> optFields = null)

Get a custom field

<b>Required scope: </b><code>custom_fields:read</code>  Get the complete definition of a custom field’s metadata.  Since custom fields can be defined for one of a number of types, and these types have different data and behaviors, there are fields that are relevant to a particular type. For instance, as noted above, enum_options is only relevant for the enum type and defines the set of choices that the enum could represent. The examples below show some of these type-specific custom field definitions.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customFieldGid** | **string** | Globally unique identifier for the custom field. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateCustomField201Response**](CreateCustomField201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the complete definition of a custom field’s metadata. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcustomfieldsforworkspace"></a>
# **GetCustomFieldsForWorkspace**
> GetCustomFieldsForWorkspace200Response GetCustomFieldsForWorkspace (string workspaceGid, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get a workspace's custom fields

<b>Required scope: </b><code>custom_fields:read</code>  Returns a list of the compact representation of all of the custom fields in a workspace.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceGid** | **string** | Globally unique identifier for the workspace or organization. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetCustomFieldsForWorkspace200Response**](GetCustomFieldsForWorkspace200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved all custom fields for the given workspace. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insertenumoptionforcustomfield"></a>
# **InsertEnumOptionForCustomField**
> CreateEnumOptionForCustomField201Response InsertEnumOptionForCustomField (string customFieldGid, bool optPretty = null, List<string> optFields = null, InsertEnumOptionForCustomFieldRequest insertEnumOptionForCustomFieldRequest = null)

Reorder a custom field's enum

<b>Required scope: </b><code>custom_fields:write</code>  Moves a particular enum option to be either before or after another specified enum option in the custom field. Locked custom fields can only be reordered by the user who locked the field.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customFieldGid** | **string** | Globally unique identifier for the custom field. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |
| **insertEnumOptionForCustomFieldRequest** | [**InsertEnumOptionForCustomFieldRequest**](InsertEnumOptionForCustomFieldRequest.md) | The enum option object to create. | [optional]  |

### Return type

[**CreateEnumOptionForCustomField201Response**](CreateEnumOptionForCustomField201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom field enum option successfully reordered. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatecustomfield"></a>
# **UpdateCustomField**
> CreateCustomField201Response UpdateCustomField (string customFieldGid, bool optPretty = null, List<string> optFields = null, UpdateCustomFieldRequest updateCustomFieldRequest = null)

Update a custom field

<b>Required scope: </b><code>custom_fields:write</code>  A specific, existing custom field can be updated by making a PUT request on the URL for that custom field. Only the fields provided in the `data` block will be updated; any unspecified fields will remain unchanged When using this method, it is best to specify only those fields you wish to change, or else you may overwrite changes made by another user since you last retrieved the custom field. A custom field’s `type` cannot be updated. An enum custom field’s `enum_options` cannot be updated with this endpoint. Instead see “Work With Enum Options” for information on how to update `enum_options`. Locked custom fields can only be updated by the user who locked the field. Returns the complete updated custom field record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customFieldGid** | **string** | Globally unique identifier for the custom field. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |
| **updateCustomFieldRequest** | [**UpdateCustomFieldRequest**](UpdateCustomFieldRequest.md) | The custom field object with all updated properties. | [optional]  |

### Return type

[**CreateCustomField201Response**](CreateCustomField201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The custom field was successfully updated. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateenumoption"></a>
# **UpdateEnumOption**
> CreateEnumOptionForCustomField201Response UpdateEnumOption (string enumOptionGid, bool optPretty = null, List<string> optFields = null, UpdateEnumOptionRequest updateEnumOptionRequest = null)

Update an enum option

<b>Required scope: </b><code>custom_fields:write</code>  Updates an existing enum option. Enum custom fields require at least one enabled enum option. Locked custom fields can only be updated by the user who locked the field. Returns the full record of the updated enum option.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **enumOptionGid** | **string** | Globally unique identifier for the enum option. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |
| **updateEnumOptionRequest** | [**UpdateEnumOptionRequest**](UpdateEnumOptionRequest.md) | The enum option object to update | [optional]  |

### Return type

[**CreateEnumOptionForCustomField201Response**](CreateEnumOptionForCustomField201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the specified custom field enum. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

