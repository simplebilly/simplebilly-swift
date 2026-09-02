# ProductVariantAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createProductVariant**](ProductVariantAPI.md#createproductvariant) | **POST** /api/v1/product-variants | 
[**deleteProductVariant**](ProductVariantAPI.md#deleteproductvariant) | **DELETE** /api/v1/product-variants/{variant_id} | 
[**generateProductVariants**](ProductVariantAPI.md#generateproductvariants) | **POST** /api/v1/product-variants/generate | 
[**getProductVariant**](ProductVariantAPI.md#getproductvariant) | **GET** /api/v1/product-variants/{variant_id} | 
[**listProductVariants**](ProductVariantAPI.md#listproductvariants) | **GET** /api/v1/product-variants/ | 
[**updateProductVariant**](ProductVariantAPI.md#updateproductvariant) | **PUT** /api/v1/product-variants/{variant_id} | 


# **createProductVariant**
```swift
    open class func createProductVariant(productVariant: ProductVariant, completion: @escaping (_ data: ProductVariant?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productVariant = ProductVariant(barcode: "barcode_example", imageLink: "imageLink_example", isActive: false, name: "name_example", optionValues: 123, price: "price_example", priceDelta: "priceDelta_example", productId: 123, sku: "sku_example", stockQuantity: 123) // ProductVariant | 

ProductVariantAPI.createProductVariant(productVariant: productVariant) { (response, error) in
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
 **productVariant** | [**ProductVariant**](ProductVariant.md) |  | 

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProductVariant**
```swift
    open class func deleteProductVariant(variantId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let variantId = "variantId_example" // String | 

ProductVariantAPI.deleteProductVariant(variantId: variantId) { (response, error) in
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
 **variantId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generateProductVariants**
```swift
    open class func generateProductVariants(generateVariantsRequest: GenerateVariantsRequest, completion: @escaping (_ data: [ProductVariant]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let generateVariantsRequest = GenerateVariantsRequest(options: "TODO", priceDelta: "priceDelta_example", productId: 123, skuPrefix: "skuPrefix_example") // GenerateVariantsRequest | 

ProductVariantAPI.generateProductVariants(generateVariantsRequest: generateVariantsRequest) { (response, error) in
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
 **generateVariantsRequest** | [**GenerateVariantsRequest**](GenerateVariantsRequest.md) |  | 

### Return type

[**[ProductVariant]**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProductVariant**
```swift
    open class func getProductVariant(variantId: String, completion: @escaping (_ data: ProductVariant?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let variantId = "variantId_example" // String | 

ProductVariantAPI.getProductVariant(variantId: variantId) { (response, error) in
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
 **variantId** | **String** |  | 

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProductVariants**
```swift
    open class func listProductVariants(page: Int? = nil, pageSize: Int? = nil, productId: UUID? = nil, isActive: Bool? = nil, completion: @escaping (_ data: [ProductVariant]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let productId = 987 // UUID |  (optional)
let isActive = true // Bool |  (optional)

ProductVariantAPI.listProductVariants(page: page, pageSize: pageSize, productId: productId, isActive: isActive) { (response, error) in
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
 **isActive** | **Bool** |  | [optional] 

### Return type

[**[ProductVariant]**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProductVariant**
```swift
    open class func updateProductVariant(variantId: String, body: AnyCodable, completion: @escaping (_ data: ProductVariant?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let variantId = "variantId_example" // String | 
let body =  // AnyCodable | 

ProductVariantAPI.updateProductVariant(variantId: variantId, body: body) { (response, error) in
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
 **variantId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

