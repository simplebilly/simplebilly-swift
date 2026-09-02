# ProductionOrder

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bomId** | **UUID** | References the BOM entity. | [optional] 
**components** | **AnyCodable** | JSON snapshot of the BOM components at creation time. | [optional] 
**endDate** | **Date** |  | [optional] 
**notes** | **String** |  | [optional] 
**orderNumber** | **String** |  | 
**productId** | **UUID** | The finished product to manufacture. References the product entity. | 
**quantity** | **Int64** | Quantity of finished product to produce. | 
**sourceWarehouseId** | **String** | Warehouse components are consumed from. References the warehouse entity. | [optional] 
**startDate** | **Date** |  | [optional] 
**status** | [**ProductionOrderStatus**](ProductionOrderStatus.md) | One of: planned | in_production | completed | cancelled | [optional] 
**targetWarehouseId** | **String** | Warehouse the finished product is added to. References the warehouse entity. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


