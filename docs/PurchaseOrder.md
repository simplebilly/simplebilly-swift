# PurchaseOrder

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **String** |  | [optional] 
**deliveryAddress** | **AnyCodable** |  | [optional] 
**expectedDeliveryDate** | **Date** |  | [optional] 
**lineItems** | **AnyCodable** | JSON array of &#x60;{product_id, name, quantity, unit_price_net, tax_rate, delivery_date}&#x60;. | [optional] 
**notes** | **String** |  | [optional] 
**orderDate** | **Date** |  | 
**poNumber** | **String** |  | 
**status** | [**PurchaseOrderStatus**](PurchaseOrderStatus.md) | One of: draft | ordered | partially_received | received | cancelled | 
**supplierContactId** | **String** | References the supplier entity. | [optional] 
**supplierName** | **String** |  | [optional] 
**totalGrossAmount** | **String** |  | [optional] 
**totalNetAmount** | **String** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


