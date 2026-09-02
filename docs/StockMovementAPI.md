# StockMovementAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getStockMovement**](StockMovementAPI.md#getstockmovement) | **GET** /api/v1/stock-movements/{movement_id} | 
[**listStockMovements**](StockMovementAPI.md#liststockmovements) | **GET** /api/v1/stock-movements/ | 


# **getStockMovement**
```swift
    open class func getStockMovement(movementId: String, completion: @escaping (_ data: StockMovement?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let movementId = "movementId_example" // String | 

StockMovementAPI.getStockMovement(movementId: movementId) { (response, error) in
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
 **movementId** | **String** |  | 

### Return type

[**StockMovement**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listStockMovements**
```swift
    open class func listStockMovements(page: Int? = nil, pageSize: Int? = nil, productId: UUID? = nil, warehouseId: String? = nil, movementType: String? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [StockMovement]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let productId = 987 // UUID |  (optional)
let warehouseId = "warehouseId_example" // String |  (optional)
let movementType = "movementType_example" // String |  (optional)
let from = Date() // Date | Only movements on or after this date (inclusive). (optional)
let to = Date() // Date | Only movements on or before this date (inclusive). (optional)

StockMovementAPI.listStockMovements(page: page, pageSize: pageSize, productId: productId, warehouseId: warehouseId, movementType: movementType, from: from, to: to) { (response, error) in
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
 **productId** | **UUID** |  | [optional] 
 **warehouseId** | **String** |  | [optional] 
 **movementType** | **String** |  | [optional] 
 **from** | **Date** | Only movements on or after this date (inclusive). | [optional] 
 **to** | **Date** | Only movements on or before this date (inclusive). | [optional] 

### Return type

[**[StockMovement]**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

