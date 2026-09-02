# OnlineshopAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSmtpConfigApi**](OnlineshopAPI.md#getsmtpconfigapi) | **GET** /api/v1/settings/smtp | 
[**saveSmtpConfigApi**](OnlineshopAPI.md#savesmtpconfigapi) | **PUT** /api/v1/settings/smtp | 


# **getSmtpConfigApi**
```swift
    open class func getSmtpConfigApi(completion: @escaping (_ data: SmtpConfig?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


OnlineshopAPI.getSmtpConfigApi() { (response, error) in
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

[**SmtpConfig**](SmtpConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **saveSmtpConfigApi**
```swift
    open class func saveSmtpConfigApi(smtpConfig: SmtpConfig? = nil, completion: @escaping (_ data: SmtpConfig?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let smtpConfig = SmtpConfig(encryption: SmtpEncryption(), fromAddress: "fromAddress_example", fromName: "fromName_example", host: "host_example", password: "password_example", port: 123, timeoutSeconds: 123, username: "username_example") // SmtpConfig |  (optional)

OnlineshopAPI.saveSmtpConfigApi(smtpConfig: smtpConfig) { (response, error) in
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
 **smtpConfig** | [**SmtpConfig**](SmtpConfig.md) |  | [optional] 

### Return type

[**SmtpConfig**](SmtpConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

