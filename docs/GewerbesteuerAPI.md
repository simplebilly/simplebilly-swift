# GewerbesteuerAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gewerbesteuerApi**](GewerbesteuerAPI.md#gewerbesteuerapi) | **GET** /api/v1/bookkeeping/gewerbesteuer | 


# **gewerbesteuerApi**
```swift
    open class func gewerbesteuerApi(year: Int, hebesatz: String? = nil, gewerbeertrag: String? = nil, country: String? = nil, gemeindeschluessel: String? = nil, completion: @escaping (_ data: GewerbesteuerErgebnis?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 
let hebesatz = "hebesatz_example" // String |  (optional)
let gewerbeertrag = "gewerbeertrag_example" // String |  (optional)
let country = "country_example" // String |  (optional)
let gemeindeschluessel = "gemeindeschluessel_example" // String |  (optional)

GewerbesteuerAPI.gewerbesteuerApi(year: year, hebesatz: hebesatz, gewerbeertrag: gewerbeertrag, country: country, gemeindeschluessel: gemeindeschluessel) { (response, error) in
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
 **year** | **Int** |  | 
 **hebesatz** | **String** |  | [optional] 
 **gewerbeertrag** | **String** |  | [optional] 
 **country** | **String** |  | [optional] 
 **gemeindeschluessel** | **String** |  | [optional] 

### Return type

[**GewerbesteuerErgebnis**](GewerbesteuerErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

