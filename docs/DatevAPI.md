# DatevAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**datevExportApi**](DatevAPI.md#datevexportapi) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV
[**datevPreviewApi**](DatevAPI.md#datevpreviewapi) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review


# **datevExportApi**
```swift
    open class func datevExportApi(accountSchema: String? = nil, dateFrom: String? = nil, dateTo: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: DatevExportResponse?, _ error: Error?) -> Void)
```

Export bookkeeping data as DATEV CSV

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let accountSchema = "accountSchema_example" // String |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

// Export bookkeeping data as DATEV CSV
DatevAPI.datevExportApi(accountSchema: accountSchema, dateFrom: dateFrom, dateTo: dateTo, page: page, pageSize: pageSize) { (response, error) in
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
 **accountSchema** | **String** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**DatevExportResponse**](DatevExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **datevPreviewApi**
```swift
    open class func datevPreviewApi(accountSchema: String? = nil, dateFrom: String? = nil, dateTo: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: [DatevBookingPreview]?, _ error: Error?) -> Void)
```

Exported_datev_bookings: returns formed bookings for review

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let accountSchema = "accountSchema_example" // String |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

// Exported_datev_bookings: returns formed bookings for review
DatevAPI.datevPreviewApi(accountSchema: accountSchema, dateFrom: dateFrom, dateTo: dateTo, page: page, pageSize: pageSize) { (response, error) in
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
 **accountSchema** | **String** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**[DatevBookingPreview]**](DatevBookingPreview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

