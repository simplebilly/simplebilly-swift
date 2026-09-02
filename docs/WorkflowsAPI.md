# WorkflowsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listWorkflowsApi**](WorkflowsAPI.md#listworkflowsapi) | **GET** /api/v1/workflows | 
[**setWorkflowEnabledApi**](WorkflowsAPI.md#setworkflowenabledapi) | **PUT** /api/v1/workflows/{workflow_id}/enabled | 


# **listWorkflowsApi**
```swift
    open class func listWorkflowsApi(completion: @escaping (_ data: [Workflow]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


WorkflowsAPI.listWorkflowsApi() { (response, error) in
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

[**[Workflow]**](Workflow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setWorkflowEnabledApi**
```swift
    open class func setWorkflowEnabledApi(workflowId: String, workflowEnabledUpdate: WorkflowEnabledUpdate, completion: @escaping (_ data: Workflow?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let workflowId = "workflowId_example" // String | 
let workflowEnabledUpdate = WorkflowEnabledUpdate(enabled: false) // WorkflowEnabledUpdate | 

WorkflowsAPI.setWorkflowEnabledApi(workflowId: workflowId, workflowEnabledUpdate: workflowEnabledUpdate) { (response, error) in
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
 **workflowId** | **String** |  | 
 **workflowEnabledUpdate** | [**WorkflowEnabledUpdate**](WorkflowEnabledUpdate.md) |  | 

### Return type

[**Workflow**](Workflow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

