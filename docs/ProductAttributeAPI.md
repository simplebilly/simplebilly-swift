# ProductAttributeAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createProductAttribute**](ProductAttributeAPI.md#createproductattribute) | **POST** /api/v1/product-attributes | 
[**deleteProductAttribute**](ProductAttributeAPI.md#deleteproductattribute) | **DELETE** /api/v1/product-attributes/{attribute_id} | 
[**getProductAttribute**](ProductAttributeAPI.md#getproductattribute) | **GET** /api/v1/product-attributes/{attribute_id} | 
[**listProductAttributes**](ProductAttributeAPI.md#listproductattributes) | **GET** /api/v1/product-attributes/ | 
[**updateProductAttribute**](ProductAttributeAPI.md#updateproductattribute) | **PUT** /api/v1/product-attributes/{attribute_id} | 


# **createProductAttribute**
```swift
    open class func createProductAttribute(productAttributeCreate: ProductAttributeCreate, completion: @escaping (_ data: ProductAttribute?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productAttributeCreate = ProductAttributeCreate(isFilterable: false, name: "name_example", position: 123, productId: 123, unit: "unit_example", value: "value_example") // ProductAttributeCreate | 

ProductAttributeAPI.createProductAttribute(productAttributeCreate: productAttributeCreate) { (response, error) in
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
 **productAttributeCreate** | [**ProductAttributeCreate**](ProductAttributeCreate.md) |  | 

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProductAttribute**
```swift
    open class func deleteProductAttribute(attributeId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attributeId = "attributeId_example" // String | 

ProductAttributeAPI.deleteProductAttribute(attributeId: attributeId) { (response, error) in
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
 **attributeId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProductAttribute**
```swift
    open class func getProductAttribute(attributeId: String, completion: @escaping (_ data: ProductAttribute?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attributeId = "attributeId_example" // String | 

ProductAttributeAPI.getProductAttribute(attributeId: attributeId) { (response, error) in
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
 **attributeId** | **String** |  | 

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProductAttributes**
```swift
    open class func listProductAttributes(page: Int? = nil, pageSize: Int? = nil, productId: UUID? = nil, isFilterable: Bool? = nil, search: String? = nil, completion: @escaping (_ data: [ProductAttribute]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let productId = 987 // UUID |  (optional)
let isFilterable = true // Bool |  (optional)
let search = "search_example" // String |  (optional)

ProductAttributeAPI.listProductAttributes(page: page, pageSize: pageSize, productId: productId, isFilterable: isFilterable, search: search) { (response, error) in
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
 **isFilterable** | **Bool** |  | [optional] 
 **search** | **String** |  | [optional] 

### Return type

[**[ProductAttribute]**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProductAttribute**
```swift
    open class func updateProductAttribute(attributeId: String, productAttributeUpdate: ProductAttributeUpdate, completion: @escaping (_ data: ProductAttribute?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attributeId = "attributeId_example" // String | 
let productAttributeUpdate = ProductAttributeUpdate(isFilterable: false, name: "name_example", position: 123, productId: 123, unit: "unit_example", value: "value_example") // ProductAttributeUpdate | 

ProductAttributeAPI.updateProductAttribute(attributeId: attributeId, productAttributeUpdate: productAttributeUpdate) { (response, error) in
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
 **attributeId** | **String** |  | 
 **productAttributeUpdate** | [**ProductAttributeUpdate**](ProductAttributeUpdate.md) |  | 

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

