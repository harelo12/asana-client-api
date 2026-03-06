# AsanaApiClient.Model.BudgetEstimateRequest
Defines how the estimate portion of a budget is configured. This object controls whether the estimate is enabled, what data source it uses, and which tasks (by billable status) are included in calculating the estimate value. When disabled (enabled: false and source: none), the estimate is hidden and the API response will return `value: null` and `units: null` for this field.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillableStatusFilter** | **string** | Billable status filter applied to the estimate when &#x60;source&#x60; is &#x60;tasks&#x60;. Ignored when &#x60;source&#x60; is &#x60;capacity_plans&#x60; or &#x60;none&#x60;. When not provided, defaults to &#x60;billable&#x60;. | [optional] 
**Source** | **string** | The data source for the estimate. &#x60;tasks&#x60;: use task-level estimated time attributed to the parent. &#x60;capacity_plans&#x60;: use capacity plan estimates attributed to the parent. &#x60;none&#x60;: disables the estimate; only valid when &#x60;enabled&#x60; is &#x60;false&#x60;. When &#x60;enabled&#x60; is &#x60;true&#x60;, &#x60;source&#x60; must not be &#x60;none&#x60;. | [optional] 
**Enabled** | **bool** | Controls whether the estimate is displayed in the budget. This flag primarily affects UI presentation and the response payload. When &#x60;false&#x60; (and &#x60;source&#x60; is &#x60;none&#x60;), the estimate is hidden and the API response will return &#x60;value: null&#x60; and &#x60;units: null&#x60; for this field. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

