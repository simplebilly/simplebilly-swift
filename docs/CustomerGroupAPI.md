# CustomerGroupAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addGroupMembers**](CustomerGroupAPI.md#addgroupmembers) | **POST** /api/v1/customer-groups/{customer_group_id}/members | 
[**createCustomerGroup**](CustomerGroupAPI.md#createcustomergroup) | **POST** /api/v1/customer-groups | 
[**deleteCustomerGroup**](CustomerGroupAPI.md#deletecustomergroup) | **DELETE** /api/v1/customer-groups/{customer_group_id} | 
[**getCustomerGroup**](CustomerGroupAPI.md#getcustomergroup) | **GET** /api/v1/customer-groups/{customer_group_id} | 
[**listCustomerGroups**](CustomerGroupAPI.md#listcustomergroups) | **GET** /api/v1/customer-groups/ | 
[**updateCustomerGroup**](CustomerGroupAPI.md#updatecustomergroup) | **PUT** /api/v1/customer-groups/{customer_group_id} | 


# **addGroupMembers**
```swift
    open class func addGroupMembers(customerGroupId: String, body: AnyCodable, completion: @escaping (_ data: CustomerGroup?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let customerGroupId = "customerGroupId_example" // String | 
let body =  // AnyCodable | 

CustomerGroupAPI.addGroupMembers(customerGroupId: customerGroupId, body: body) { (response, error) in
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
 **customerGroupId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createCustomerGroup**
```swift
    open class func createCustomerGroup(customerGroupCreate: CustomerGroupCreate, completion: @escaping (_ data: CustomerGroup?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let customerGroupCreate = CustomerGroupCreate(description: "description_example", memberIds: ["memberIds_example"], membershipFilter: "membershipFilter_example", name: "name_example") // CustomerGroupCreate | 

CustomerGroupAPI.createCustomerGroup(customerGroupCreate: customerGroupCreate) { (response, error) in
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
 **customerGroupCreate** | [**CustomerGroupCreate**](CustomerGroupCreate.md) |  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteCustomerGroup**
```swift
    open class func deleteCustomerGroup(customerGroupId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let customerGroupId = "customerGroupId_example" // String | 

CustomerGroupAPI.deleteCustomerGroup(customerGroupId: customerGroupId) { (response, error) in
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
 **customerGroupId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCustomerGroup**
```swift
    open class func getCustomerGroup(customerGroupId: String, completion: @escaping (_ data: CustomerGroup?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let customerGroupId = "customerGroupId_example" // String | 

CustomerGroupAPI.getCustomerGroup(customerGroupId: customerGroupId) { (response, error) in
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
 **customerGroupId** | **String** |  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listCustomerGroups**
```swift
    open class func listCustomerGroups(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [CustomerGroup]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

CustomerGroupAPI.listCustomerGroups(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[CustomerGroup]**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateCustomerGroup**
```swift
    open class func updateCustomerGroup(customerGroupId: String, customerGroupUpdate: CustomerGroupUpdate, completion: @escaping (_ data: CustomerGroup?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let customerGroupId = "customerGroupId_example" // String | 
let customerGroupUpdate = CustomerGroupUpdate(description: "description_example", memberIds: ["memberIds_example"], membershipFilter: "membershipFilter_example", name: "name_example") // CustomerGroupUpdate | 

CustomerGroupAPI.updateCustomerGroup(customerGroupId: customerGroupId, customerGroupUpdate: customerGroupUpdate) { (response, error) in
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
 **customerGroupId** | **String** |  | 
 **customerGroupUpdate** | [**CustomerGroupUpdate**](CustomerGroupUpdate.md) |  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

