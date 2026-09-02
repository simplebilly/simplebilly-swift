# WarehouseAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createWarehouse**](WarehouseAPI.md#createwarehouse) | **POST** /api/v1/warehouses | 
[**deleteWarehouse**](WarehouseAPI.md#deletewarehouse) | **DELETE** /api/v1/warehouses/{warehouse_id} | 
[**getWarehouse**](WarehouseAPI.md#getwarehouse) | **GET** /api/v1/warehouses/{warehouse_id} | 
[**listWarehouses**](WarehouseAPI.md#listwarehouses) | **GET** /api/v1/warehouses/ | 
[**updateWarehouse**](WarehouseAPI.md#updatewarehouse) | **PUT** /api/v1/warehouses/{warehouse_id} | 


# **createWarehouse**
```swift
    open class func createWarehouse(warehouse: Warehouse, completion: @escaping (_ data: Warehouse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouse = Warehouse(addressCity: "addressCity_example", addressCountry: CountryCode(), addressStreet: "addressStreet_example", addressZip: "addressZip_example", binLocations: 123, code: "code_example", isActive: false, isDefault: false, name: "name_example", notes: "notes_example") // Warehouse | 

WarehouseAPI.createWarehouse(warehouse: warehouse) { (response, error) in
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
 **warehouse** | [**Warehouse**](Warehouse.md) |  | 

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWarehouse**
```swift
    open class func deleteWarehouse(warehouseId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouseId = "warehouseId_example" // String | 

WarehouseAPI.deleteWarehouse(warehouseId: warehouseId) { (response, error) in
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

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWarehouse**
```swift
    open class func getWarehouse(warehouseId: String, completion: @escaping (_ data: Warehouse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouseId = "warehouseId_example" // String | 

WarehouseAPI.getWarehouse(warehouseId: warehouseId) { (response, error) in
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

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWarehouses**
```swift
    open class func listWarehouses(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, isActive: Bool? = nil, completion: @escaping (_ data: [Warehouse]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let isActive = true // Bool |  (optional)

WarehouseAPI.listWarehouses(page: page, pageSize: pageSize, search: search, isActive: isActive) { (response, error) in
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
 **isActive** | **Bool** |  | [optional] 

### Return type

[**[Warehouse]**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateWarehouse**
```swift
    open class func updateWarehouse(warehouseId: String, body: AnyCodable, completion: @escaping (_ data: Warehouse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let warehouseId = "warehouseId_example" // String | 
let body =  // AnyCodable | 

WarehouseAPI.updateWarehouse(warehouseId: warehouseId, body: body) { (response, error) in
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
 **body** | **AnyCodable** |  | 

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

