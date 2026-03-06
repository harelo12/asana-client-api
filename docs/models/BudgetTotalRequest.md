# AsanaApiClient.Model.BudgetTotalRequest
Defines how the total portion of a budget is configured. The total represents a user-defined target value, not an aggregated one. This object specifies whether the total is displayed and the current value for the selected budget_type.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Indicates whether the total value is active and should be displayed in the budget. This flag primarily affects UI presentation and the response payload. | [optional] 
**Value** | **decimal** | The user-set value for the total budget. When &#x60;budget_type&#x60; is &#x60;time&#x60;, represents minutes. When &#x60;budget_type&#x60; is &#x60;cost&#x60;, represents the monetary amount in the domain&#39;s currency. This value is stored separately for each &#x60;budget_type&#x60;, so switching between types preserves each value. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

