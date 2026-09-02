# EmailTemplateAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createEmailTemplate**](EmailTemplateAPI.md#createemailtemplate) | **POST** /api/v1/email-templates | 
[**deleteEmailTemplate**](EmailTemplateAPI.md#deleteemailtemplate) | **DELETE** /api/v1/email-templates/{email_template_id} | 
[**getEmailTemplate**](EmailTemplateAPI.md#getemailtemplate) | **GET** /api/v1/email-templates/{email_template_id} | 
[**listEmailTemplates**](EmailTemplateAPI.md#listemailtemplates) | **GET** /api/v1/email-templates/ | 
[**renderEmailTemplate**](EmailTemplateAPI.md#renderemailtemplate) | **POST** /api/v1/email-templates/{email_template_id}/render | 
[**updateEmailTemplate**](EmailTemplateAPI.md#updateemailtemplate) | **PUT** /api/v1/email-templates/{email_template_id} | 


# **createEmailTemplate**
```swift
    open class func createEmailTemplate(emailTemplateCreate: EmailTemplateCreate, completion: @escaping (_ data: EmailTemplate?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let emailTemplateCreate = EmailTemplateCreate(body: "body_example", name: "name_example", status: EmailTemplateStatus(), subject: "subject_example", variables: 123) // EmailTemplateCreate | 

EmailTemplateAPI.createEmailTemplate(emailTemplateCreate: emailTemplateCreate) { (response, error) in
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
 **emailTemplateCreate** | [**EmailTemplateCreate**](EmailTemplateCreate.md) |  | 

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteEmailTemplate**
```swift
    open class func deleteEmailTemplate(emailTemplateId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let emailTemplateId = "emailTemplateId_example" // String | 

EmailTemplateAPI.deleteEmailTemplate(emailTemplateId: emailTemplateId) { (response, error) in
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
 **emailTemplateId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEmailTemplate**
```swift
    open class func getEmailTemplate(emailTemplateId: String, completion: @escaping (_ data: EmailTemplate?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let emailTemplateId = "emailTemplateId_example" // String | 

EmailTemplateAPI.getEmailTemplate(emailTemplateId: emailTemplateId) { (response, error) in
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
 **emailTemplateId** | **String** |  | 

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listEmailTemplates**
```swift
    open class func listEmailTemplates(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, search: String? = nil, completion: @escaping (_ data: [EmailTemplate]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let search = "search_example" // String |  (optional)

EmailTemplateAPI.listEmailTemplates(page: page, pageSize: pageSize, status: status, search: search) { (response, error) in
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
 **status** | **String** |  | [optional] 
 **search** | **String** |  | [optional] 

### Return type

[**[EmailTemplate]**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **renderEmailTemplate**
```swift
    open class func renderEmailTemplate(emailTemplateId: String, body: AnyCodable, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let emailTemplateId = "emailTemplateId_example" // String | 
let body =  // AnyCodable | 

EmailTemplateAPI.renderEmailTemplate(emailTemplateId: emailTemplateId, body: body) { (response, error) in
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
 **emailTemplateId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateEmailTemplate**
```swift
    open class func updateEmailTemplate(emailTemplateId: String, emailTemplateUpdate: EmailTemplateUpdate, completion: @escaping (_ data: EmailTemplate?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let emailTemplateId = "emailTemplateId_example" // String | 
let emailTemplateUpdate = EmailTemplateUpdate(body: "body_example", name: "name_example", status: EmailTemplateStatus(), subject: "subject_example", variables: 123) // EmailTemplateUpdate | 

EmailTemplateAPI.updateEmailTemplate(emailTemplateId: emailTemplateId, emailTemplateUpdate: emailTemplateUpdate) { (response, error) in
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
 **emailTemplateId** | **String** |  | 
 **emailTemplateUpdate** | [**EmailTemplateUpdate**](EmailTemplateUpdate.md) |  | 

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

