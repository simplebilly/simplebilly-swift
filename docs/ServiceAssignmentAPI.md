# ServiceAssignmentAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createServiceAssignment**](ServiceAssignmentAPI.md#createserviceassignment) | **POST** /api/v1/service-assignments | 
[**deleteServiceAssignment**](ServiceAssignmentAPI.md#deleteserviceassignment) | **DELETE** /api/v1/service-assignments/{id} | 
[**getServiceAssignment**](ServiceAssignmentAPI.md#getserviceassignment) | **GET** /api/v1/service-assignments/{id} | 
[**getServiceAssignments**](ServiceAssignmentAPI.md#getserviceassignments) | **GET** /api/v1/service-assignments/ | 
[**updateServiceAssignment**](ServiceAssignmentAPI.md#updateserviceassignment) | **PUT** /api/v1/service-assignments/{id} | 


# **createServiceAssignment**
```swift
    open class func createServiceAssignment(serviceAssignmentCreate: ServiceAssignmentCreate, completion: @escaping (_ data: ServiceAssignment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let serviceAssignmentCreate = ServiceAssignmentCreate(employeeId: 123, jobId: 123, notes: "notes_example", scheduledDate: Date(), scheduledEnd: "scheduledEnd_example", scheduledStart: "scheduledStart_example", status: ServiceAssignmentStatus()) // ServiceAssignmentCreate | 

ServiceAssignmentAPI.createServiceAssignment(serviceAssignmentCreate: serviceAssignmentCreate) { (response, error) in
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
 **serviceAssignmentCreate** | [**ServiceAssignmentCreate**](ServiceAssignmentCreate.md) |  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteServiceAssignment**
```swift
    open class func deleteServiceAssignment(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ServiceAssignmentAPI.deleteServiceAssignment(id: id) { (response, error) in
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

# **getServiceAssignment**
```swift
    open class func getServiceAssignment(id: UUID, completion: @escaping (_ data: ServiceAssignment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ServiceAssignmentAPI.getServiceAssignment(id: id) { (response, error) in
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

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getServiceAssignments**
```swift
    open class func getServiceAssignments(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [ServiceAssignment]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

ServiceAssignmentAPI.getServiceAssignments(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[ServiceAssignment]**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateServiceAssignment**
```swift
    open class func updateServiceAssignment(id: UUID, serviceAssignmentUpdate: ServiceAssignmentUpdate, completion: @escaping (_ data: ServiceAssignment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let serviceAssignmentUpdate = ServiceAssignmentUpdate(employeeId: 123, jobId: 123, notes: "notes_example", scheduledDate: Date(), scheduledEnd: "scheduledEnd_example", scheduledStart: "scheduledStart_example", status: ServiceAssignmentStatus()) // ServiceAssignmentUpdate | 

ServiceAssignmentAPI.updateServiceAssignment(id: id, serviceAssignmentUpdate: serviceAssignmentUpdate) { (response, error) in
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
 **serviceAssignmentUpdate** | [**ServiceAssignmentUpdate**](ServiceAssignmentUpdate.md) |  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

