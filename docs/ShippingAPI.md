# ShippingAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCredentialsApi**](ShippingAPI.md#getcredentialsapi) | **GET** /api/v1/shipping/credentials | 
[**getRatesApi**](ShippingAPI.md#getratesapi) | **POST** /api/v1/shipping/rates | 
[**listProvidersApi**](ShippingAPI.md#listprovidersapi) | **GET** /api/v1/shipping/providers | 
[**saveCredentialsApi**](ShippingAPI.md#savecredentialsapi) | **PUT** /api/v1/shipping/credentials | 


# **getCredentialsApi**
```swift
    open class func getCredentialsApi(completion: @escaping (_ data: ShippingCredentials?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


ShippingAPI.getCredentialsApi() { (response, error) in
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

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRatesApi**
```swift
    open class func getRatesApi(rateRequest: RateRequest, completion: @escaping (_ data: RateResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let rateRequest = RateRequest(customer: CustomerInfo(annualVolume: 123, isRegistered: false), packages: [Package(description: "description_example", heightCm: 123, lengthCm: 123, reference: "reference_example", weightKg: 123, widthCm: 123)], recipient: Address(city: "city_example", company: "company_example", country: "country_example", email: "email_example", name: "name_example", phone: "phone_example", street: "street_example", streetNumber: "streetNumber_example", zip: "zip_example"), sender: nil) // RateRequest | 

ShippingAPI.getRatesApi(rateRequest: rateRequest) { (response, error) in
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
 **rateRequest** | [**RateRequest**](RateRequest.md) |  | 

### Return type

[**RateResponse**](RateResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProvidersApi**
```swift
    open class func listProvidersApi(completion: @escaping (_ data: [ProviderInfo]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


ShippingAPI.listProvidersApi() { (response, error) in
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

[**[ProviderInfo]**](ProviderInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **saveCredentialsApi**
```swift
    open class func saveCredentialsApi(shippingCredentials: ShippingCredentials, completion: @escaping (_ data: ShippingCredentials?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shippingCredentials = ShippingCredentials(dhl: DhlCredentials(apiKey: "apiKey_example", clientId: "clientId_example", clientSecret: "clientSecret_example"), ups: UpsCredentials(clientId: "clientId_example", clientSecret: "clientSecret_example", shipperNumber: "shipperNumber_example")) // ShippingCredentials | 

ShippingAPI.saveCredentialsApi(shippingCredentials: shippingCredentials) { (response, error) in
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
 **shippingCredentials** | [**ShippingCredentials**](ShippingCredentials.md) |  | 

### Return type

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

