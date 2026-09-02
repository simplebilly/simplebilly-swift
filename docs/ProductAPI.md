# ProductAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createProductApi**](ProductAPI.md#createproductapi) | **POST** /api/v1/products | 
[**deleteProductApi**](ProductAPI.md#deleteproductapi) | **DELETE** /api/v1/products/{product_id} | 
[**getProductApi**](ProductAPI.md#getproductapi) | **GET** /api/v1/products/{product_id} | 
[**getProductStockApi**](ProductAPI.md#getproductstockapi) | **GET** /api/v1/products/{product_id}/stock | 
[**getProductsApi**](ProductAPI.md#getproductsapi) | **GET** /api/v1/products/ | 
[**listLowStockProductsApi**](ProductAPI.md#listlowstockproductsapi) | **GET** /api/v1/products/low-stock | 
[**productRestore**](ProductAPI.md#productrestore) | **POST** /api/v1/products/{product_id}/restore | 
[**updateProductApi**](ProductAPI.md#updateproductapi) | **PUT** /api/v1/products/{product_id} | 
[**updateProductStockApi**](ProductAPI.md#updateproductstockapi) | **PUT** /api/v1/products/{product_id}/stock | 


# **createProductApi**
```swift
    open class func createProductApi(productCreate: ProductCreate, completion: @escaping (_ data: Product?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productCreate = ProductCreate(availability: "availability_example", barcode: "barcode_example", brand: "brand_example", categoryId: "categoryId_example", condition: "condition_example", defaultLedgerAccount: "defaultLedgerAccount_example", defaultPrice: "defaultPrice_example", defaultPriceFormulaId: 123, defaultTaxRate: "defaultTaxRate_example", description: "description_example", gtin: "gtin_example", height: "height_example", imageLink: "imageLink_example", images: 123, isTaxable: false, length: "length_example", link: "link_example", maxStock: 123, minStock: 123, mpn: "mpn_example", name: "name_example", packageHeight: "packageHeight_example", packageLength: "packageLength_example", packageWeightUnit: "packageWeightUnit_example", packageWeightValue: "packageWeightValue_example", packageWidth: "packageWidth_example", productCode: "productCode_example", productType: "productType_example", purchasePrice: "purchasePrice_example", reorderQuantity: 123, salePrice: "salePrice_example", shippingPrice: "shippingPrice_example", shippingRequiresInsurance: false, sku: "sku_example", stockQuantity: 123, tags: 123, taxPrice: "taxPrice_example", trackBatch: false, trackSerial: false, unit: 123, weightUnit: "weightUnit_example", weightValue: "weightValue_example", width: "width_example") // ProductCreate | 

ProductAPI.createProductApi(productCreate: productCreate) { (response, error) in
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
 **productCreate** | [**ProductCreate**](ProductCreate.md) |  | 

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProductApi**
```swift
    open class func deleteProductApi(productId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 

ProductAPI.deleteProductApi(productId: productId) { (response, error) in
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

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProductApi**
```swift
    open class func getProductApi(productId: UUID, completion: @escaping (_ data: Product?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 

ProductAPI.getProductApi(productId: productId) { (response, error) in
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

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProductStockApi**
```swift
    open class func getProductStockApi(productId: UUID, completion: @escaping (_ data: ProductStock?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 

ProductAPI.getProductStockApi(productId: productId) { (response, error) in
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

### Return type

[**ProductStock**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProductsApi**
```swift
    open class func getProductsApi(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Product]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

ProductAPI.getProductsApi(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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
 **includeDeleted** | **Bool** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**[Product]**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listLowStockProductsApi**
```swift
    open class func listLowStockProductsApi(threshold: Int64? = nil, completion: @escaping (_ data: [ProductStock]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let threshold = 987 // Int64 |  (optional)

ProductAPI.listLowStockProductsApi(threshold: threshold) { (response, error) in
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
 **threshold** | **Int64** |  | [optional] 

### Return type

[**[ProductStock]**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **productRestore**
```swift
    open class func productRestore(productId: UUID, completion: @escaping (_ data: Product?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 

ProductAPI.productRestore(productId: productId) { (response, error) in
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

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProductApi**
```swift
    open class func updateProductApi(productId: UUID, productUpdate: ProductUpdate, completion: @escaping (_ data: Product?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 
let productUpdate = ProductUpdate(availability: "availability_example", barcode: "barcode_example", brand: "brand_example", categoryId: "categoryId_example", condition: "condition_example", defaultLedgerAccount: "defaultLedgerAccount_example", defaultPrice: "defaultPrice_example", defaultPriceFormulaId: 123, defaultTaxRate: "defaultTaxRate_example", description: "description_example", gtin: "gtin_example", height: "height_example", imageLink: "imageLink_example", images: 123, isTaxable: false, length: "length_example", link: "link_example", maxStock: 123, minStock: 123, mpn: "mpn_example", name: "name_example", packageHeight: "packageHeight_example", packageLength: "packageLength_example", packageWeightUnit: "packageWeightUnit_example", packageWeightValue: "packageWeightValue_example", packageWidth: "packageWidth_example", productCode: "productCode_example", productType: "productType_example", purchasePrice: "purchasePrice_example", reorderQuantity: 123, salePrice: "salePrice_example", shippingPrice: "shippingPrice_example", shippingRequiresInsurance: false, sku: "sku_example", stockQuantity: 123, tags: 123, taxPrice: "taxPrice_example", trackBatch: false, trackSerial: false, unit: 123, weightUnit: "weightUnit_example", weightValue: "weightValue_example", width: "width_example") // ProductUpdate | 

ProductAPI.updateProductApi(productId: productId, productUpdate: productUpdate) { (response, error) in
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
 **productUpdate** | [**ProductUpdate**](ProductUpdate.md) |  | 

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProductStockApi**
```swift
    open class func updateProductStockApi(productId: UUID, stockUpdateRequest: StockUpdateRequest, completion: @escaping (_ data: ProductStock?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 
let stockUpdateRequest = StockUpdateRequest(quantity: 123) // StockUpdateRequest | 

ProductAPI.updateProductStockApi(productId: productId, stockUpdateRequest: stockUpdateRequest) { (response, error) in
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
 **stockUpdateRequest** | [**StockUpdateRequest**](StockUpdateRequest.md) |  | 

### Return type

[**ProductStock**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

