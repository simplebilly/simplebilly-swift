# BankingAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bankLookupApi**](BankingAPI.md#banklookupapi) | **GET** /api/v1/bookkeeping/banking/lookup | 
[**bankTransactionsApi**](BankingAPI.md#banktransactionsapi) | **GET** /api/v1/bookkeeping/banking/transactions | 
[**hebesatzLookupApi**](BankingAPI.md#hebesatzlookupapi) | **GET** /api/v1/bookkeeping/hebesatz | 


# **bankLookupApi**
```swift
    open class func bankLookupApi(iban: String, completion: @escaping (_ data: BankLookup?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let iban = "iban_example" // String | 

BankingAPI.bankLookupApi(iban: iban) { (response, error) in
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
 **iban** | **String** |  | 

### Return type

[**BankLookup**](BankLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bankTransactionsApi**
```swift
    open class func bankTransactionsApi(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


BankingAPI.bankTransactionsApi() { (response, error) in
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

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **hebesatzLookupApi**
```swift
    open class func hebesatzLookupApi(gemeindeschluessel: String? = nil, plz: String? = nil, name: String? = nil, stichtag: String? = nil, countryCode: String? = nil, completion: @escaping (_ data: [HebesatzLookup]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let gemeindeschluessel = "gemeindeschluessel_example" // String |  (optional)
let plz = "plz_example" // String |  (optional)
let name = "name_example" // String |  (optional)
let stichtag = "stichtag_example" // String | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from <= date <= valid_to. (optional)
let countryCode = "countryCode_example" // String |  (optional)

BankingAPI.hebesatzLookupApi(gemeindeschluessel: gemeindeschluessel, plz: plz, name: name, stichtag: stichtag, countryCode: countryCode) { (response, error) in
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
 **gemeindeschluessel** | **String** |  | [optional] 
 **plz** | **String** |  | [optional] 
 **name** | **String** |  | [optional] 
 **stichtag** | **String** | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from &lt;&#x3D; date &lt;&#x3D; valid_to. | [optional] 
 **countryCode** | **String** |  | [optional] 

### Return type

[**[HebesatzLookup]**](HebesatzLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

