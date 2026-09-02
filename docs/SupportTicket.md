# SupportTicket

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assignedTo** | **UUID** |  | [optional] 
**channelId** | **UUID** |  | [optional] 
**channelType** | [**SupportChannelType**](SupportChannelType.md) |  | [optional] 
**closedAt** | **Date** |  | [optional] 
**createdAt** | **Date** |  | 
**customerEmail** | **String** |  | [optional] 
**customerId** | **String** | References the customer entity. | [optional] 
**customerName** | **String** |  | [optional] 
**externalId** | **String** |  | [optional] 
**firstMessageAt** | **Date** |  | 
**lastMessageAt** | **Date** |  | 
**leadId** | **UUID** | References the lead entity. | [optional] 
**messageCount** | **Int** |  | 
**orderRef** | **String** |  | [optional] 
**priority** | [**TicketPriority**](TicketPriority.md) |  | 
**resolution** | **String** |  | [optional] 
**status** | [**SupportTicketStatus**](SupportTicketStatus.md) |  | 
**subject** | **String** |  | 
**tags** | **AnyCodable** |  | 
**tenantId** | **UUID** |  | 
**updatedAt** | **Date** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


