# AiAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**aiSuggestApi**](AiAPI.md#aisuggestapi) | **POST** /api/v1/support/ai/suggest | 
[**createWorkerApi**](AiAPI.md#createworkerapi) | **POST** /api/v1/support/ai/workers | 
[**listWorkersApi**](AiAPI.md#listworkersapi) | **GET** /api/v1/support/ai/workers | 
[**runWorkerApi**](AiAPI.md#runworkerapi) | **POST** /api/v1/support/ai/workers/{worker_id}/run | 


# **aiSuggestApi**
```swift
    open class func aiSuggestApi(aiSuggestionRequest: AiSuggestionRequest, completion: @escaping (_ data: AiSuggestion?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let aiSuggestionRequest = AiSuggestionRequest(instructions: "instructions_example", messageBody: "messageBody_example", ticketId: 123) // AiSuggestionRequest | 

AiAPI.aiSuggestApi(aiSuggestionRequest: aiSuggestionRequest) { (response, error) in
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
 **aiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md) |  | 

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createWorkerApi**
```swift
    open class func createWorkerApi(aiConfigDto: AiConfigDto, completion: @escaping (_ data: AiWorkerConfig?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let aiConfigDto = AiConfigDto(autoReply: false, maxToolCalls: 123, model: "model_example", name: "name_example", provider: "provider_example", systemPrompt: "systemPrompt_example", triggerOn: ["triggerOn_example"]) // AiConfigDto | 

AiAPI.createWorkerApi(aiConfigDto: aiConfigDto) { (response, error) in
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
 **aiConfigDto** | [**AiConfigDto**](AiConfigDto.md) |  | 

### Return type

[**AiWorkerConfig**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWorkersApi**
```swift
    open class func listWorkersApi(completion: @escaping (_ data: [AiWorkerConfig]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


AiAPI.listWorkersApi() { (response, error) in
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

[**[AiWorkerConfig]**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **runWorkerApi**
```swift
    open class func runWorkerApi(workerId: UUID, aiSuggestionRequest: AiSuggestionRequest, completion: @escaping (_ data: AiSuggestion?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let workerId = 987 // UUID | 
let aiSuggestionRequest = AiSuggestionRequest(instructions: "instructions_example", messageBody: "messageBody_example", ticketId: 123) // AiSuggestionRequest | 

AiAPI.runWorkerApi(workerId: workerId, aiSuggestionRequest: aiSuggestionRequest) { (response, error) in
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
 **workerId** | **UUID** |  | 
 **aiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md) |  | 

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

