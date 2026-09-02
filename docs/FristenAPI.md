# FristenAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fristenApi**](FristenAPI.md#fristenapi) | **GET** /api/v1/bookkeeping/fristen | 


# **fristenApi**
```swift
    open class func fristenApi(bundesland: String? = nil, voranmeldungsrhythmus: String? = nil, dauerfristverlaengerung: Bool? = nil, estAktiv: Bool? = nil, gewstAktiv: Bool? = nil, monate: Int? = nil, completion: @escaping (_ data: FristenErgebnis?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let bundesland = "bundesland_example" // String |  (optional)
let voranmeldungsrhythmus = "voranmeldungsrhythmus_example" // String |  (optional)
let dauerfristverlaengerung = true // Bool |  (optional)
let estAktiv = true // Bool |  (optional)
let gewstAktiv = true // Bool |  (optional)
let monate = 987 // Int |  (optional)

FristenAPI.fristenApi(bundesland: bundesland, voranmeldungsrhythmus: voranmeldungsrhythmus, dauerfristverlaengerung: dauerfristverlaengerung, estAktiv: estAktiv, gewstAktiv: gewstAktiv, monate: monate) { (response, error) in
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
 **bundesland** | **String** |  | [optional] 
 **voranmeldungsrhythmus** | **String** |  | [optional] 
 **dauerfristverlaengerung** | **Bool** |  | [optional] 
 **estAktiv** | **Bool** |  | [optional] 
 **gewstAktiv** | **Bool** |  | [optional] 
 **monate** | **Int** |  | [optional] 

### Return type

[**FristenErgebnis**](FristenErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

