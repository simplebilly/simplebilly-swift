# SuitabilityAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**shippingSuitabilityApi**](SuitabilityAPI.md#shippingsuitabilityapi) | **POST** /api/v1/shipping/suitability | 


# **shippingSuitabilityApi**
```swift
    open class func shippingSuitabilityApi(suitabilityRequest: SuitabilityRequest, completion: @escaping (_ data: SuitabilityResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let suitabilityRequest = SuitabilityRequest(customerAnnualVolume: 123, items: [CartItemInput(productId: 123, quantity: 123)], recipient: Address(city: "city_example", company: "company_example", country: "country_example", email: "email_example", name: "name_example", phone: "phone_example", street: "street_example", streetNumber: "streetNumber_example", zip: "zip_example"), sender: nil) // SuitabilityRequest | 

SuitabilityAPI.shippingSuitabilityApi(suitabilityRequest: suitabilityRequest) { (response, error) in
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
 **suitabilityRequest** | [**SuitabilityRequest**](SuitabilityRequest.md) |  | 

### Return type

[**SuitabilityResult**](SuitabilityResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

