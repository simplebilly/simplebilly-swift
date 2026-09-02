# ProductionOrderCosting

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**costPerUnit** | **String** | material_cost_total ÷ quantity. | 
**costSource** | **String** | \&quot;actual\&quot; when costed from stock-movement consumption, else \&quot;planned\&quot;. | 
**lines** | [CostingLine] |  | 
**marginPerUnit** | **String** | sale_price − cost_per_unit. | [optional] 
**marginPercent** | **String** | margin_per_unit ÷ cost_per_unit as a percentage. | [optional] 
**materialCostTotal** | **String** | Total material cost for the whole order. | 
**orderNumber** | **String** |  | 
**productionOrderId** | **UUID** |  | 
**quantity** | **Int64** |  | 
**salePrice** | **String** | Finished product&#39;s sale price per unit (used to compute margin). | [optional] 
**status** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


