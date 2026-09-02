# ListOpenItemsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listOpenItemsApi**](ListOpenItemsAPI.md#listopenitemsapi) | **GET** /api/v1/bookkeeping/open-items | 


# **listOpenItemsApi**
```swift
    open class func listOpenItemsApi(reminderLevel1Days: Int64? = nil, reminderLevel2Days: Int64? = nil, reminderLevel3Days: Int64? = nil, customerId: String? = nil, completion: @escaping (_ data: [OpenItem]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let reminderLevel1Days = 987 // Int64 |  (optional)
let reminderLevel2Days = 987 // Int64 |  (optional)
let reminderLevel3Days = 987 // Int64 |  (optional)
let customerId = "customerId_example" // String |  (optional)

ListOpenItemsAPI.listOpenItemsApi(reminderLevel1Days: reminderLevel1Days, reminderLevel2Days: reminderLevel2Days, reminderLevel3Days: reminderLevel3Days, customerId: customerId) { (response, error) in
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
 **reminderLevel1Days** | **Int64** |  | [optional] 
 **reminderLevel2Days** | **Int64** |  | [optional] 
 **reminderLevel3Days** | **Int64** |  | [optional] 
 **customerId** | **String** |  | [optional] 

### Return type

[**[OpenItem]**](OpenItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

