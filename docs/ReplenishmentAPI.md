# ReplenishmentAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**applyReplenishments**](ReplenishmentAPI.md#applyreplenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
[**getReplenishments**](ReplenishmentAPI.md#getreplenishments) | **GET** /api/v1/replenishments | 


# **applyReplenishments**
```swift
    open class func applyReplenishments(targetWarehouseId: String? = nil, sourceWarehouseId: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let targetWarehouseId = "targetWarehouseId_example" // String | Warehouse to be replenished. Defaults to the tenant's default warehouse. (optional)
let sourceWarehouseId = "sourceWarehouseId_example" // String | Restrict source warehouses to this id. (optional)

// Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
ReplenishmentAPI.applyReplenishments(targetWarehouseId: targetWarehouseId, sourceWarehouseId: sourceWarehouseId) { (response, error) in
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
 **targetWarehouseId** | **String** | Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] 
 **sourceWarehouseId** | **String** | Restrict source warehouses to this id. | [optional] 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getReplenishments**
```swift
    open class func getReplenishments(targetWarehouseId: String? = nil, sourceWarehouseId: String? = nil, completion: @escaping (_ data: ReplenishmentResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let targetWarehouseId = "targetWarehouseId_example" // String | Warehouse to be replenished. Defaults to the tenant's default warehouse. (optional)
let sourceWarehouseId = "sourceWarehouseId_example" // String | Restrict source warehouses to this id. (optional)

ReplenishmentAPI.getReplenishments(targetWarehouseId: targetWarehouseId, sourceWarehouseId: sourceWarehouseId) { (response, error) in
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
 **targetWarehouseId** | **String** | Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] 
 **sourceWarehouseId** | **String** | Restrict source warehouses to this id. | [optional] 

### Return type

[**ReplenishmentResponse**](ReplenishmentResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

