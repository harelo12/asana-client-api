# AsanaApiClient.Api.TimeTrackingEntriesApi

All URIs are relative to *https://app.asana.com/api/1.0*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTimeTrackingEntry**](TimeTrackingEntriesApi.md#createtimetrackingentry) | **POST** /tasks/{task_gid}/time_tracking_entries | Create a time tracking entry |
| [**DeleteTimeTrackingEntry**](TimeTrackingEntriesApi.md#deletetimetrackingentry) | **DELETE** /time_tracking_entries/{time_tracking_entry_gid} | Delete a time tracking entry |
| [**GetTimeTrackingEntries**](TimeTrackingEntriesApi.md#gettimetrackingentries) | **GET** /time_tracking_entries | Get multiple time tracking entries |
| [**GetTimeTrackingEntriesForTask**](TimeTrackingEntriesApi.md#gettimetrackingentriesfortask) | **GET** /tasks/{task_gid}/time_tracking_entries | Get time tracking entries for a task |
| [**GetTimeTrackingEntry**](TimeTrackingEntriesApi.md#gettimetrackingentry) | **GET** /time_tracking_entries/{time_tracking_entry_gid} | Get a time tracking entry |
| [**UpdateTimeTrackingEntry**](TimeTrackingEntriesApi.md#updatetimetrackingentry) | **PUT** /time_tracking_entries/{time_tracking_entry_gid} | Update a time tracking entry |

<a id="createtimetrackingentry"></a>
# **CreateTimeTrackingEntry**
> CreateTimeTrackingEntry201Response CreateTimeTrackingEntry (string taskGid, CreateTimeTrackingEntryRequest createTimeTrackingEntryRequest, bool optPretty = null, List<string> optFields = null)

Create a time tracking entry

Creates a time tracking entry on a given task.  Returns the record of the newly created time tracking entry.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **createTimeTrackingEntryRequest** | [**CreateTimeTrackingEntryRequest**](CreateTimeTrackingEntryRequest.md) | Information about the time tracking entry. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTimeTrackingEntry201Response**](CreateTimeTrackingEntry201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successfully created a time tracking entry for the task. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletetimetrackingentry"></a>
# **DeleteTimeTrackingEntry**
> ApproveAccessRequest200Response DeleteTimeTrackingEntry (string timeTrackingEntryGid, bool optPretty = null)

Delete a time tracking entry

A specific, existing time tracking entry can be deleted by making a `DELETE` request on the URL for that time tracking entry.  Returns an empty data record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **timeTrackingEntryGid** | **string** | Globally unique identifier for the time tracking entry. |  |
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
| **200** | Successfully deleted the specified time tracking entry. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettimetrackingentries"></a>
# **GetTimeTrackingEntries**
> GetTimeTrackingEntriesForTask200Response GetTimeTrackingEntries (bool optPretty = null, string task = null, string attributableTo = null, string portfolio = null, string user = null, string workspace = null, DateOnly enteredOnStartDate = null, DateOnly enteredOnEndDate = null, string timesheetApprovalStatus = null, int limit = null, string offset = null, List<string> optFields = null)

Get multiple time tracking entries

<b>Required scope: </b><code>time_tracking_entries:read</code>  Returns a list of time tracking entries filtered to a task, attributed project, portfolio or user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **task** | **string** | Globally unique identifier for the task to filter time tracking entries by. | [optional]  |
| **attributableTo** | **string** | Globally unique identifier for the project the time tracking entries are attributed to. | [optional]  |
| **portfolio** | **string** | Globally unique identifier for the portfolio to filter time tracking entries by. | [optional]  |
| **user** | **string** | Globally unique identifier for the user to filter time tracking entries by. | [optional]  |
| **workspace** | **string** | Globally unique identifier for the workspace. At least one of &#x60;entered_on_start_date&#x60; or &#x60;entered_on_end_date&#x60; must be provided when filtering by workspace. | [optional]  |
| **enteredOnStartDate** | **DateOnly** | The start date for filtering time tracking entries by when they were entered. | [optional]  |
| **enteredOnEndDate** | **DateOnly** | The end date for filtering time tracking entries by when they were entered. | [optional]  |
| **timesheetApprovalStatus** | **string** | Globally unique identifier for the timesheet approval status to filter time tracking entries by. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTimeTrackingEntriesForTask200Response**](GetTimeTrackingEntriesForTask200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested time tracking entries. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **402** | The request was valid, but the queried object or object mutation specified in the request is above your current premium level. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettimetrackingentriesfortask"></a>
# **GetTimeTrackingEntriesForTask**
> GetTimeTrackingEntriesForTask200Response GetTimeTrackingEntriesForTask (string taskGid, bool optPretty = null, int limit = null, string offset = null, List<string> optFields = null)

Get time tracking entries for a task

<b>Required scope: </b><code>time_tracking_entries:read</code>  Returns time tracking entries for a given task.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taskGid** | **string** | The task to operate on. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **limit** | **int** | Results per page. The number of objects to return per page. The value must be between 1 and 100. | [optional]  |
| **offset** | **string** | Offset token. An offset to the next page returned by the API. A pagination request will return an offset token, which can be used as an input parameter to the next request. If an offset is not passed in, the API will return the first page of results. *Note: You can only pass in an offset that was returned to you via a previously paginated request.* | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**GetTimeTrackingEntriesForTask200Response**](GetTimeTrackingEntriesForTask200Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested time tracking entries. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettimetrackingentry"></a>
# **GetTimeTrackingEntry**
> CreateTimeTrackingEntry201Response GetTimeTrackingEntry (string timeTrackingEntryGid, bool optPretty = null, List<string> optFields = null)

Get a time tracking entry

<b>Required scope: </b><code>time_tracking_entries:read</code>  Returns the complete time tracking entry record for a single time tracking entry.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **timeTrackingEntryGid** | **string** | Globally unique identifier for the time tracking entry. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTimeTrackingEntry201Response**](CreateTimeTrackingEntry201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved the requested time tracking entry. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatetimetrackingentry"></a>
# **UpdateTimeTrackingEntry**
> CreateTimeTrackingEntry201Response UpdateTimeTrackingEntry (string timeTrackingEntryGid, UpdateTimeTrackingEntryRequest updateTimeTrackingEntryRequest, bool optPretty = null, List<string> optFields = null)

Update a time tracking entry

A specific, existing time tracking entry can be updated by making a `PUT` request on the URL for that time tracking entry. Only the fields provided in the `data` block will be updated; any unspecified fields will remain unchanged.  When using this method, it is best to specify only those fields you wish to change, or else you may overwrite changes made by another user since you last retrieved the task.  Returns the complete updated time tracking entry record.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **timeTrackingEntryGid** | **string** | Globally unique identifier for the time tracking entry. |  |
| **updateTimeTrackingEntryRequest** | [**UpdateTimeTrackingEntryRequest**](UpdateTimeTrackingEntryRequest.md) | The updated fields for the time tracking entry. |  |
| **optPretty** | **bool** | Provides “pretty” output. Provides the response in a “pretty” format. In the case of JSON this means doing proper line breaking and indentation to make it readable. This will take extra time and increase the response size so it is advisable only to use this during debugging. | [optional]  |
| **optFields** | [**List&lt;string&gt;**](string.md) | This endpoint returns a resource which excludes some properties by default. To include those optional properties, set this query parameter to a comma-separated list of the properties you wish to include. | [optional]  |

### Return type

[**CreateTimeTrackingEntry201Response**](CreateTimeTrackingEntry201Response.md)

### Authorization

[personalAccessToken](../README.md#personalAccessToken), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated the time tracking entry. |  -  |
| **400** | This usually occurs because of a missing or malformed parameter. Check the documentation and the syntax of your request and try again. |  -  |
| **401** | A valid authentication token was not provided with the request, so the API could not associate a user with the request. |  -  |
| **403** | The authentication and request syntax was valid but the server is refusing to complete the request. This can happen if you try to read or write to objects or properties that the user does not have access to. |  -  |
| **404** | Either the request method and path supplied do not specify a known action in the API, or the object specified by the request does not exist. |  -  |
| **500** | There was a problem on Asana’s end. In the event of a server error the response body should contain an error phrase. These phrases can be used by Asana support to quickly look up the incident that caused the server error. Some errors are due to server load, and will not supply an error phrase. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

