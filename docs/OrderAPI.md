# OrderAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addOrderTags**](OrderAPI.md#addordertags) | **POST** /api/v1/orders/{order_id}/tags | 
[**findOrderByExternalRef**](OrderAPI.md#findorderbyexternalref) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} | 
[**getOrder**](OrderAPI.md#getorder) | **GET** /api/v1/order/{order_number} | 
[**getOrders**](OrderAPI.md#getorders) | **GET** /api/v1/orders | 
[**patchOrder**](OrderAPI.md#patchorder) | **PATCH** /api/v1/orders/{order_id} | 
[**replaceOrderTags**](OrderAPI.md#replaceordertags) | **PUT** /api/v1/orders/{order_id}/tags | 
[**updateOrderState**](OrderAPI.md#updateorderstate) | **PUT** /api/v1/orders/{order_id}/state | 


# **addOrderTags**
```swift
    open class func addOrderTags(orderId: String, orderTagsRequest: OrderTagsRequest, completion: @escaping (_ data: Order?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderId = "orderId_example" // String | 
let orderTagsRequest = OrderTagsRequest(tags: ["tags_example"]) // OrderTagsRequest | 

OrderAPI.addOrderTags(orderId: orderId, orderTagsRequest: orderTagsRequest) { (response, error) in
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
 **orderId** | **String** |  | 
 **orderTagsRequest** | [**OrderTagsRequest**](OrderTagsRequest.md) |  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **findOrderByExternalRef**
```swift
    open class func findOrderByExternalRef(extRef: String, completion: @escaping (_ data: Order?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let extRef = "extRef_example" // String | 

OrderAPI.findOrderByExternalRef(extRef: extRef) { (response, error) in
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
 **extRef** | **String** |  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getOrder**
```swift
    open class func getOrder(orderNumber: String, completion: @escaping (_ data: Order?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderNumber = "orderNumber_example" // String | 

OrderAPI.getOrder(orderNumber: orderNumber) { (response, error) in
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
 **orderNumber** | **String** |  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getOrders**
```swift
    open class func getOrders(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Order]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

OrderAPI.getOrders(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[Order]**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patchOrder**
```swift
    open class func patchOrder(orderId: String, body: AnyCodable, completion: @escaping (_ data: Order?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderId = "orderId_example" // String | 
let body =  // AnyCodable | 

OrderAPI.patchOrder(orderId: orderId, body: body) { (response, error) in
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
 **orderId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replaceOrderTags**
```swift
    open class func replaceOrderTags(orderId: String, orderTagsRequest: OrderTagsRequest, completion: @escaping (_ data: Order?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderId = "orderId_example" // String | 
let orderTagsRequest = OrderTagsRequest(tags: ["tags_example"]) // OrderTagsRequest | 

OrderAPI.replaceOrderTags(orderId: orderId, orderTagsRequest: orderTagsRequest) { (response, error) in
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
 **orderId** | **String** |  | 
 **orderTagsRequest** | [**OrderTagsRequest**](OrderTagsRequest.md) |  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateOrderState**
```swift
    open class func updateOrderState(orderId: String, orderStateUpdate: OrderStateUpdate, completion: @escaping (_ data: Order?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderId = "orderId_example" // String | 
let orderStateUpdate = OrderStateUpdate(sendStateToShop: false, state: "state_example") // OrderStateUpdate | 

OrderAPI.updateOrderState(orderId: orderId, orderStateUpdate: orderStateUpdate) { (response, error) in
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
 **orderId** | **String** |  | 
 **orderStateUpdate** | [**OrderStateUpdate**](OrderStateUpdate.md) |  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

