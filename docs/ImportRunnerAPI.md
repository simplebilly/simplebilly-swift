# ImportRunnerAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getImportStatus**](ImportRunnerAPI.md#getimportstatus) | **GET** /api/v1/import/{job_id} | 
[**startImport**](ImportRunnerAPI.md#startimport) | **POST** /api/v1/import/start | 
[**testImportConnection**](ImportRunnerAPI.md#testimportconnection) | **POST** /api/v1/import/test | 


# **getImportStatus**
```swift
    open class func getImportStatus(jobId: String, completion: @escaping (_ data: ImportJobStatus?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let jobId = "jobId_example" // String | 

ImportRunnerAPI.getImportStatus(jobId: jobId) { (response, error) in
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
 **jobId** | **String** |  | 

### Return type

[**ImportJobStatus**](ImportJobStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **startImport**
```swift
    open class func startImport(importStartRequest: ImportStartRequest, completion: @escaping (_ data: ImportStartResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let importStartRequest = ImportStartRequest(apiKey: "apiKey_example", provider: "provider_example", years: [123]) // ImportStartRequest | 

ImportRunnerAPI.startImport(importStartRequest: importStartRequest) { (response, error) in
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
 **importStartRequest** | [**ImportStartRequest**](ImportStartRequest.md) |  | 

### Return type

[**ImportStartResponse**](ImportStartResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **testImportConnection**
```swift
    open class func testImportConnection(importTestRequest: ImportTestRequest, completion: @escaping (_ data: ImportTestResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let importTestRequest = ImportTestRequest(apiKey: "apiKey_example", provider: "provider_example") // ImportTestRequest | 

ImportRunnerAPI.testImportConnection(importTestRequest: importTestRequest) { (response, error) in
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
 **importTestRequest** | [**ImportTestRequest**](ImportTestRequest.md) |  | 

### Return type

[**ImportTestResponse**](ImportTestResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

