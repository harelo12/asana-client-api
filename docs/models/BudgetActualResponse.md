# AsanaApiClient.Model.BudgetActualResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillableStatusFilter** | **string** | Billable status filter applied to time tracking entries contributing to the actual value. Determines which entries are included in aggregation. When not provided, defaults to &#x60;billable&#x60;. | [optional] 
**Value** | **decimal** | The aggregated actual value for the budget. * When &#x60;budget_type&#x60; is &#x60;time&#x60;, represents the total actual minutes from time tracking entries. * When &#x60;budget_type&#x60; is &#x60;cost&#x60;, represents the total actual cost, computed as (actual time × resource rate). | [optional] [readonly] 
**Units** | **string** | The units of the actual value. * When &#x60;budget_type&#x60; is &#x60;time&#x60;, units are &#x60;\&quot;minutes\&quot;&#x60;. * When &#x60;budget_type&#x60; is &#x60;cost&#x60;, units are the ISO 4217 currency code configured at the domain level. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

