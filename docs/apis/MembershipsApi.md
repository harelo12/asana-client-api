# AsanaApiClient.Api.MembershipsApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateMembership**](MembershipsApi.md#createmembership) | **POST** /memberships | Create a membership |
| [**DeleteMembership**](MembershipsApi.md#deletemembership) | **DELETE** /memberships/{membership_gid} | Delete a membership |
| [**GetMembership**](MembershipsApi.md#getmembership) | **GET** /memberships/{membership_gid} | Get a membership |
| [**GetMemberships**](MembershipsApi.md#getmemberships) | **GET** /memberships | Get multiple memberships |
| [**UpdateMembership**](MembershipsApi.md#updatemembership) | **PUT** /memberships/{membership_gid} | Update a membership |

<a id="createmembership"></a>
# **CreateMembership**
> CreateMembership201Response CreateMembership (bool optPretty = null, CreateMembershipRequest createMembershipRequest = null)

Create a membership

Creates a new membership in a `goal`, `project`, `portfolio`, `custom_type`, or `custom_field`, where members can be Teams or Users.  Returns the full record of the newly created membership.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **createMembershipRequest** | [**CreateMembershipRequest**](CreateMembershipRequest.md) | The updated fields for the membership. | [optional]  |

### Return type

[**CreateMembership201Response**](CreateMembership201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created the requested membership. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletemembership"></a>
# **DeleteMembership**
> ApproveAccessRequest200Response DeleteMembership (string membershipGid, bool optPretty = null)

Delete a membership

A specific, existing membership for a `goal`, `project`, `portfolio`, `custom_type`, or `custom_field` can be deleted by making a `DELETE` request on the URL for that membership.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **membershipGid** | **string** | Globally unique identifier for the membership. |  |
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
| **200** | Successfully deleted the requested membership. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getmembership"></a>
# **GetMembership**
> CreateMembership201Response GetMembership (string membershipGid, bool optPretty = null)

Get a membership

Returns a `project_membership`, `goal_membership`, `portfolio_membership`, `custom_type_membership`, or `custom_field_membership` record for a membership id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **membershipGid** | **string** | Globally unique identifier for the membership. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**CreateMembership201Response**](CreateMembership201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the record for a single membership. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getmemberships"></a>
# **GetMemberships**
> GetMemberships200Response GetMemberships (bool optPretty = null, string parent = null, string member = null, string resourceSubtype = null, int limit = null, string offset = null, List<string> optFields = null)

Get multiple memberships

Returns compact `goal_membership`, `project_membership`, `portfolio_membership`, `custom_type_membership`, or `custom_field_membership` records. The possible types for `parent` in this request are `goal`, `project`, `portfolio`, `custom_type`, or `custom_field`. An additional member (user GID or team GID) can be passed in to filter to a specific membership.  Alternatively, when `parent` is absent, you can use the `member` and `resource_subtype` parameters together to fetch all memberships of a specific type for a given member. For example, passing `member` as a team GID and `resource_subtype` as `project_membership` will return all project memberships for that team.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **parent** | **string** | Globally unique identifier for &#x60;goal&#x60;, &#x60;project&#x60;, &#x60;portfolio&#x60;, &#x60;custom_type&#x60;, or &#x60;custom_field&#x60;. This parameter is optional when &#x60;resource_subtype&#x60; is provided along with &#x60;member&#x60;. | [optional]  |
| **member** | **string** | Globally unique identifier for &#x60;team&#x60; or &#x60;user&#x60;. When used with &#x60;resource_subtype&#x60; and without &#x60;parent&#x60;, returns all memberships of the specified subtype for this member. | [optional]  |
| **resourceSubtype** | **string** | The type of membership to return. Required when &#x60;parent&#x60; is absent. Currently supported value is &#x60;project_membership&#x60; (when &#x60;member&#x60; is a team GID, returns all project memberships for that team). | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetMemberships200Response**](GetMemberships200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested membership. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatemembership"></a>
# **UpdateMembership**
> CreateMembership201Response UpdateMembership (string membershipGid, UpdateMembershipRequest updateMembershipRequest, bool optPretty = null)

Update a membership

An existing membership can be updated by making a `PUT` request on the membership. Only the fields provided in the `data` block will be updated; any unspecified fields will remain unchanged. Memberships on `goals`, `projects`, `portfolios`, `custom_types`, and `custom_fields` can be updated.  Returns the full record of the updated membership.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **membershipGid** | **string** | Globally unique identifier for the membership. |  |
| **updateMembershipRequest** | [**UpdateMembershipRequest**](UpdateMembershipRequest.md) | The membership to update. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |

### Return type

[**CreateMembership201Response**](CreateMembership201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the requested membership. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

