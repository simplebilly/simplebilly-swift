# GewinnverwendungAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gewinnverwendungApi**](GewinnverwendungAPI.md#gewinnverwendungapi) | **GET** /api/v1/bookkeeping/gewinnverwendung | 
[**gewinnverwendungExportApi**](GewinnverwendungAPI.md#gewinnverwendungexportapi) | **GET** /api/v1/bookkeeping/gewinnverwendung/export | 


# **gewinnverwendungApi**
```swift
    open class func gewinnverwendungApi(year: Int, completion: @escaping (_ data: GewinnverwendungsReport?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

GewinnverwendungAPI.gewinnverwendungApi(year: year) { (response, error) in
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

[**GewinnverwendungsReport**](GewinnverwendungsReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gewinnverwendungExportApi**
```swift
    open class func gewinnverwendungExportApi(year: Int, completion: @escaping (_ data: GewinnverwendungsExportResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

GewinnverwendungAPI.gewinnverwendungExportApi(year: year) { (response, error) in
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

[**GewinnverwendungsExportResponse**](GewinnverwendungsExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

