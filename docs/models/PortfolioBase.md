# AsanaApiClient.Model.PortfolioBase

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Name** | **string** | The name of the portfolio. | [optional] 
**Archived** | **bool** | [Opt In](/docs/inputoutput-options). True if the portfolio is archived, false if not. Archived portfolios do not show in the UI by default and may be treated differently for queries. | [optional] 
**Color** | **string** | Color of the portfolio. | [optional] 
**StartOn** | **DateOnly** | The day on which work for this portfolio begins, or null if the portfolio has no start date. This takes a date with &#x60;YYYY-MM-DD&#x60; format. *Note: &#x60;due_on&#x60; must be present in the request when setting or unsetting the &#x60;start_on&#x60; parameter. Additionally, &#x60;start_on&#x60; and &#x60;due_on&#x60; cannot be the same date.* | [optional] 
**DueOn** | **DateOnly** | The day on which this portfolio is due. This takes a date with format YYYY-MM-DD. | [optional] 
**DefaultAccessLevel** | **string** | The default access level when inviting new members to the portfolio | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

