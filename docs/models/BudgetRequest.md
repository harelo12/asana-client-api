# AsanaApiClient.Model.BudgetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**BudgetType** | **string** | The type of the budget, in \&quot;cost\&quot; or \&quot;time\&quot;. The value of this property will dictate how the corresponding values for actual, estimate, and total are interpreted. | [optional] 
**Estimate** | [**BudgetEstimateRequest**](BudgetEstimateRequest.md) |  | [optional] 
**Actual** | [**BudgetActualRequest**](BudgetActualRequest.md) |  | [optional] 
**Total** | [**BudgetTotalRequest**](BudgetTotalRequest.md) |  | [optional] 
**Parent** | **string** | Globally unique ID of the parent object: project. Can only be set on create, immutable thereafter. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

