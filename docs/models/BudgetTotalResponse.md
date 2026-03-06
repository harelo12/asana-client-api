# AsanaApiClient.Model.BudgetTotalResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Indicates whether the total value is active and should be displayed in the budget. This flag primarily affects UI presentation and the response payload. | [optional] 
**Value** | **decimal** | The user-set value for the total budget. When &#x60;budget_type&#x60; is &#x60;time&#x60;, represents minutes. When &#x60;budget_type&#x60; is &#x60;cost&#x60;, represents the monetary amount in the domain&#39;s currency. This value is stored separately for each &#x60;budget_type&#x60;, so switching between types preserves each value. | [optional] 
**Units** | **string** | The units of the total value. When &#x60;budget_type&#x60; is &#x60;time&#x60;, units are &#x60;\&quot;minutes\&quot;&#x60;. When &#x60;budget_type&#x60; is &#x60;cost&#x60;, units are the ISO 4217 currency code configured at the domain level. When &#x60;enabled&#x60; is &#x60;false&#x60;, this field will be &#x60;null&#x60;. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

