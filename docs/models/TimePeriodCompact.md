# AsanaApiClient.Model.TimePeriodCompact
<p><strong style={{ color: \"#4573D2\" }}>Full object requires scope: </strong><code>time_periods:read</code></p>  A generic Asana Resource, containing a globally unique identifier.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**EndOn** | **string** | The localized end date of the time period in &#x60;YYYY-MM-DD&#x60; format. | [optional] 
**StartOn** | **string** | The localized start date of the time period in &#x60;YYYY-MM-DD&#x60; format. | [optional] 
**Period** | **string** | The cadence and index of the time period. | [optional] 
**DisplayName** | **string** | A string representing the cadence code and the fiscal year. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

