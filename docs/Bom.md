# Bom

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**components** | **AnyCodable** | JSON array of &#x60;{product_id, name, quantity, unit, scrap_rate}&#x60;. | [optional] 
**description** | **String** |  | [optional] 
**name** | **String** |  | 
**outputQuantity** | **Int64** | Output quantity per production run (defaults to 1). | [optional] 
**productId** | **UUID** | The finished product this BOM produces. References the product entity. | 
**status** | [**BomStatus**](BomStatus.md) | One of: draft | active | archived | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


