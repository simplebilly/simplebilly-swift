# WarehouseStockAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createWarehouseStock**](WarehouseStockAPI.md#createwarehousestock) | **POST** /api/v1/warehouses/{warehouse_id}/stock | 
[**deleteWarehouseStock**](WarehouseStockAPI.md#deletewarehousestock) | **DELETE** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 
[**listWarehouseStock**](WarehouseStockAPI.md#listwarehousestock) | **GET** /api/v1/warehouses/{warehouse_id}/stock | 
[**updateWarehouseStock**](WarehouseStockAPI.md#updatewarehousestock) | **PUT** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 


# **createWarehouseStock**
```swift
    open class func createWarehouseStock(warehouseId: String, stockAdjustment: StockAdjustment, completion: @escaping (_ data: WarehouseStock?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouseId = "warehouseId_example" // String | 
let stockAdjustment = StockAdjustment(batchNumber: "batchNumber_example", binLocation: "binLocation_example", expiryDate: Date(), productId: 123, quantity: 123, serialNumbers: ["serialNumbers_example"]) // StockAdjustment | 

WarehouseStockAPI.createWarehouseStock(warehouseId: warehouseId, stockAdjustment: stockAdjustment) { (response, error) in
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
 **warehouseId** | **String** |  | 
 **stockAdjustment** | [**StockAdjustment**](StockAdjustment.md) |  | 

### Return type

[**WarehouseStock**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWarehouseStock**
```swift
    open class func deleteWarehouseStock(warehouseId: String, productId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouseId = "warehouseId_example" // String | 
let productId = 987 // UUID | 

WarehouseStockAPI.deleteWarehouseStock(warehouseId: warehouseId, productId: productId) { (response, error) in
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
 **warehouseId** | **String** |  | 
 **productId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWarehouseStock**
```swift
    open class func listWarehouseStock(warehouseId: String, completion: @escaping (_ data: [WarehouseStock]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouseId = "warehouseId_example" // String | 

WarehouseStockAPI.listWarehouseStock(warehouseId: warehouseId) { (response, error) in
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
 **warehouseId** | **String** |  | 

### Return type

[**[WarehouseStock]**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateWarehouseStock**
```swift
    open class func updateWarehouseStock(warehouseId: String, productId: UUID, stockAdjustment: StockAdjustment, completion: @escaping (_ data: WarehouseStock?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouseId = "warehouseId_example" // String | 
let productId = 987 // UUID | 
let stockAdjustment = StockAdjustment(batchNumber: "batchNumber_example", binLocation: "binLocation_example", expiryDate: Date(), productId: 123, quantity: 123, serialNumbers: ["serialNumbers_example"]) // StockAdjustment | 

WarehouseStockAPI.updateWarehouseStock(warehouseId: warehouseId, productId: productId, stockAdjustment: stockAdjustment) { (response, error) in
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
 **warehouseId** | **String** |  | 
 **productId** | **UUID** |  | 
 **stockAdjustment** | [**StockAdjustment**](StockAdjustment.md) |  | 

### Return type

[**WarehouseStock**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

