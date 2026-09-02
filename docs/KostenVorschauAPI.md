# KostenVorschauAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**kostenVorschauApi**](KostenVorschauAPI.md#kostenvorschauapi) | **GET** /api/v1/bookkeeping/kosten-vorschau | 


# **kostenVorschauApi**
```swift
    open class func kostenVorschauApi(year: Int, month: Int, completion: @escaping (_ data: KostenVorschau?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 
let month = 987 // Int | 

KostenVorschauAPI.kostenVorschauApi(year: year, month: month) { (response, error) in
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
 **month** | **Int** |  | 

### Return type

[**KostenVorschau**](KostenVorschau.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

