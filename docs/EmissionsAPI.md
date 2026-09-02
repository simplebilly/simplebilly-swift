# EmissionsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createEmissionEntryApi**](EmissionsAPI.md#createemissionentryapi) | **POST** /api/v1/bookkeeping/emissions/entries | 
[**createEmissionTargetApi**](EmissionsAPI.md#createemissiontargetapi) | **POST** /api/v1/bookkeeping/emissions/targets | 
[**deleteEmissionEntryApi**](EmissionsAPI.md#deleteemissionentryapi) | **DELETE** /api/v1/bookkeeping/emissions/entries/{id} | 
[**deleteEmissionTargetApi**](EmissionsAPI.md#deleteemissiontargetapi) | **DELETE** /api/v1/bookkeeping/emissions/targets/{id} | 
[**emissionsEntriesApi**](EmissionsAPI.md#emissionsentriesapi) | **GET** /api/v1/bookkeeping/emissions/entries | 
[**emissionsExportApi**](EmissionsAPI.md#emissionsexportapi) | **GET** /api/v1/bookkeeping/emissions/export | 
[**emissionsFactorsApi**](EmissionsAPI.md#emissionsfactorsapi) | **GET** /api/v1/bookkeeping/emissions/factors | 
[**emissionsReportApi**](EmissionsAPI.md#emissionsreportapi) | **GET** /api/v1/bookkeeping/emissions/report | 
[**emissionsTargetsApi**](EmissionsAPI.md#emissionstargetsapi) | **GET** /api/v1/bookkeeping/emissions/targets | 


# **createEmissionEntryApi**
```swift
    open class func createEmissionEntryApi(createEmissionEntry: CreateEmissionEntry, completion: @escaping (_ data: EmissionEntry?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let createEmissionEntry = CreateEmissionEntry(activityValue: "activityValue_example", categoryId: "categoryId_example", description: "description_example", method: "method_example", scope: "scope_example", unit: "unit_example", year: 123) // CreateEmissionEntry | 

EmissionsAPI.createEmissionEntryApi(createEmissionEntry: createEmissionEntry) { (response, error) in
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
 **createEmissionEntry** | [**CreateEmissionEntry**](CreateEmissionEntry.md) |  | 

### Return type

[**EmissionEntry**](EmissionEntry.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createEmissionTargetApi**
```swift
    open class func createEmissionTargetApi(createEmissionTarget: CreateEmissionTarget, completion: @escaping (_ data: EmissionTarget?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let createEmissionTarget = CreateEmissionTarget(baseValue: "baseValue_example", baseYear: 123, description: "description_example", scope: "scope_example", targetValue: "targetValue_example", targetYear: 123) // CreateEmissionTarget | 

EmissionsAPI.createEmissionTargetApi(createEmissionTarget: createEmissionTarget) { (response, error) in
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
 **createEmissionTarget** | [**CreateEmissionTarget**](CreateEmissionTarget.md) |  | 

### Return type

[**EmissionTarget**](EmissionTarget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteEmissionEntryApi**
```swift
    open class func deleteEmissionEntryApi(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

EmissionsAPI.deleteEmissionEntryApi(id: id) { (response, error) in
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
 **id** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteEmissionTargetApi**
```swift
    open class func deleteEmissionTargetApi(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

EmissionsAPI.deleteEmissionTargetApi(id: id) { (response, error) in
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
 **id** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissionsEntriesApi**
```swift
    open class func emissionsEntriesApi(year: Int, completion: @escaping (_ data: [EmissionEntry]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

EmissionsAPI.emissionsEntriesApi(year: year) { (response, error) in
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

[**[EmissionEntry]**](EmissionEntry.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissionsExportApi**
```swift
    open class func emissionsExportApi(year: Int, completion: @escaping (_ data: EmissionsExportResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

EmissionsAPI.emissionsExportApi(year: year) { (response, error) in
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

[**EmissionsExportResponse**](EmissionsExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissionsFactorsApi**
```swift
    open class func emissionsFactorsApi(completion: @escaping (_ data: [EmissionFactorResponse]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


EmissionsAPI.emissionsFactorsApi() { (response, error) in
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

[**[EmissionFactorResponse]**](EmissionFactorResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissionsReportApi**
```swift
    open class func emissionsReportApi(year: Int, completion: @escaping (_ data: EmissionsReport?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

EmissionsAPI.emissionsReportApi(year: year) { (response, error) in
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

[**EmissionsReport**](EmissionsReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissionsTargetsApi**
```swift
    open class func emissionsTargetsApi(completion: @escaping (_ data: [EmissionTarget]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


EmissionsAPI.emissionsTargetsApi() { (response, error) in
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

[**[EmissionTarget]**](EmissionTarget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

