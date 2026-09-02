# AutomationsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listAutomations**](AutomationsAPI.md#listautomations) | **GET** /api/v1/automations | 
[**triggerAutomation**](AutomationsAPI.md#triggerautomation) | **POST** /api/v1/automations/{key}/trigger | 
[**updateAutomation**](AutomationsAPI.md#updateautomation) | **PUT** /api/v1/automations/{key} | 


# **listAutomations**
```swift
    open class func listAutomations(completion: @escaping (_ data: [AutomationDto]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


AutomationsAPI.listAutomations() { (response, error) in
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

[**[AutomationDto]**](AutomationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **triggerAutomation**
```swift
    open class func triggerAutomation(key: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let key = "key_example" // String | 

AutomationsAPI.triggerAutomation(key: key) { (response, error) in
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
 **key** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAutomation**
```swift
    open class func updateAutomation(key: String, updateAutomation: UpdateAutomation, completion: @escaping (_ data: AutomationDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let key = "key_example" // String | 
let updateAutomation = UpdateAutomation(config: 123, enabled: false) // UpdateAutomation | 

AutomationsAPI.updateAutomation(key: key, updateAutomation: updateAutomation) { (response, error) in
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
 **key** | **String** |  | 
 **updateAutomation** | [**UpdateAutomation**](UpdateAutomation.md) |  | 

### Return type

[**AutomationDto**](AutomationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

