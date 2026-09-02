# GobdExportAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**buchhalterCsvApi**](GobdExportAPI.md#buchhaltercsvapi) | **GET** /api/v1/bookkeeping/buchhalter-csv | 
[**gobdExportApi**](GobdExportAPI.md#gobdexportapi) | **GET** /api/v1/bookkeeping/gobd | GoBD/GDPdU export. Default: ZIP archive (&#x60;index.xml&#x60; + CSV tables, IDEA format). &#x60;?format&#x3D;csv&#x60; returns the legacy single-journal CSV as JSON.


# **buchhalterCsvApi**
```swift
    open class func buchhalterCsvApi(dateFrom: String, dateTo: String, completion: @escaping (_ data: GoBDExportResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let dateFrom = "dateFrom_example" // String | 
let dateTo = "dateTo_example" // String | 

GobdExportAPI.buchhalterCsvApi(dateFrom: dateFrom, dateTo: dateTo) { (response, error) in
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
 **dateFrom** | **String** |  | 
 **dateTo** | **String** |  | 

### Return type

[**GoBDExportResponse**](GoBDExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gobdExportApi**
```swift
    open class func gobdExportApi(year: Int, format: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 
let format = "format_example" // String | Export format: `zip` (default, full GDPdU/IDEA export) or `csv` (legacy single-journal CSV as JSON). (optional)

// GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.
GobdExportAPI.gobdExportApi(year: year, format: format) { (response, error) in
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
 **format** | **String** | Export format: &#x60;zip&#x60; (default, full GDPdU/IDEA export) or &#x60;csv&#x60; (legacy single-journal CSV as JSON). | [optional] 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

