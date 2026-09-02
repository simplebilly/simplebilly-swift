# ShippingRuleAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createShippingRule**](ShippingRuleAPI.md#createshippingrule) | **POST** /api/v1/shipping-rules | 
[**deleteShippingRule**](ShippingRuleAPI.md#deleteshippingrule) | **DELETE** /api/v1/shipping-rules/{rule_id} | 
[**getShippingRule**](ShippingRuleAPI.md#getshippingrule) | **GET** /api/v1/shipping-rules/{rule_id} | 
[**listShippingRules**](ShippingRuleAPI.md#listshippingrules) | **GET** /api/v1/shipping-rules/ | 
[**updateShippingRule**](ShippingRuleAPI.md#updateshippingrule) | **PUT** /api/v1/shipping-rules/{rule_id} | 


# **createShippingRule**
```swift
    open class func createShippingRule(shippingRuleCreate: ShippingRuleCreate, completion: @escaping (_ data: ShippingRule?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shippingRuleCreate = ShippingRuleCreate(carrier: "carrier_example", country: CountryCode(), deliveryTime: "deliveryTime_example", isActive: false, maxWeightKg: 123, minWeightKg: 123, name: "name_example", notes: "notes_example", price: "price_example", priority: 123) // ShippingRuleCreate | 

ShippingRuleAPI.createShippingRule(shippingRuleCreate: shippingRuleCreate) { (response, error) in
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
 **shippingRuleCreate** | [**ShippingRuleCreate**](ShippingRuleCreate.md) |  | 

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteShippingRule**
```swift
    open class func deleteShippingRule(ruleId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ruleId = "ruleId_example" // String | 

ShippingRuleAPI.deleteShippingRule(ruleId: ruleId) { (response, error) in
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
 **ruleId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getShippingRule**
```swift
    open class func getShippingRule(ruleId: String, completion: @escaping (_ data: ShippingRule?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ruleId = "ruleId_example" // String | 

ShippingRuleAPI.getShippingRule(ruleId: ruleId) { (response, error) in
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
 **ruleId** | **String** |  | 

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listShippingRules**
```swift
    open class func listShippingRules(page: Int? = nil, pageSize: Int? = nil, country: String? = nil, completion: @escaping (_ data: [ShippingRule]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let country = "country_example" // String |  (optional)

ShippingRuleAPI.listShippingRules(page: page, pageSize: pageSize, country: country) { (response, error) in
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
 **country** | **String** |  | [optional] 

### Return type

[**[ShippingRule]**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateShippingRule**
```swift
    open class func updateShippingRule(ruleId: String, shippingRuleUpdate: ShippingRuleUpdate, completion: @escaping (_ data: ShippingRule?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ruleId = "ruleId_example" // String | 
let shippingRuleUpdate = ShippingRuleUpdate(carrier: "carrier_example", country: CountryCode(), deliveryTime: "deliveryTime_example", isActive: false, maxWeightKg: 123, minWeightKg: 123, name: "name_example", notes: "notes_example", price: "price_example", priority: 123) // ShippingRuleUpdate | 

ShippingRuleAPI.updateShippingRule(ruleId: ruleId, shippingRuleUpdate: shippingRuleUpdate) { (response, error) in
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
 **ruleId** | **String** |  | 
 **shippingRuleUpdate** | [**ShippingRuleUpdate**](ShippingRuleUpdate.md) |  | 

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

