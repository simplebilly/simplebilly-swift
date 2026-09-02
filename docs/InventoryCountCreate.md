# InventoryCountCreate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countDate** | **Date** |  | 
**countNumber** | **String** |  | 
**lineItems** | **AnyCodable** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. | 
**notes** | **String** |  | [optional] 
**status** | [**InventoryCountStatus**](InventoryCountStatus.md) | One of: draft | counting | reviewed | posted | 
**warehouseId** | **String** | References the warehouse entity. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


