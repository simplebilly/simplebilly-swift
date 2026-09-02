# ActivityAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createActivity**](ActivityAPI.md#createactivity) | **POST** /api/v1/activities | 
[**deleteActivity**](ActivityAPI.md#deleteactivity) | **DELETE** /api/v1/activities/{activity_id} | 
[**getActivity**](ActivityAPI.md#getactivity) | **GET** /api/v1/activities/{activity_id} | 
[**listActivities**](ActivityAPI.md#listactivities) | **GET** /api/v1/activities/ | 
[**updateActivity**](ActivityAPI.md#updateactivity) | **PUT** /api/v1/activities/{activity_id} | 
[**updateActivityStatus**](ActivityAPI.md#updateactivitystatus) | **PUT** /api/v1/activities/{activity_id}/status | 


# **createActivity**
```swift
    open class func createActivity(activity: Activity, completion: @escaping (_ data: Activity?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let activity = Activity(activityType: ActivityType(), assignedTo: "assignedTo_example", contactId: "contactId_example", description: "description_example", dueDate: Date(), reminderDate: Date(), status: ActivityStatus(), subject: "subject_example") // Activity | 

ActivityAPI.createActivity(activity: activity) { (response, error) in
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
 **activity** | [**Activity**](Activity.md) |  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteActivity**
```swift
    open class func deleteActivity(activityId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let activityId = "activityId_example" // String | 

ActivityAPI.deleteActivity(activityId: activityId) { (response, error) in
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
 **activityId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getActivity**
```swift
    open class func getActivity(activityId: String, completion: @escaping (_ data: Activity?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let activityId = "activityId_example" // String | 

ActivityAPI.getActivity(activityId: activityId) { (response, error) in
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
 **activityId** | **String** |  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listActivities**
```swift
    open class func listActivities(page: Int? = nil, pageSize: Int? = nil, contactId: String? = nil, activityType: String? = nil, status: String? = nil, assignedTo: String? = nil, overdueOnly: Bool? = nil, completion: @escaping (_ data: [Activity]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let contactId = "contactId_example" // String |  (optional)
let activityType = "activityType_example" // String |  (optional)
let status = "status_example" // String |  (optional)
let assignedTo = "assignedTo_example" // String |  (optional)
let overdueOnly = true // Bool | Only show overdue follow-ups. (optional)

ActivityAPI.listActivities(page: page, pageSize: pageSize, contactId: contactId, activityType: activityType, status: status, assignedTo: assignedTo, overdueOnly: overdueOnly) { (response, error) in
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
 **contactId** | **String** |  | [optional] 
 **activityType** | **String** |  | [optional] 
 **status** | **String** |  | [optional] 
 **assignedTo** | **String** |  | [optional] 
 **overdueOnly** | **Bool** | Only show overdue follow-ups. | [optional] 

### Return type

[**[Activity]**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateActivity**
```swift
    open class func updateActivity(activityId: String, body: AnyCodable, completion: @escaping (_ data: Activity?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let activityId = "activityId_example" // String | 
let body =  // AnyCodable | 

ActivityAPI.updateActivity(activityId: activityId, body: body) { (response, error) in
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
 **activityId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateActivityStatus**
```swift
    open class func updateActivityStatus(activityId: String, activityStatusUpdate: ActivityStatusUpdate, completion: @escaping (_ data: Activity?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let activityId = "activityId_example" // String | 
let activityStatusUpdate = ActivityStatusUpdate(status: "status_example") // ActivityStatusUpdate | 

ActivityAPI.updateActivityStatus(activityId: activityId, activityStatusUpdate: activityStatusUpdate) { (response, error) in
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
 **activityId** | **String** |  | 
 **activityStatusUpdate** | [**ActivityStatusUpdate**](ActivityStatusUpdate.md) |  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

