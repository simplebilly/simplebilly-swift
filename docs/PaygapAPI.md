# PaygapAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**paygapAuskunftApi**](PaygapAPI.md#paygapauskunftapi) | **GET** /api/v1/bookkeeping/paygap/auskunft/{employee_id} | 
[**paygapExportApi**](PaygapAPI.md#paygapexportapi) | **GET** /api/v1/bookkeeping/paygap/export | 
[**paygapReportApi**](PaygapAPI.md#paygapreportapi) | **GET** /api/v1/bookkeeping/paygap/report | 


# **paygapAuskunftApi**
```swift
    open class func paygapAuskunftApi(employeeId: UUID, completion: @escaping (_ data: PayGapInfoResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let employeeId = 987 // UUID | 

PaygapAPI.paygapAuskunftApi(employeeId: employeeId) { (response, error) in
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
 **employeeId** | **UUID** |  | 

### Return type

[**PayGapInfoResponse**](PayGapInfoResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paygapExportApi**
```swift
    open class func paygapExportApi(completion: @escaping (_ data: PayGapExportResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


PaygapAPI.paygapExportApi() { (response, error) in
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

[**PayGapExportResponse**](PayGapExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paygapReportApi**
```swift
    open class func paygapReportApi(completion: @escaping (_ data: PayGapReport?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


PaygapAPI.paygapReportApi() { (response, error) in
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

[**PayGapReport**](PayGapReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

