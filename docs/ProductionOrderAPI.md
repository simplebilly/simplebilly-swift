# ProductionOrderAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createProductionOrder**](ProductionOrderAPI.md#createproductionorder) | **POST** /api/v1/production-orders | 
[**deleteProductionOrder**](ProductionOrderAPI.md#deleteproductionorder) | **DELETE** /api/v1/production-orders/{production_order_id} | 
[**getProductionOrder**](ProductionOrderAPI.md#getproductionorder) | **GET** /api/v1/production-orders/{production_order_id} | 
[**listProductionOrders**](ProductionOrderAPI.md#listproductionorders) | **GET** /api/v1/production-orders/ | 
[**productionOrderCosting**](ProductionOrderAPI.md#productionordercosting) | **GET** /api/v1/production-orders/{production_order_id}/costing | Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product&#39;s sale price.
[**updateProductionOrder**](ProductionOrderAPI.md#updateproductionorder) | **PUT** /api/v1/production-orders/{production_order_id} | 
[**updateProductionOrderStatus**](ProductionOrderAPI.md#updateproductionorderstatus) | **PUT** /api/v1/production-orders/{production_order_id}/status | 


# **createProductionOrder**
```swift
    open class func createProductionOrder(productionOrder: ProductionOrder, completion: @escaping (_ data: ProductionOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productionOrder = ProductionOrder(bomId: 123, components: 123, endDate: Date(), notes: "notes_example", orderNumber: "orderNumber_example", productId: 123, quantity: 123, sourceWarehouseId: "sourceWarehouseId_example", startDate: Date(), status: ProductionOrderStatus(), targetWarehouseId: "targetWarehouseId_example") // ProductionOrder | 

ProductionOrderAPI.createProductionOrder(productionOrder: productionOrder) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productionOrder** | [**ProductionOrder**](ProductionOrder.md) |  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProductionOrder**
```swift
    open class func deleteProductionOrder(productionOrderId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productionOrderId = 987 // UUID | 

ProductionOrderAPI.deleteProductionOrder(productionOrderId: productionOrderId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productionOrderId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProductionOrder**
```swift
    open class func getProductionOrder(productionOrderId: UUID, completion: @escaping (_ data: ProductionOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productionOrderId = 987 // UUID | 

ProductionOrderAPI.getProductionOrder(productionOrderId: productionOrderId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productionOrderId** | **UUID** |  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProductionOrders**
```swift
    open class func listProductionOrders(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, status: String? = nil, completion: @escaping (_ data: [ProductionOrder]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let status = "status_example" // String | Filter by status. (optional)

ProductionOrderAPI.listProductionOrders(page: page, pageSize: pageSize, search: search, status: status) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 
 **search** | **String** |  | [optional] 
 **status** | **String** | Filter by status. | [optional] 

### Return type

[**[ProductionOrder]**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **productionOrderCosting**
```swift
    open class func productionOrderCosting(productionOrderId: UUID, completion: @escaping (_ data: ProductionOrderCosting?, _ error: Error?) -> Void)
```

Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productionOrderId = 987 // UUID | 

// Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.
ProductionOrderAPI.productionOrderCosting(productionOrderId: productionOrderId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productionOrderId** | **UUID** |  | 

### Return type

[**ProductionOrderCosting**](ProductionOrderCosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProductionOrder**
```swift
    open class func updateProductionOrder(productionOrderId: UUID, productionOrder: ProductionOrder, completion: @escaping (_ data: ProductionOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productionOrderId = 987 // UUID | 
let productionOrder = ProductionOrder(bomId: 123, components: 123, endDate: Date(), notes: "notes_example", orderNumber: "orderNumber_example", productId: 123, quantity: 123, sourceWarehouseId: "sourceWarehouseId_example", startDate: Date(), status: ProductionOrderStatus(), targetWarehouseId: "targetWarehouseId_example") // ProductionOrder | 

ProductionOrderAPI.updateProductionOrder(productionOrderId: productionOrderId, productionOrder: productionOrder) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productionOrderId** | **UUID** |  | 
 **productionOrder** | [**ProductionOrder**](ProductionOrder.md) |  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProductionOrderStatus**
```swift
    open class func updateProductionOrderStatus(productionOrderId: UUID, productionOrderStatusUpdate: ProductionOrderStatusUpdate, completion: @escaping (_ data: ProductionOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productionOrderId = 987 // UUID | 
let productionOrderStatusUpdate = ProductionOrderStatusUpdate(status: "status_example") // ProductionOrderStatusUpdate | 

ProductionOrderAPI.updateProductionOrderStatus(productionOrderId: productionOrderId, productionOrderStatusUpdate: productionOrderStatusUpdate) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productionOrderId** | **UUID** |  | 
 **productionOrderStatusUpdate** | [**ProductionOrderStatusUpdate**](ProductionOrderStatusUpdate.md) |  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

