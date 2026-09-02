# ReportsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bilanzReportApi**](ReportsAPI.md#bilanzreportapi) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet)
[**guvReportApi**](ReportsAPI.md#guvreportapi) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement)
[**kontenansichtReportApi**](ReportsAPI.md#kontenansichtreportapi) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview)
[**umsatzsteuerReportApi**](ReportsAPI.md#umsatzsteuerreportapi) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report)


# **bilanzReportApi**
```swift
    open class func bilanzReportApi(year: Int? = nil, month: Int? = nil, dateFrom: String? = nil, dateTo: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: BilanzReport?, _ error: Error?) -> Void)
```

Bilanz (Balance Sheet)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let month = 987 // Int |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

// Bilanz (Balance Sheet)
ReportsAPI.bilanzReportApi(year: year, month: month, dateFrom: dateFrom, dateTo: dateTo, page: page, pageSize: pageSize) { (response, error) in
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
 **month** | **Int** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**BilanzReport**](BilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **guvReportApi**
```swift
    open class func guvReportApi(year: Int? = nil, month: Int? = nil, dateFrom: String? = nil, dateTo: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: GuVReport?, _ error: Error?) -> Void)
```

Gewinn- und Verlustrechnung (P&L statement)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let month = 987 // Int |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

// Gewinn- und Verlustrechnung (P&L statement)
ReportsAPI.guvReportApi(year: year, month: month, dateFrom: dateFrom, dateTo: dateTo, page: page, pageSize: pageSize) { (response, error) in
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
 **month** | **Int** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**GuVReport**](GuVReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **kontenansichtReportApi**
```swift
    open class func kontenansichtReportApi(year: Int? = nil, month: Int? = nil, dateFrom: String? = nil, dateTo: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: KontoReport?, _ error: Error?) -> Void)
```

Kontenansicht (Account Overview)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let month = 987 // Int |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

// Kontenansicht (Account Overview)
ReportsAPI.kontenansichtReportApi(year: year, month: month, dateFrom: dateFrom, dateTo: dateTo, page: page, pageSize: pageSize) { (response, error) in
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
 **month** | **Int** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**KontoReport**](KontoReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **umsatzsteuerReportApi**
```swift
    open class func umsatzsteuerReportApi(year: Int? = nil, month: Int? = nil, dateFrom: String? = nil, dateTo: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: UmsatzsteuerReport?, _ error: Error?) -> Void)
```

Umsatzsteuer-Voranmeldung (VAT report)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let month = 987 // Int |  (optional)
let dateFrom = "dateFrom_example" // String |  (optional)
let dateTo = "dateTo_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

// Umsatzsteuer-Voranmeldung (VAT report)
ReportsAPI.umsatzsteuerReportApi(year: year, month: month, dateFrom: dateFrom, dateTo: dateTo, page: page, pageSize: pageSize) { (response, error) in
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
 **month** | **Int** |  | [optional] 
 **dateFrom** | **String** |  | [optional] 
 **dateTo** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**UmsatzsteuerReport**](UmsatzsteuerReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

