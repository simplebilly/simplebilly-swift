# UserManagementAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getUser**](UserManagementAPI.md#getuser) | **GET** /api/v1/users/{user_id} | 
[**listUsers**](UserManagementAPI.md#listusers) | **GET** /api/v1/users | 
[**removeUser**](UserManagementAPI.md#removeuser) | **DELETE** /api/v1/users/{user_id} | 
[**updateUserPermissions**](UserManagementAPI.md#updateuserpermissions) | **PUT** /api/v1/users/{user_id}/permissions | 
[**updateUserRole**](UserManagementAPI.md#updateuserrole) | **PUT** /api/v1/users/{user_id}/role | 


# **getUser**
```swift
    open class func getUser(userId: UUID, completion: @escaping (_ data: TenantUser?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let userId = 987 // UUID | 

UserManagementAPI.getUser(userId: userId) { (response, error) in
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
 **userId** | **UUID** |  | 

### Return type

[**TenantUser**](TenantUser.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listUsers**
```swift
    open class func listUsers(completion: @escaping (_ data: [TenantUser]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


UserManagementAPI.listUsers() { (response, error) in
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

[**[TenantUser]**](TenantUser.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeUser**
```swift
    open class func removeUser(userId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let userId = 987 // UUID | 

UserManagementAPI.removeUser(userId: userId) { (response, error) in
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
 **userId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateUserPermissions**
```swift
    open class func updateUserPermissions(userId: UUID, updatePermissionsPayload: UpdatePermissionsPayload, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let userId = 987 // UUID | 
let updatePermissionsPayload = UpdatePermissionsPayload(permissions: ["permissions_example"]) // UpdatePermissionsPayload | 

UserManagementAPI.updateUserPermissions(userId: userId, updatePermissionsPayload: updatePermissionsPayload) { (response, error) in
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
 **userId** | **UUID** |  | 
 **updatePermissionsPayload** | [**UpdatePermissionsPayload**](UpdatePermissionsPayload.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateUserRole**
```swift
    open class func updateUserRole(userId: UUID, updateRolePayload: UpdateRolePayload, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let userId = 987 // UUID | 
let updateRolePayload = UpdateRolePayload(role: "role_example", syncPermissions: false) // UpdateRolePayload | 

UserManagementAPI.updateUserRole(userId: userId, updateRolePayload: updateRolePayload) { (response, error) in
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
 **userId** | **UUID** |  | 
 **updateRolePayload** | [**UpdateRolePayload**](UpdateRolePayload.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

