# TenantSettingsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTenantSettings**](TenantSettingsAPI.md#gettenantsettings) | **GET** /api/v1/settings/tenant | 
[**updateTenantSettings**](TenantSettingsAPI.md#updatetenantsettings) | **PUT** /api/v1/settings/tenant | 


# **getTenantSettings**
```swift
    open class func getTenantSettings(completion: @escaping (_ data: TenantSettings?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


TenantSettingsAPI.getTenantSettings() { (response, error) in
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

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateTenantSettings**
```swift
    open class func updateTenantSettings(updateTenantSettings: UpdateTenantSettings, completion: @escaping (_ data: TenantSettings?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let updateTenantSettings = UpdateTenantSettings(companyType: CompanyType(), features: PartialFeatureSettings(onlineshop: false, reportBilanz: false, reportBwa: false, reportEuer: false, reportGewerbesteuer: false, reportGuv: false, reportKst: false, reportUstva: false)) // UpdateTenantSettings | 

TenantSettingsAPI.updateTenantSettings(updateTenantSettings: updateTenantSettings) { (response, error) in
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
 **updateTenantSettings** | [**UpdateTenantSettings**](UpdateTenantSettings.md) |  | 

### Return type

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

