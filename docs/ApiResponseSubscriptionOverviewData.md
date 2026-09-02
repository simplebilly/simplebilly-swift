# ApiResponseSubscriptionOverviewData

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currentPeriodEnd** | **Date** |  | [optional] 
**features** | [**PlanFeatures**](PlanFeatures.md) |  | 
**isTrialing** | **Bool** |  | 
**limits** | [**PlanLimits**](PlanLimits.md) |  | 
**manageUrl** | **String** |  | [optional] 
**plan** | **String** | Resolved plan id (free/starter/business/enterprise, or a custom override id). | 
**planName** | **String** |  | 
**priceEur** | **Double** | Monthly price in EUR; &#x60;-1.0&#x60; &#x3D; custom pricing (enterprise). | 
**quantity** | **Int** |  | [optional] 
**status** | **String** |  | [optional] 
**subscriptionId** | **String** |  | [optional] 
**trialEndsAt** | **Date** |  | [optional] 
**usage** | [**UsageSnapshot**](UsageSnapshot.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


