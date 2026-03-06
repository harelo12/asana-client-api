# AsanaApiClient.Model.DeprecatedPortfolioMembershipCompact
This object determines if a user is a member of a portfolio.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Portfolio** | [**PortfolioCompact**](PortfolioCompact.md) |  | [optional] 
**User** | [**UserCompact**](UserCompact.md) |  | [optional] 
**AccessLevel** | **string** | Whether the member has admin, editor, or viewer access to the portfolio. Portfolios do not support commenter access yet. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

