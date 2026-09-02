# ServiceJobAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createServiceJob**](ServiceJobAPI.md#createservicejob) | **POST** /api/v1/service-jobs | 
[**deleteServiceJob**](ServiceJobAPI.md#deleteservicejob) | **DELETE** /api/v1/service-jobs/{id} | 
[**getServiceJob**](ServiceJobAPI.md#getservicejob) | **GET** /api/v1/service-jobs/{id} | 
[**getServiceJobs**](ServiceJobAPI.md#getservicejobs) | **GET** /api/v1/service-jobs/ | 
[**updateServiceJob**](ServiceJobAPI.md#updateservicejob) | **PUT** /api/v1/service-jobs/{id} | 


# **createServiceJob**
```swift
    open class func createServiceJob(serviceJobCreate: ServiceJobCreate, completion: @escaping (_ data: ServiceJob?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let serviceJobCreate = ServiceJobCreate(address: "address_example", customerEmail: "customerEmail_example", customerId: 123, customerName: "customerName_example", customerPhone: "customerPhone_example", description: "description_example", estimatedDurationMinutes: 123, lat: 123, lng: 123, notes: "notes_example", status: ServiceJobStatus()) // ServiceJobCreate | 

ServiceJobAPI.createServiceJob(serviceJobCreate: serviceJobCreate) { (response, error) in
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
 **serviceJobCreate** | [**ServiceJobCreate**](ServiceJobCreate.md) |  | 

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteServiceJob**
```swift
    open class func deleteServiceJob(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ServiceJobAPI.deleteServiceJob(id: id) { (response, error) in
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

# **getServiceJob**
```swift
    open class func getServiceJob(id: UUID, completion: @escaping (_ data: ServiceJob?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ServiceJobAPI.getServiceJob(id: id) { (response, error) in
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

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getServiceJobs**
```swift
    open class func getServiceJobs(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [ServiceJob]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

ServiceJobAPI.getServiceJobs(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[ServiceJob]**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateServiceJob**
```swift
    open class func updateServiceJob(id: UUID, serviceJobUpdate: ServiceJobUpdate, completion: @escaping (_ data: ServiceJob?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let serviceJobUpdate = ServiceJobUpdate(address: "address_example", customerEmail: "customerEmail_example", customerId: 123, customerName: "customerName_example", customerPhone: "customerPhone_example", description: "description_example", estimatedDurationMinutes: 123, lat: 123, lng: 123, notes: "notes_example", status: ServiceJobStatus()) // ServiceJobUpdate | 

ServiceJobAPI.updateServiceJob(id: id, serviceJobUpdate: serviceJobUpdate) { (response, error) in
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
 **serviceJobUpdate** | [**ServiceJobUpdate**](ServiceJobUpdate.md) |  | 

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

