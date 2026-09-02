# WebhookEvent

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **Int** |  | [optional] 
**channel** | **String** | source for inbound, target URL for outbound. | [optional] 
**direction** | [**WebhookDirection**](WebhookDirection.md) | inbound | outbound | 
**eventType** | **String** |  | 
**lastError** | **String** |  | [optional] 
**payload** | **AnyCodable** |  | [optional] 
**status** | [**WebhookEventStatus**](WebhookEventStatus.md) | accepted | delivered | failed | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


