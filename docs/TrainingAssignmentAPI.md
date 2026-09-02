# TrainingAssignmentAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTrainingAssignment**](TrainingAssignmentAPI.md#createtrainingassignment) | **POST** /api/v1/training-assignments | 
[**deleteTrainingAssignment**](TrainingAssignmentAPI.md#deletetrainingassignment) | **DELETE** /api/v1/training-assignments/{id} | 
[**getTrainingAssignment**](TrainingAssignmentAPI.md#gettrainingassignment) | **GET** /api/v1/training-assignments/{id} | 
[**getTrainingAssignments**](TrainingAssignmentAPI.md#gettrainingassignments) | **GET** /api/v1/training-assignments/ | 
[**updateTrainingAssignment**](TrainingAssignmentAPI.md#updatetrainingassignment) | **PUT** /api/v1/training-assignments/{id} | 


# **createTrainingAssignment**
```swift
    open class func createTrainingAssignment(trainingAssignmentCreate: TrainingAssignmentCreate, completion: @escaping (_ data: TrainingAssignment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let trainingAssignmentCreate = TrainingAssignmentCreate(assignedBy: 123, dueDate: Date(), employeeId: 123, notes: "notes_example", status: AssignmentStatus(), trainingId: 123) // TrainingAssignmentCreate | 

TrainingAssignmentAPI.createTrainingAssignment(trainingAssignmentCreate: trainingAssignmentCreate) { (response, error) in
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
 **trainingAssignmentCreate** | [**TrainingAssignmentCreate**](TrainingAssignmentCreate.md) |  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteTrainingAssignment**
```swift
    open class func deleteTrainingAssignment(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

TrainingAssignmentAPI.deleteTrainingAssignment(id: id) { (response, error) in
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

# **getTrainingAssignment**
```swift
    open class func getTrainingAssignment(id: UUID, completion: @escaping (_ data: TrainingAssignment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

TrainingAssignmentAPI.getTrainingAssignment(id: id) { (response, error) in
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

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTrainingAssignments**
```swift
    open class func getTrainingAssignments(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [TrainingAssignment]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

TrainingAssignmentAPI.getTrainingAssignments(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[TrainingAssignment]**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateTrainingAssignment**
```swift
    open class func updateTrainingAssignment(id: UUID, trainingAssignmentUpdate: TrainingAssignmentUpdate, completion: @escaping (_ data: TrainingAssignment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let trainingAssignmentUpdate = TrainingAssignmentUpdate(assignedBy: 123, dueDate: Date(), employeeId: 123, notes: "notes_example", status: AssignmentStatus(), trainingId: 123) // TrainingAssignmentUpdate | 

TrainingAssignmentAPI.updateTrainingAssignment(id: id, trainingAssignmentUpdate: trainingAssignmentUpdate) { (response, error) in
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
 **trainingAssignmentUpdate** | [**TrainingAssignmentUpdate**](TrainingAssignmentUpdate.md) |  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

