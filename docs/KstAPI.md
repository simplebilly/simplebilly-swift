# KstAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**kstApi**](KstAPI.md#kstapi) | **GET** /api/v1/bookkeeping/kst | 


# **kstApi**
```swift
    open class func kstApi(year: Int, gewinn: String? = nil, completion: @escaping (_ data: KstErgebnis?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 
let gewinn = "gewinn_example" // String |  (optional)

KstAPI.kstApi(year: year, gewinn: gewinn) { (response, error) in
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
 **gewinn** | **String** |  | [optional] 

### Return type

[**KstErgebnis**](KstErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

