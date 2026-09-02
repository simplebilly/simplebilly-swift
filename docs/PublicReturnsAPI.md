# PublicReturnsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPublicReturnStatus**](PublicReturnsAPI.md#getpublicreturnstatus) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.
[**listPublicReturns**](PublicReturnsAPI.md#listpublicreturns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth).
[**requestPublicReturn**](PublicReturnsAPI.md#requestpublicreturn) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth).


# **getPublicReturnStatus**
```swift
    open class func getPublicReturnStatus(email: String, returnNumber: String? = nil, returnOrderId: String? = nil, orderNumber: String? = nil, completion: @escaping (_ data: PublicReturnStatusResponse?, _ error: Error?) -> Void)
```

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let email = "email_example" // String | 
let returnNumber = "returnNumber_example" // String | Either return_number or return_order_id must be provided. (optional)
let returnOrderId = "returnOrderId_example" // String |  (optional)
let orderNumber = "orderNumber_example" // String |  (optional)

// Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.
PublicReturnsAPI.getPublicReturnStatus(email: email, returnNumber: returnNumber, returnOrderId: returnOrderId, orderNumber: orderNumber) { (response, error) in
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
 **email** | **String** |  | 
 **returnNumber** | **String** | Either return_number or return_order_id must be provided. | [optional] 
 **returnOrderId** | **String** |  | [optional] 
 **orderNumber** | **String** |  | [optional] 

### Return type

[**PublicReturnStatusResponse**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPublicReturns**
```swift
    open class func listPublicReturns(orderNumber: String, email: String, completion: @escaping (_ data: [PublicReturnStatusResponse]?, _ error: Error?) -> Void)
```

List all returns for an order (public, no auth).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderNumber = "orderNumber_example" // String | 
let email = "email_example" // String | 

// List all returns for an order (public, no auth).
PublicReturnsAPI.listPublicReturns(orderNumber: orderNumber, email: email) { (response, error) in
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
 **email** | **String** |  | 

### Return type

[**[PublicReturnStatusResponse]**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **requestPublicReturn**
```swift
    open class func requestPublicReturn(publicReturnRequest: PublicReturnRequest, completion: @escaping (_ data: PublicReturnResponse?, _ error: Error?) -> Void)
```

Customer requests a return for an order (public, no auth).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let publicReturnRequest = PublicReturnRequest(email: "email_example", items: [PublicReturnItem(name: "name_example", productId: "productId_example", quantity: 123, reason: "reason_example")], notes: "notes_example", orderNumber: "orderNumber_example") // PublicReturnRequest | 

// Customer requests a return for an order (public, no auth).
PublicReturnsAPI.requestPublicReturn(publicReturnRequest: publicReturnRequest) { (response, error) in
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
 **publicReturnRequest** | [**PublicReturnRequest**](PublicReturnRequest.md) |  | 

### Return type

[**PublicReturnResponse**](PublicReturnResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

