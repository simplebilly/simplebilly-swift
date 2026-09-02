# DeliveryDate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customerId** | **String** | References the customer entity. | [optional] 
**fulfilledDate** | **Date** | Date actually delivered (set on fulfillment). | [optional] 
**note** | **String** |  | [optional] 
**orderNumber** | **String** | Sales order number (&#x60;order.order_number&#x60;). | 
**originalDate** | **Date** | Original date promised before rescheduling. | [optional] 
**productId** | **String** | Product line item this date applies to, if per-item. References the product entity. | [optional] 
**promisedDate** | **Date** | Date promised to the customer. | 
**status** | [**DeliveryDateStatus**](DeliveryDateStatus.md) | One of: promised | confirmed | rescheduled | fulfilled | late | cancelled | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


