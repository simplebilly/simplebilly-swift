# StockMovement

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delta** | **Int64** | Signed movement: positive &#x3D; into stock, negative &#x3D; out of stock. | 
**movementType** | [**MovementType**](MovementType.md) | One of the &#x60;MOVEMENT_*&#x60; constants. | 
**productId** | **UUID** | References the product entity. | 
**quantity** | **Int64** | Absolute quantity moved (always &gt;&#x3D; 0). | 
**reason** | **String** |  | [optional] 
**referenceId** | **String** | Primary-key of the referencing entity. | [optional] 
**referenceType** | [**ReferenceType**](ReferenceType.md) | Entity that caused the movement, e.g. &#x60;goods_receipt&#x60;, &#x60;stock_transfer&#x60;. | [optional] 
**warehouseId** | **String** | References the warehouse entity. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


