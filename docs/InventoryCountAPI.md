# InventoryCountAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createInventoryCount**](InventoryCountAPI.md#createinventorycount) | **POST** /api/v1/inventory-counts | 
[**deleteInventoryCount**](InventoryCountAPI.md#deleteinventorycount) | **DELETE** /api/v1/inventory-counts/{inventory_count_id} | 
[**generateInventoryCount**](InventoryCountAPI.md#generateinventorycount) | **POST** /api/v1/inventory-counts/generate | 
[**getInventoryCount**](InventoryCountAPI.md#getinventorycount) | **GET** /api/v1/inventory-counts/{inventory_count_id} | 
[**listInventoryCounts**](InventoryCountAPI.md#listinventorycounts) | **GET** /api/v1/inventory-counts/ | 
[**updateInventoryCount**](InventoryCountAPI.md#updateinventorycount) | **PUT** /api/v1/inventory-counts/{inventory_count_id} | 
[**updateInventoryCountStatus**](InventoryCountAPI.md#updateinventorycountstatus) | **PUT** /api/v1/inventory-counts/{inventory_count_id}/status | 


# **createInventoryCount**
```swift
    open class func createInventoryCount(inventoryCount: InventoryCount, completion: @escaping (_ data: InventoryCount?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let inventoryCount = InventoryCount(countDate: Date(), countNumber: "countNumber_example", lineItems: 123, notes: "notes_example", status: InventoryCountStatus(), warehouseId: "warehouseId_example") // InventoryCount | 

InventoryCountAPI.createInventoryCount(inventoryCount: inventoryCount) { (response, error) in
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
 **inventoryCount** | [**InventoryCount**](InventoryCount.md) |  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteInventoryCount**
```swift
    open class func deleteInventoryCount(inventoryCountId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let inventoryCountId = "inventoryCountId_example" // String | 

InventoryCountAPI.deleteInventoryCount(inventoryCountId: inventoryCountId) { (response, error) in
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
 **inventoryCountId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generateInventoryCount**
```swift
    open class func generateInventoryCount(generateCountRequest: GenerateCountRequest, completion: @escaping (_ data: InventoryCount?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let generateCountRequest = GenerateCountRequest(notes: "notes_example", productIds: [123], warehouseId: "warehouseId_example") // GenerateCountRequest | 

InventoryCountAPI.generateInventoryCount(generateCountRequest: generateCountRequest) { (response, error) in
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
 **generateCountRequest** | [**GenerateCountRequest**](GenerateCountRequest.md) |  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getInventoryCount**
```swift
    open class func getInventoryCount(inventoryCountId: String, completion: @escaping (_ data: InventoryCount?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let inventoryCountId = "inventoryCountId_example" // String | 

InventoryCountAPI.getInventoryCount(inventoryCountId: inventoryCountId) { (response, error) in
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
 **inventoryCountId** | **String** |  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listInventoryCounts**
```swift
    open class func listInventoryCounts(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, warehouseId: String? = nil, completion: @escaping (_ data: [InventoryCount]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let warehouseId = "warehouseId_example" // String |  (optional)

InventoryCountAPI.listInventoryCounts(page: page, pageSize: pageSize, status: status, warehouseId: warehouseId) { (response, error) in
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

[**[InventoryCount]**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateInventoryCount**
```swift
    open class func updateInventoryCount(inventoryCountId: String, body: AnyCodable, completion: @escaping (_ data: InventoryCount?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let inventoryCountId = "inventoryCountId_example" // String | 
let body =  // AnyCodable | 

InventoryCountAPI.updateInventoryCount(inventoryCountId: inventoryCountId, body: body) { (response, error) in
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
 **inventoryCountId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateInventoryCountStatus**
```swift
    open class func updateInventoryCountStatus(inventoryCountId: String, inventoryCountStatusUpdate: InventoryCountStatusUpdate, completion: @escaping (_ data: InventoryCount?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let inventoryCountId = "inventoryCountId_example" // String | 
let inventoryCountStatusUpdate = InventoryCountStatusUpdate(status: "status_example") // InventoryCountStatusUpdate | 

InventoryCountAPI.updateInventoryCountStatus(inventoryCountId: inventoryCountId, inventoryCountStatusUpdate: inventoryCountStatusUpdate) { (response, error) in
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
 **inventoryCountId** | **String** |  | 
 **inventoryCountStatusUpdate** | [**InventoryCountStatusUpdate**](InventoryCountStatusUpdate.md) |  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

