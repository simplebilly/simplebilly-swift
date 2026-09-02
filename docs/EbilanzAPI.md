# EbilanzAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ebilanzReportApi**](EbilanzAPI.md#ebilanzreportapi) | **GET** /api/v1/bookkeeping/ebilanz | 
[**ebilanzXbrlExportApi**](EbilanzAPI.md#ebilanzxbrlexportapi) | **GET** /api/v1/bookkeeping/ebilanz/xbrl | 


# **ebilanzReportApi**
```swift
    open class func ebilanzReportApi(year: Int? = nil, dateFrom: String? = nil, dateTo: String? = nil, completion: @escaping (_ data: EBilanzReport?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)

EbilanzAPI.ebilanzReportApi(year: year, dateFrom: dateFrom, dateTo: dateTo) { (response, error) in
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
 **year** | **Int** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 

### Return type

[**EBilanzReport**](EBilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebilanzXbrlExportApi**
```swift
    open class func ebilanzXbrlExportApi(year: Int? = nil, dateFrom: String? = nil, dateTo: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)

EbilanzAPI.ebilanzXbrlExportApi(year: year, dateFrom: dateFrom, dateTo: dateTo) { (response, error) in
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
 **year** | **Int** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

