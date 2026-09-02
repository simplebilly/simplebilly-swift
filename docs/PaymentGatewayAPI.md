# PaymentGatewayAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPaymentGatewayApi**](PaymentGatewayAPI.md#createpaymentgatewayapi) | **POST** /api/v1/payment-gateways | 
[**deletePaymentGatewayApi**](PaymentGatewayAPI.md#deletepaymentgatewayapi) | **DELETE** /api/v1/payment-gateways/{gateway_id} | 
[**listPaymentGatewaysApi**](PaymentGatewayAPI.md#listpaymentgatewaysapi) | **GET** /api/v1/payment-gateways/ | 
[**oauthAuthorizeApi**](PaymentGatewayAPI.md#oauthauthorizeapi) | **POST** /api/v1/payment-gateways/oauth/authorize | 
[**oauthCallbackApi**](PaymentGatewayAPI.md#oauthcallbackapi) | **POST** /api/v1/payment-gateways/oauth/callback | 
[**updatePaymentGatewayApi**](PaymentGatewayAPI.md#updatepaymentgatewayapi) | **PUT** /api/v1/payment-gateways/{gateway_id} | 


# **createPaymentGatewayApi**
```swift
    open class func createPaymentGatewayApi(body: AnyCodable, completion: @escaping (_ data: PaymentGateway?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let body =  // AnyCodable | 

PaymentGatewayAPI.createPaymentGatewayApi(body: body) { (response, error) in
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
 **body** | **AnyCodable** |  | 

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePaymentGatewayApi**
```swift
    open class func deletePaymentGatewayApi(gatewayId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let gatewayId = "gatewayId_example" // String | 

PaymentGatewayAPI.deletePaymentGatewayApi(gatewayId: gatewayId) { (response, error) in
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
 **gatewayId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPaymentGatewaysApi**
```swift
    open class func listPaymentGatewaysApi(completion: @escaping (_ data: [PaymentGateway]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


PaymentGatewayAPI.listPaymentGatewaysApi() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

[**[PaymentGateway]**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauthAuthorizeApi**
```swift
    open class func oauthAuthorizeApi(gatewayOAuthAuthorizeRequest: GatewayOAuthAuthorizeRequest, completion: @escaping (_ data: GatewayOAuthAuthorizeResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let gatewayOAuthAuthorizeRequest = GatewayOAuthAuthorizeRequest(gatewayType: "gatewayType_example", redirectUri: "redirectUri_example") // GatewayOAuthAuthorizeRequest | 

PaymentGatewayAPI.oauthAuthorizeApi(gatewayOAuthAuthorizeRequest: gatewayOAuthAuthorizeRequest) { (response, error) in
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
 **gatewayOAuthAuthorizeRequest** | [**GatewayOAuthAuthorizeRequest**](GatewayOAuthAuthorizeRequest.md) |  | 

### Return type

[**GatewayOAuthAuthorizeResponse**](GatewayOAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauthCallbackApi**
```swift
    open class func oauthCallbackApi(gatewayOAuthCallbackRequest: GatewayOAuthCallbackRequest, completion: @escaping (_ data: PaymentGateway?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let gatewayOAuthCallbackRequest = GatewayOAuthCallbackRequest(code: "code_example", gatewayType: "gatewayType_example", redirectUri: "redirectUri_example", state: "state_example") // GatewayOAuthCallbackRequest | 

PaymentGatewayAPI.oauthCallbackApi(gatewayOAuthCallbackRequest: gatewayOAuthCallbackRequest) { (response, error) in
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
 **gatewayOAuthCallbackRequest** | [**GatewayOAuthCallbackRequest**](GatewayOAuthCallbackRequest.md) |  | 

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePaymentGatewayApi**
```swift
    open class func updatePaymentGatewayApi(gatewayId: String, body: AnyCodable, completion: @escaping (_ data: PaymentGateway?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let gatewayId = "gatewayId_example" // String | 
let body =  // AnyCodable | 

PaymentGatewayAPI.updatePaymentGatewayApi(gatewayId: gatewayId, body: body) { (response, error) in
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
 **gatewayId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

