# AsanaApiClient.Model.BudgetResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**BudgetType** | **string** | The type of the budget, in \&quot;cost\&quot; or \&quot;time\&quot;. The value of this property will dictate how the corresponding values for actual, estimate, and total are interpreted. | [optional] 
**Estimate** | [**BudgetEstimateResponse**](BudgetEstimateResponse.md) |  | [optional] 
**Actual** | [**BudgetActualResponse**](BudgetActualResponse.md) |  | [optional] 
**Total** | [**BudgetTotalResponse**](BudgetTotalResponse.md) |  | [optional] 
**Parent** | [**BudgetResponseAllOfParent**](BudgetResponseAllOfParent.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

