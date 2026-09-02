# SupportTicketAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTicketApi**](SupportTicketAPI.md#createticketapi) | **POST** /api/v1/support/tickets | 
[**deleteTicketApi**](SupportTicketAPI.md#deleteticketapi) | **DELETE** /api/v1/support/tickets/{ticket_id} | 
[**getTicketApi**](SupportTicketAPI.md#getticketapi) | **GET** /api/v1/support/tickets/{ticket_id} | 
[**listTicketsApi**](SupportTicketAPI.md#listticketsapi) | **GET** /api/v1/support/tickets | 
[**updateTicketApi**](SupportTicketAPI.md#updateticketapi) | **PUT** /api/v1/support/tickets/{ticket_id} | 


# **createTicketApi**
```swift
    open class func createTicketApi(createTicketRequest: CreateTicketRequest, completion: @escaping (_ data: SupportTicket?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let createTicketRequest = CreateTicketRequest(channelId: 123, channelType: "channelType_example", customerEmail: "customerEmail_example", customerId: "customerId_example", customerName: "customerName_example", externalId: "externalId_example", messageBody: "messageBody_example", orderRef: "orderRef_example", subject: "subject_example") // CreateTicketRequest | 

SupportTicketAPI.createTicketApi(createTicketRequest: createTicketRequest) { (response, error) in
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
 **createTicketRequest** | [**CreateTicketRequest**](CreateTicketRequest.md) |  | 

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteTicketApi**
```swift
    open class func deleteTicketApi(ticketId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ticketId = 987 // UUID | 

SupportTicketAPI.deleteTicketApi(ticketId: ticketId) { (response, error) in
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
 **ticketId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTicketApi**
```swift
    open class func getTicketApi(ticketId: UUID, completion: @escaping (_ data: SupportTicket?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ticketId = 987 // UUID | 

SupportTicketAPI.getTicketApi(ticketId: ticketId) { (response, error) in
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
 **ticketId** | **UUID** |  | 

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTicketsApi**
```swift
    open class func listTicketsApi(status: String? = nil, priority: String? = nil, assignedTo: UUID? = nil, channelType: String? = nil, customerId: String? = nil, search: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: [SupportTicket]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let status = "status_example" // String |  (optional)
let priority = "priority_example" // String |  (optional)
let assignedTo = 987 // UUID |  (optional)
let channelType = "channelType_example" // String |  (optional)
let customerId = "customerId_example" // String |  (optional)
let search = "search_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

SupportTicketAPI.listTicketsApi(status: status, priority: priority, assignedTo: assignedTo, channelType: channelType, customerId: customerId, search: search, page: page, pageSize: pageSize) { (response, error) in
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
 **priority** | **String** |  | [optional] 
 **assignedTo** | **UUID** |  | [optional] 
 **channelType** | **String** |  | [optional] 
 **customerId** | **String** |  | [optional] 
 **search** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**[SupportTicket]**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateTicketApi**
```swift
    open class func updateTicketApi(ticketId: UUID, supportTicketUpdate: SupportTicketUpdate, completion: @escaping (_ data: SupportTicket?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ticketId = 987 // UUID | 
let supportTicketUpdate = SupportTicketUpdate(assignedTo: 123, channelId: 123, channelType: SupportChannelType(), closedAt: Date(), createdAt: Date(), customerEmail: "customerEmail_example", customerId: "customerId_example", customerName: "customerName_example", externalId: "externalId_example", firstMessageAt: Date(), lastMessageAt: Date(), leadId: 123, messageCount: 123, orderRef: "orderRef_example", priority: TicketPriority(), resolution: "resolution_example", status: SupportTicketStatus(), subject: "subject_example", tags: 123, tenantId: 123, updatedAt: Date()) // SupportTicketUpdate | 

SupportTicketAPI.updateTicketApi(ticketId: ticketId, supportTicketUpdate: supportTicketUpdate) { (response, error) in
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
 **ticketId** | **UUID** |  | 
 **supportTicketUpdate** | [**SupportTicketUpdate**](SupportTicketUpdate.md) |  | 

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

