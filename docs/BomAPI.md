# BomAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createBom**](BomAPI.md#createbom) | **POST** /api/v1/boms | 
[**deleteBom**](BomAPI.md#deletebom) | **DELETE** /api/v1/boms/{bom_id} | 
[**getBom**](BomAPI.md#getbom) | **GET** /api/v1/boms/{bom_id} | 
[**listBoms**](BomAPI.md#listboms) | **GET** /api/v1/boms/ | 
[**updateBom**](BomAPI.md#updatebom) | **PUT** /api/v1/boms/{bom_id} | 


# **createBom**
```swift
    open class func createBom(bomCreate: BomCreate, completion: @escaping (_ data: Bom?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let bomCreate = BomCreate(components: 123, description: "description_example", name: "name_example", outputQuantity: 123, productId: 123, status: BomStatus()) // BomCreate | 

BomAPI.createBom(bomCreate: bomCreate) { (response, error) in
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
 **bomCreate** | [**BomCreate**](BomCreate.md) |  | 

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteBom**
```swift
    open class func deleteBom(bomId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let bomId = 987 // UUID | 

BomAPI.deleteBom(bomId: bomId) { (response, error) in
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
 **bomId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getBom**
```swift
    open class func getBom(bomId: UUID, completion: @escaping (_ data: Bom?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let bomId = 987 // UUID | 

BomAPI.getBom(bomId: bomId) { (response, error) in
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
 **bomId** | **UUID** |  | 

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listBoms**
```swift
    open class func listBoms(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, productId: UUID? = nil, completion: @escaping (_ data: [Bom]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let productId = 987 // UUID | Filter by finished product id. (optional)

BomAPI.listBoms(page: page, pageSize: pageSize, search: search, productId: productId) { (response, error) in
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
 **productId** | **UUID** | Filter by finished product id. | [optional] 

### Return type

[**[Bom]**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateBom**
```swift
    open class func updateBom(bomId: UUID, bomUpdate: BomUpdate, completion: @escaping (_ data: Bom?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let bomId = 987 // UUID | 
let bomUpdate = BomUpdate(components: 123, description: "description_example", name: "name_example", outputQuantity: 123, productId: 123, status: BomStatus()) // BomUpdate | 

BomAPI.updateBom(bomId: bomId, bomUpdate: bomUpdate) { (response, error) in
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
 **bomId** | **UUID** |  | 
 **bomUpdate** | [**BomUpdate**](BomUpdate.md) |  | 

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

