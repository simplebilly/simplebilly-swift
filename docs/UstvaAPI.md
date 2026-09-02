# UstvaAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**jahresustApi**](UstvaAPI.md#jahresustapi) | **GET** /api/v1/bookkeeping/jahresust | 
[**ustvaApi**](UstvaAPI.md#ustvaapi) | **GET** /api/v1/bookkeeping/ustva | 


# **jahresustApi**
```swift
    open class func jahresustApi(year: Int, completion: @escaping (_ data: JahresUstErgebnis?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

UstvaAPI.jahresustApi(year: year) { (response, error) in
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

### Return type

[**JahresUstErgebnis**](JahresUstErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ustvaApi**
```swift
    open class func ustvaApi(zeitraum: String, completion: @escaping (_ data: UstvaErgebnis?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let zeitraum = "zeitraum_example" // String | 

UstvaAPI.ustvaApi(zeitraum: zeitraum) { (response, error) in
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
 **zeitraum** | **String** |  | 

### Return type

[**UstvaErgebnis**](UstvaErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

