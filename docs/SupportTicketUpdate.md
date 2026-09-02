# SupportTicketUpdate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assignedTo** | **UUID** |  | [optional] 
**channelId** | **UUID** |  | [optional] 
**channelType** | [**SupportChannelType**](SupportChannelType.md) |  | [optional] 
**closedAt** | **Date** |  | [optional] 
**createdAt** | **Date** |  | [optional] 
**customerEmail** | **String** |  | [optional] 
**customerId** | **String** | References the customer entity. | [optional] 
**customerName** | **String** |  | [optional] 
**externalId** | **String** |  | [optional] 
**firstMessageAt** | **Date** |  | [optional] 
**lastMessageAt** | **Date** |  | [optional] 
**leadId** | **UUID** | References the lead entity. | [optional] 
**messageCount** | **Int** |  | [optional] 
**orderRef** | **String** |  | [optional] 
**priority** | [**TicketPriority**](TicketPriority.md) |  | [optional] 
**resolution** | **String** |  | [optional] 
**status** | [**SupportTicketStatus**](SupportTicketStatus.md) |  | [optional] 
**subject** | **String** |  | [optional] 
**tags** | **AnyCodable** |  | [optional] 
**tenantId** | **UUID** |  | [optional] 
**updatedAt** | **Date** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


