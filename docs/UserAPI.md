# UserAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**changePassword**](UserAPI.md#changepassword) | **POST** /user/change-password | Change the current user&#39;s password (requires the current password).
[**createTeam**](UserAPI.md#createteam) | **POST** /user/teams | Create a new team within the current tenant
[**generateApiKey**](UserAPI.md#generateapikey) | **POST** /user/api-key | Generate a new API key for the current user
[**inviteUser**](UserAPI.md#inviteuser) | **POST** /user/invite | Invite a user to the current tenant/organization
[**listTeams**](UserAPI.md#listteams) | **GET** /user/teams | List all teams in the current tenant
[**removeUserFromOrg**](UserAPI.md#removeuserfromorg) | **DELETE** /user/remove | Remove a user from the current organization
[**updateProfile**](UserAPI.md#updateprofile) | **PUT** /user/profile | Update the current user&#39;s profile
[**userProfile**](UserAPI.md#userprofile) | **GET** /user/profile | Get the current user&#39;s profile
[**userTenants**](UserAPI.md#usertenants) | **GET** /user/tenants | List all tenants (organizations) the current user belongs to


# **changePassword**
```swift
    open class func changePassword(changePasswordRequest: ChangePasswordRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Change the current user's password (requires the current password).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let changePasswordRequest = ChangePasswordRequest(currentPassword: "currentPassword_example", newPassword: "newPassword_example") // ChangePasswordRequest | 

// Change the current user's password (requires the current password).
UserAPI.changePassword(changePasswordRequest: changePasswordRequest) { (response, error) in
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
 **changePasswordRequest** | [**ChangePasswordRequest**](ChangePasswordRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createTeam**
```swift
    open class func createTeam(teamCreate: TeamCreate, completion: @escaping (_ data: ApiResponseTeam?, _ error: Error?) -> Void)
```

Create a new team within the current tenant

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let teamCreate = TeamCreate(description: "description_example", name: "name_example", parentTeamId: 123) // TeamCreate | 

// Create a new team within the current tenant
UserAPI.createTeam(teamCreate: teamCreate) { (response, error) in
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
 **teamCreate** | [**TeamCreate**](TeamCreate.md) |  | 

### Return type

[**ApiResponseTeam**](ApiResponseTeam.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generateApiKey**
```swift
    open class func generateApiKey(completion: @escaping (_ data: ApiResponseString?, _ error: Error?) -> Void)
```

Generate a new API key for the current user

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Generate a new API key for the current user
UserAPI.generateApiKey() { (response, error) in
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

[**ApiResponseString**](ApiResponseString.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **inviteUser**
```swift
    open class func inviteUser(inviteRequest: InviteRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Invite a user to the current tenant/organization

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let inviteRequest = InviteRequest(email: "email_example") // InviteRequest | 

// Invite a user to the current tenant/organization
UserAPI.inviteUser(inviteRequest: inviteRequest) { (response, error) in
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
 **inviteRequest** | [**InviteRequest**](InviteRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTeams**
```swift
    open class func listTeams(completion: @escaping (_ data: ApiResponseVecTeam?, _ error: Error?) -> Void)
```

List all teams in the current tenant

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List all teams in the current tenant
UserAPI.listTeams() { (response, error) in
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

[**ApiResponseVecTeam**](ApiResponseVecTeam.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeUserFromOrg**
```swift
    open class func removeUserFromOrg(removeUserRequest: RemoveUserRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Remove a user from the current organization

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let removeUserRequest = RemoveUserRequest(email: "email_example") // RemoveUserRequest | 

// Remove a user from the current organization
UserAPI.removeUserFromOrg(removeUserRequest: removeUserRequest) { (response, error) in
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
 **removeUserRequest** | [**RemoveUserRequest**](RemoveUserRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProfile**
```swift
    open class func updateProfile(updateProfileRequest: UpdateProfileRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Update the current user's profile

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let updateProfileRequest = UpdateProfileRequest(avatarUrl: "avatarUrl_example", firstName: "firstName_example", lastName: "lastName_example", name: "name_example") // UpdateProfileRequest | 

// Update the current user's profile
UserAPI.updateProfile(updateProfileRequest: updateProfileRequest) { (response, error) in
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
 **updateProfileRequest** | [**UpdateProfileRequest**](UpdateProfileRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userProfile**
```swift
    open class func userProfile(completion: @escaping (_ data: ApiResponseUserProfile?, _ error: Error?) -> Void)
```

Get the current user's profile

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Get the current user's profile
UserAPI.userProfile() { (response, error) in
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

[**ApiResponseUserProfile**](ApiResponseUserProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userTenants**
```swift
    open class func userTenants(completion: @escaping (_ data: ApiResponseVecUserTenantInfo?, _ error: Error?) -> Void)
```

List all tenants (organizations) the current user belongs to

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List all tenants (organizations) the current user belongs to
UserAPI.userTenants() { (response, error) in
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

[**ApiResponseVecUserTenantInfo**](ApiResponseVecUserTenantInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

