# StockTransferAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createStockTransfer**](StockTransferAPI.md#createstocktransfer) | **POST** /api/v1/stock-transfers | 
[**deleteStockTransfer**](StockTransferAPI.md#deletestocktransfer) | **DELETE** /api/v1/stock-transfers/{stock_transfer_id} | 
[**getStockTransfer**](StockTransferAPI.md#getstocktransfer) | **GET** /api/v1/stock-transfers/{stock_transfer_id} | 
[**listStockTransfers**](StockTransferAPI.md#liststocktransfers) | **GET** /api/v1/stock-transfers/ | 
[**updateStockTransferStatus**](StockTransferAPI.md#updatestocktransferstatus) | **PUT** /api/v1/stock-transfers/{stock_transfer_id}/status | 


# **createStockTransfer**
```swift
    open class func createStockTransfer(stockTransfer: StockTransfer, completion: @escaping (_ data: StockTransfer?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let stockTransfer = StockTransfer(lineItems: 123, notes: "notes_example", sourceWarehouseId: "sourceWarehouseId_example", status: StockTransferStatus(), targetWarehouseId: "targetWarehouseId_example", transferDate: Date(), transferNumber: "transferNumber_example") // StockTransfer | 

StockTransferAPI.createStockTransfer(stockTransfer: stockTransfer) { (response, error) in
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
 **stockTransfer** | [**StockTransfer**](StockTransfer.md) |  | 

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteStockTransfer**
```swift
    open class func deleteStockTransfer(stockTransferId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let stockTransferId = "stockTransferId_example" // String | 

StockTransferAPI.deleteStockTransfer(stockTransferId: stockTransferId) { (response, error) in
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
 **stockTransferId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getStockTransfer**
```swift
    open class func getStockTransfer(stockTransferId: String, completion: @escaping (_ data: StockTransfer?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let stockTransferId = "stockTransferId_example" // String | 

StockTransferAPI.getStockTransfer(stockTransferId: stockTransferId) { (response, error) in
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
 **stockTransferId** | **String** |  | 

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listStockTransfers**
```swift
    open class func listStockTransfers(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, warehouseId: String? = nil, completion: @escaping (_ data: [StockTransfer]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let warehouseId = "warehouseId_example" // String |  (optional)

StockTransferAPI.listStockTransfers(page: page, pageSize: pageSize, status: status, warehouseId: warehouseId) { (response, error) in
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
 **status** | **String** |  | [optional] 
 **warehouseId** | **String** |  | [optional] 

### Return type

[**[StockTransfer]**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateStockTransferStatus**
```swift
    open class func updateStockTransferStatus(stockTransferId: String, stockTransferStatusUpdate: StockTransferStatusUpdate, completion: @escaping (_ data: StockTransfer?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let stockTransferId = "stockTransferId_example" // String | 
let stockTransferStatusUpdate = StockTransferStatusUpdate(status: "status_example") // StockTransferStatusUpdate | 

StockTransferAPI.updateStockTransferStatus(stockTransferId: stockTransferId, stockTransferStatusUpdate: stockTransferStatusUpdate) { (response, error) in
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
 **stockTransferId** | **String** |  | 
 **stockTransferStatusUpdate** | [**StockTransferStatusUpdate**](StockTransferStatusUpdate.md) |  | 

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

