# InstituteProfileAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getInstituteProfile**](InstituteProfileAPI.md#getinstituteprofile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing).
[**updateInstituteProfile**](InstituteProfileAPI.md#updateinstituteprofile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert).


# **getInstituteProfile**
```swift
    open class func getInstituteProfile(completion: @escaping (_ data: InstituteProfile?, _ error: Error?) -> Void)
```

Current institute profile (created with defaults when missing).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Current institute profile (created with defaults when missing).
InstituteProfileAPI.getInstituteProfile() { (response, error) in
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

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateInstituteProfile**
```swift
    open class func updateInstituteProfile(instituteProfileUpdate: InstituteProfileUpdate, completion: @escaping (_ data: InstituteProfile?, _ error: Error?) -> Void)
```

Update the institute profile (institute_type and/or kapitalmarktorientiert).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let instituteProfileUpdate = InstituteProfileUpdate(instituteType: "instituteType_example", kapitalmarktorientiert: false) // InstituteProfileUpdate | 

// Update the institute profile (institute_type and/or kapitalmarktorientiert).
InstituteProfileAPI.updateInstituteProfile(instituteProfileUpdate: instituteProfileUpdate) { (response, error) in
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
 **instituteProfileUpdate** | [**InstituteProfileUpdate**](InstituteProfileUpdate.md) |  | 

### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

