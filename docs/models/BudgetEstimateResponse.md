# AsanaApiClient.Model.BudgetEstimateResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillableStatusFilter** | **string** | Billable status filter applied to the estimate when &#x60;source&#x60; is &#x60;tasks&#x60;. Ignored when &#x60;source&#x60; is &#x60;capacity_plans&#x60; or &#x60;none&#x60;. When not provided, defaults to &#x60;billable&#x60;. | [optional] 
**Source** | **string** | The data source for the estimate. &#x60;tasks&#x60;: use task-level estimated time attributed to the parent. &#x60;capacity_plans&#x60;: use capacity plan estimates attributed to the parent. &#x60;none&#x60;: disables the estimate; only valid when &#x60;enabled&#x60; is &#x60;false&#x60;. When &#x60;enabled&#x60; is &#x60;true&#x60;, &#x60;source&#x60; must not be &#x60;none&#x60;. | [optional] 
**Enabled** | **bool** | Controls whether the estimate is displayed in the budget. This flag primarily affects UI presentation and the response payload. When &#x60;false&#x60; (and &#x60;source&#x60; is &#x60;none&#x60;), the estimate is hidden and the API response will return &#x60;value: null&#x60; and &#x60;units: null&#x60; for this field. | [optional] 
**Units** | **string** | The units of the estimate value. When &#x60;budget_type&#x60; is &#x60;time&#x60;, units are &#x60;\&quot;minutes\&quot;&#x60;. When &#x60;budget_type&#x60; is &#x60;cost&#x60;, units are the ISO 4217 currency code configured at the domain level. When &#x60;source&#x60; is &#x60;none&#x60; and &#x60;enabled&#x60; is &#x60;false&#x60;, this field will be &#x60;null&#x60;. | [optional] [readonly] 
**Value** | **decimal** | The aggregated estimate value for the budget. This value is computed based on the selected &#x60;source&#x60; and, when &#x60;source&#x60; is &#x60;tasks&#x60;, the specified &#x60;billable_status_filter&#x60;. When &#x60;budget_type&#x60; is &#x60;time&#x60;, represents the aggregated estimated minutes on the parent. When &#x60;budget_type&#x60; is &#x60;cost&#x60;, represents the aggregated estimated cost on the parent (estimated time x resource rate). When &#x60;source&#x60; is &#x60;none&#x60; and &#x60;enabled&#x60; is &#x60;false&#x60;, this field will be &#x60;null&#x60;. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

