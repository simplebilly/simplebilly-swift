# StockTransfer

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**lineItems** | **AnyCodable** | JSON array of &#x60;{product_id, name, quantity, batch_number?}&#x60;. | 
**notes** | **String** |  | [optional] 
**sourceWarehouseId** | **String** | References the warehouse entity. | 
**status** | [**StockTransferStatus**](StockTransferStatus.md) | One of: draft | completed | cancelled | 
**targetWarehouseId** | **String** | References the warehouse entity. | 
**transferDate** | **Date** |  | 
**transferNumber** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


