# GroupFigureAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createGroupFigure**](GroupFigureAPI.md#creategroupfigure) | **POST** /api/v1/group-figures | 
[**deleteGroupFigure**](GroupFigureAPI.md#deletegroupfigure) | **DELETE** /api/v1/group-figures/{year} | 
[**getGroupFigure**](GroupFigureAPI.md#getgroupfigure) | **GET** /api/v1/group-figures/{year} | 
[**getGroupFigures**](GroupFigureAPI.md#getgroupfigures) | **GET** /api/v1/group-figures/ | 
[**updateGroupFigure**](GroupFigureAPI.md#updategroupfigure) | **PUT** /api/v1/group-figures/{year} | 


# **createGroupFigure**
```swift
    open class func createGroupFigure(groupFigureCreate: GroupFigureCreate, completion: @escaping (_ data: GroupFigure?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let groupFigureCreate = GroupFigureCreate(bilanzsumme: "bilanzsumme_example", exemptionClaimed: false, mitarbeiter: 123, nettoUmsatz: "nettoUmsatz_example", parentName: "parentName_example", parentSitus: "parentSitus_example") // GroupFigureCreate | 

GroupFigureAPI.createGroupFigure(groupFigureCreate: groupFigureCreate) { (response, error) in
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
 **groupFigureCreate** | [**GroupFigureCreate**](GroupFigureCreate.md) |  | 

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteGroupFigure**
```swift
    open class func deleteGroupFigure(year: Int, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

GroupFigureAPI.deleteGroupFigure(year: year) { (response, error) in
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

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getGroupFigure**
```swift
    open class func getGroupFigure(year: Int, completion: @escaping (_ data: GroupFigure?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 

GroupFigureAPI.getGroupFigure(year: year) { (response, error) in
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

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getGroupFigures**
```swift
    open class func getGroupFigures(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [GroupFigure]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

GroupFigureAPI.getGroupFigures(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[GroupFigure]**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateGroupFigure**
```swift
    open class func updateGroupFigure(year: Int, groupFigureUpdate: GroupFigureUpdate, completion: @escaping (_ data: GroupFigure?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 
let groupFigureUpdate = GroupFigureUpdate(bilanzsumme: "bilanzsumme_example", exemptionClaimed: false, mitarbeiter: 123, nettoUmsatz: "nettoUmsatz_example", parentName: "parentName_example", parentSitus: "parentSitus_example") // GroupFigureUpdate | 

GroupFigureAPI.updateGroupFigure(year: year, groupFigureUpdate: groupFigureUpdate) { (response, error) in
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
 **groupFigureUpdate** | [**GroupFigureUpdate**](GroupFigureUpdate.md) |  | 

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

