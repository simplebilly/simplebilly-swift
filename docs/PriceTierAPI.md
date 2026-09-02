# PriceTierAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPriceTier**](PriceTierAPI.md#createpricetier) | **POST** /api/v1/price-tiers | 
[**deletePriceTier**](PriceTierAPI.md#deletepricetier) | **DELETE** /api/v1/price-tiers/{price_tier_id} | 
[**getPriceTier**](PriceTierAPI.md#getpricetier) | **GET** /api/v1/price-tiers/{price_tier_id} | 
[**getResolvedPrice**](PriceTierAPI.md#getresolvedprice) | **GET** /api/v1/price-tiers/resolved | 
[**listPriceTiers**](PriceTierAPI.md#listpricetiers) | **GET** /api/v1/price-tiers/ | 
[**updatePriceTier**](PriceTierAPI.md#updatepricetier) | **PUT** /api/v1/price-tiers/{price_tier_id} | 


# **createPriceTier**
```swift
    open class func createPriceTier(priceTierCreate: PriceTierCreate, completion: @escaping (_ data: PriceTier?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let priceTierCreate = PriceTierCreate(customerGroupId: "customerGroupId_example", minQuantity: 123, productId: 123, unitPrice: "unitPrice_example") // PriceTierCreate | 

PriceTierAPI.createPriceTier(priceTierCreate: priceTierCreate) { (response, error) in
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
 **priceTierCreate** | [**PriceTierCreate**](PriceTierCreate.md) |  | 

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePriceTier**
```swift
    open class func deletePriceTier(priceTierId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let priceTierId = "priceTierId_example" // String | 

PriceTierAPI.deletePriceTier(priceTierId: priceTierId) { (response, error) in
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
 **priceTierId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPriceTier**
```swift
    open class func getPriceTier(priceTierId: String, completion: @escaping (_ data: PriceTier?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let priceTierId = "priceTierId_example" // String | 

PriceTierAPI.getPriceTier(priceTierId: priceTierId) { (response, error) in
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
 **priceTierId** | **String** |  | 

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getResolvedPrice**
```swift
    open class func getResolvedPrice(productId: UUID, quantity: Int64? = nil, contactId: String? = nil, completion: @escaping (_ data: ResolvedPriceResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let productId = 987 // UUID | 
let quantity = 987 // Int64 |  (optional)
let contactId = "contactId_example" // String | Contact used to match customer-group-scoped tiers. (optional)

PriceTierAPI.getResolvedPrice(productId: productId, quantity: quantity, contactId: contactId) { (response, error) in
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
 **quantity** | **Int64** |  | [optional] 
 **contactId** | **String** | Contact used to match customer-group-scoped tiers. | [optional] 

### Return type

[**ResolvedPriceResponse**](ResolvedPriceResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPriceTiers**
```swift
    open class func listPriceTiers(page: Int? = nil, pageSize: Int? = nil, productId: UUID? = nil, customerGroupId: String? = nil, completion: @escaping (_ data: [PriceTier]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let productId = 987 // UUID |  (optional)
let customerGroupId = "customerGroupId_example" // String |  (optional)

PriceTierAPI.listPriceTiers(page: page, pageSize: pageSize, productId: productId, customerGroupId: customerGroupId) { (response, error) in
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
 **customerGroupId** | **String** |  | [optional] 

### Return type

[**[PriceTier]**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePriceTier**
```swift
    open class func updatePriceTier(priceTierId: String, priceTierUpdate: PriceTierUpdate, completion: @escaping (_ data: PriceTier?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let priceTierId = "priceTierId_example" // String | 
let priceTierUpdate = PriceTierUpdate(customerGroupId: "customerGroupId_example", minQuantity: 123, productId: 123, unitPrice: "unitPrice_example") // PriceTierUpdate | 

PriceTierAPI.updatePriceTier(priceTierId: priceTierId, priceTierUpdate: priceTierUpdate) { (response, error) in
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
 **priceTierId** | **String** |  | 
 **priceTierUpdate** | [**PriceTierUpdate**](PriceTierUpdate.md) |  | 

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

