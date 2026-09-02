# LeadAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listLeadsApi**](LeadAPI.md#listleadsapi) | **GET** /api/v1/support/leads | 
[**updateLeadApi**](LeadAPI.md#updateleadapi) | **PUT** /api/v1/support/leads/{lead_id} | 


# **listLeadsApi**
```swift
    open class func listLeadsApi(status: String? = nil, source: String? = nil, search: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: [Lead]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let status = "status_example" // String |  (optional)
let source = "source_example" // String |  (optional)
let search = "search_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

LeadAPI.listLeadsApi(status: status, source: source, search: search, page: page, pageSize: pageSize) { (response, error) in
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
 **status** | **String** |  | [optional] 
 **source** | **String** |  | [optional] 
 **search** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**[Lead]**](Lead.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateLeadApi**
```swift
    open class func updateLeadApi(leadId: UUID, leadUpdate: LeadUpdate, completion: @escaping (_ data: Lead?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let leadId = 987 // UUID | 
let leadUpdate = LeadUpdate(company: "company_example", convertedAt: Date(), createdAt: Date(), email: "email_example", firstContactAt: Date(), name: "name_example", notes: "notes_example", phone: "phone_example", score: 123, source: "source_example", status: LeadStatus(), tags: 123, tenantId: 123, updatedAt: Date()) // LeadUpdate | 

LeadAPI.updateLeadApi(leadId: leadId, leadUpdate: leadUpdate) { (response, error) in
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
 **leadId** | **UUID** |  | 
 **leadUpdate** | [**LeadUpdate**](LeadUpdate.md) |  | 

### Return type

[**Lead**](Lead.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

