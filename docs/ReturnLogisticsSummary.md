# ReturnLogisticsSummary

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**byStatus** | **AnyCodable** | Number of return orders per status. | 
**byWarehouse** | [ReturnWarehouseSummary] | Per-warehouse aggregation. | 
**itemsRestocked** | **Int64** | Sum of &#x60;restock: true&#x60; line-item quantities. | 
**itemsScrapped** | **Int64** | Sum of &#x60;restock: false&#x60; line-item quantities (scrapped/disposed). | 
**totalItems** | **Int64** | Sum of all line-item quantities across returns. | 
**totalReturns** | **Int64** | Total number of return orders (excluding soft-deleted). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


