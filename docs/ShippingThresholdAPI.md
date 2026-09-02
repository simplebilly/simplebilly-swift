# ShippingThresholdAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createShippingThreshold**](ShippingThresholdAPI.md#createshippingthreshold) | **POST** /api/v1/shipping-thresholds | 
[**deleteShippingThreshold**](ShippingThresholdAPI.md#deleteshippingthreshold) | **DELETE** /api/v1/shipping-thresholds/{threshold_id} | 
[**getDeliverable**](ShippingThresholdAPI.md#getdeliverable) | **GET** /api/v1/shipping-thresholds/deliverable | 
[**getShippingThreshold**](ShippingThresholdAPI.md#getshippingthreshold) | **GET** /api/v1/shipping-thresholds/{threshold_id} | 
[**listShippingThresholds**](ShippingThresholdAPI.md#listshippingthresholds) | **GET** /api/v1/shipping-thresholds/ | 
[**updateShippingThreshold**](ShippingThresholdAPI.md#updateshippingthreshold) | **PUT** /api/v1/shipping-thresholds/{threshold_id} | 


# **createShippingThreshold**
```swift
    open class func createShippingThreshold(shippingThresholdCreate: ShippingThresholdCreate, completion: @escaping (_ data: ShippingThreshold?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shippingThresholdCreate = ShippingThresholdCreate(isActive: false, maxSellable: 123, name: "name_example", notes: "notes_example", productId: 123, reserveStock: 123, warehouseId: "warehouseId_example") // ShippingThresholdCreate | 

ShippingThresholdAPI.createShippingThreshold(shippingThresholdCreate: shippingThresholdCreate) { (response, error) in
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
 **shippingThresholdCreate** | [**ShippingThresholdCreate**](ShippingThresholdCreate.md) |  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteShippingThreshold**
```swift
    open class func deleteShippingThreshold(thresholdId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let thresholdId = "thresholdId_example" // String | 

ShippingThresholdAPI.deleteShippingThreshold(thresholdId: thresholdId) { (response, error) in
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
 **thresholdId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDeliverable**
```swift
    open class func getDeliverable(productId: UUID, warehouseId: String? = nil, completion: @escaping (_ data: DeliverableResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 
let warehouseId = "warehouseId_example" // String |  (optional)

ShippingThresholdAPI.getDeliverable(productId: productId, warehouseId: warehouseId) { (response, error) in
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
 **productId** | **UUID** |  | 
 **warehouseId** | **String** |  | [optional] 

### Return type

[**DeliverableResponse**](DeliverableResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getShippingThreshold**
```swift
    open class func getShippingThreshold(thresholdId: String, completion: @escaping (_ data: ShippingThreshold?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let thresholdId = "thresholdId_example" // String | 

ShippingThresholdAPI.getShippingThreshold(thresholdId: thresholdId) { (response, error) in
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
 **thresholdId** | **String** |  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listShippingThresholds**
```swift
    open class func listShippingThresholds(page: Int? = nil, pageSize: Int? = nil, productId: UUID? = nil, warehouseId: String? = nil, isActive: Bool? = nil, completion: @escaping (_ data: [ShippingThreshold]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let productId = 987 // UUID |  (optional)
let warehouseId = "warehouseId_example" // String |  (optional)
let isActive = true // Bool |  (optional)

ShippingThresholdAPI.listShippingThresholds(page: page, pageSize: pageSize, productId: productId, warehouseId: warehouseId, isActive: isActive) { (response, error) in
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
 **isActive** | **Bool** |  | [optional] 

### Return type

[**[ShippingThreshold]**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateShippingThreshold**
```swift
    open class func updateShippingThreshold(thresholdId: String, shippingThresholdUpdate: ShippingThresholdUpdate, completion: @escaping (_ data: ShippingThreshold?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let thresholdId = "thresholdId_example" // String | 
let shippingThresholdUpdate = ShippingThresholdUpdate(isActive: false, maxSellable: 123, name: "name_example", notes: "notes_example", productId: 123, reserveStock: 123, warehouseId: "warehouseId_example") // ShippingThresholdUpdate | 

ShippingThresholdAPI.updateShippingThreshold(thresholdId: thresholdId, shippingThresholdUpdate: shippingThresholdUpdate) { (response, error) in
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
 **thresholdId** | **String** |  | 
 **shippingThresholdUpdate** | [**ShippingThresholdUpdate**](ShippingThresholdUpdate.md) |  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

