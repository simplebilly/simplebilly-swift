# PlausibilityAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**plausibilityCheckApi**](PlausibilityAPI.md#plausibilitycheckapi) | **GET** /api/v1/bookkeeping/plausibility | 


# **plausibilityCheckApi**
```swift
    open class func plausibilityCheckApi(dateFrom: String? = nil, dateTo: String? = nil, completion: @escaping (_ data: PlausibilityReport?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)

PlausibilityAPI.plausibilityCheckApi(dateFrom: dateFrom, dateTo: dateTo) { (response, error) in
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
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 

### Return type

[**PlausibilityReport**](PlausibilityReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

