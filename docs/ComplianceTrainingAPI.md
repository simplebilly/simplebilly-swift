# ComplianceTrainingAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createComplianceTraining**](ComplianceTrainingAPI.md#createcompliancetraining) | **POST** /api/v1/compliance-trainings | 
[**deleteComplianceTraining**](ComplianceTrainingAPI.md#deletecompliancetraining) | **DELETE** /api/v1/compliance-trainings/{id} | 
[**getComplianceTraining**](ComplianceTrainingAPI.md#getcompliancetraining) | **GET** /api/v1/compliance-trainings/{id} | 
[**getComplianceTrainings**](ComplianceTrainingAPI.md#getcompliancetrainings) | **GET** /api/v1/compliance-trainings/ | 
[**updateComplianceTraining**](ComplianceTrainingAPI.md#updatecompliancetraining) | **PUT** /api/v1/compliance-trainings/{id} | 


# **createComplianceTraining**
```swift
    open class func createComplianceTraining(complianceTrainingCreate: ComplianceTrainingCreate, completion: @escaping (_ data: ComplianceTraining?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let complianceTrainingCreate = ComplianceTrainingCreate(assignable: false, code: "code_example", description: "description_example", passScore: 123, pluginPlatform: "pluginPlatform_example", source: TrainingSource(), title: "title_example", validityMonths: 123) // ComplianceTrainingCreate | 

ComplianceTrainingAPI.createComplianceTraining(complianceTrainingCreate: complianceTrainingCreate) { (response, error) in
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
 **complianceTrainingCreate** | [**ComplianceTrainingCreate**](ComplianceTrainingCreate.md) |  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteComplianceTraining**
```swift
    open class func deleteComplianceTraining(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ComplianceTrainingAPI.deleteComplianceTraining(id: id) { (response, error) in
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

# **getComplianceTraining**
```swift
    open class func getComplianceTraining(id: UUID, completion: @escaping (_ data: ComplianceTraining?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ComplianceTrainingAPI.getComplianceTraining(id: id) { (response, error) in
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

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getComplianceTrainings**
```swift
    open class func getComplianceTrainings(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [ComplianceTraining]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

ComplianceTrainingAPI.getComplianceTrainings(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 
 **search** | **String** |  | [optional] 
 **includeDeleted** | **Bool** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**[ComplianceTraining]**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateComplianceTraining**
```swift
    open class func updateComplianceTraining(id: UUID, complianceTrainingUpdate: ComplianceTrainingUpdate, completion: @escaping (_ data: ComplianceTraining?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let complianceTrainingUpdate = ComplianceTrainingUpdate(assignable: false, code: "code_example", description: "description_example", passScore: 123, pluginPlatform: "pluginPlatform_example", source: TrainingSource(), title: "title_example", validityMonths: 123) // ComplianceTrainingUpdate | 

ComplianceTrainingAPI.updateComplianceTraining(id: id, complianceTrainingUpdate: complianceTrainingUpdate) { (response, error) in
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
 **complianceTrainingUpdate** | [**ComplianceTrainingUpdate**](ComplianceTrainingUpdate.md) |  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

