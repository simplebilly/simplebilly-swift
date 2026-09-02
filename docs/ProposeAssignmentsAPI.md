# ProposeAssignmentsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**proposeAssignmentsApi**](ProposeAssignmentsAPI.md#proposeassignmentsapi) | **GET** /api/v1/bookkeeping/propose-assignments | 


# **proposeAssignmentsApi**
```swift
    open class func proposeAssignmentsApi(minConfidence: Double? = nil, customerId: String? = nil, completion: @escaping (_ data: [ProposedAssignment]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let minConfidence = 987 // Double |  (optional)
let customerId = "customerId_example" // String |  (optional)

ProposeAssignmentsAPI.proposeAssignmentsApi(minConfidence: minConfidence, customerId: customerId) { (response, error) in
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
 **minConfidence** | **Double** |  | [optional] 
 **customerId** | **String** |  | [optional] 

### Return type

[**[ProposedAssignment]**](ProposedAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

