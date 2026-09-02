# GoodsReceiptAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createGoodsReceipt**](GoodsReceiptAPI.md#creategoodsreceipt) | **POST** /api/v1/goods-receipts | 
[**deleteGoodsReceipt**](GoodsReceiptAPI.md#deletegoodsreceipt) | **DELETE** /api/v1/goods-receipts/{goods_receipt_id} | 
[**getGoodsReceipt**](GoodsReceiptAPI.md#getgoodsreceipt) | **GET** /api/v1/goods-receipts/{goods_receipt_id} | 
[**listGoodsReceipts**](GoodsReceiptAPI.md#listgoodsreceipts) | **GET** /api/v1/goods-receipts/ | 


# **createGoodsReceipt**
```swift
    open class func createGoodsReceipt(goodsReceipt: GoodsReceipt, completion: @escaping (_ data: GoodsReceipt?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let goodsReceipt = GoodsReceipt(grNumber: "grNumber_example", lineItems: 123, notes: "notes_example", purchaseOrderId: "purchaseOrderId_example", receiptDate: Date(), supplierContactId: "supplierContactId_example", supplierName: "supplierName_example", warehouseId: "warehouseId_example") // GoodsReceipt | 

GoodsReceiptAPI.createGoodsReceipt(goodsReceipt: goodsReceipt) { (response, error) in
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
 **goodsReceipt** | [**GoodsReceipt**](GoodsReceipt.md) |  | 

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteGoodsReceipt**
```swift
    open class func deleteGoodsReceipt(goodsReceiptId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let goodsReceiptId = "goodsReceiptId_example" // String | 

GoodsReceiptAPI.deleteGoodsReceipt(goodsReceiptId: goodsReceiptId) { (response, error) in
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
 **goodsReceiptId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getGoodsReceipt**
```swift
    open class func getGoodsReceipt(goodsReceiptId: String, completion: @escaping (_ data: GoodsReceipt?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let goodsReceiptId = "goodsReceiptId_example" // String | 

GoodsReceiptAPI.getGoodsReceipt(goodsReceiptId: goodsReceiptId) { (response, error) in
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
 **goodsReceiptId** | **String** |  | 

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listGoodsReceipts**
```swift
    open class func listGoodsReceipts(page: Int? = nil, pageSize: Int? = nil, purchaseOrderId: String? = nil, supplierName: String? = nil, warehouseId: String? = nil, completion: @escaping (_ data: [GoodsReceipt]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let purchaseOrderId = "purchaseOrderId_example" // String |  (optional)
let supplierName = "supplierName_example" // String |  (optional)
let warehouseId = "warehouseId_example" // String |  (optional)

GoodsReceiptAPI.listGoodsReceipts(page: page, pageSize: pageSize, purchaseOrderId: purchaseOrderId, supplierName: supplierName, warehouseId: warehouseId) { (response, error) in
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
 **purchaseOrderId** | **String** |  | [optional] 
 **supplierName** | **String** |  | [optional] 
 **warehouseId** | **String** |  | [optional] 

### Return type

[**[GoodsReceipt]**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

