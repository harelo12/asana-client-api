# AsanaApiClient.Model.BudgetActualRequest
Defines the configuration of the actual portion of a budget. The actual value represents aggregated time tracking data attributed to the budget’s parent. This object controls which time entries are included based on their billable status. When no entries match the selected filter, the value will be 0.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillableStatusFilter** | **string** | Billable status filter applied to time tracking entries contributing to the actual value. Determines which entries are included in aggregation. When not provided, defaults to &#x60;billable&#x60;. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

