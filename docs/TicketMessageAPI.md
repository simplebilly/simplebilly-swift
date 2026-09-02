# TicketMessageAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listMessagesApi**](TicketMessageAPI.md#listmessagesapi) | **GET** /api/v1/support/tickets/{ticket_id}/messages | 
[**sendMessageApi**](TicketMessageAPI.md#sendmessageapi) | **POST** /api/v1/support/tickets/{ticket_id}/messages | 


# **listMessagesApi**
```swift
    open class func listMessagesApi(ticketId: UUID, completion: @escaping (_ data: [TicketMessage]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ticketId = 987 // UUID | 

TicketMessageAPI.listMessagesApi(ticketId: ticketId) { (response, error) in
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

[**[TicketMessage]**](TicketMessage.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendMessageApi**
```swift
    open class func sendMessageApi(ticketId: UUID, sendMessageDto: SendMessageDto, completion: @escaping (_ data: TicketMessage?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let ticketId = 987 // UUID | 
let sendMessageDto = SendMessageDto(body: "body_example", isInternal: false) // SendMessageDto | 

TicketMessageAPI.sendMessageApi(ticketId: ticketId, sendMessageDto: sendMessageDto) { (response, error) in
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
 **sendMessageDto** | [**SendMessageDto**](SendMessageDto.md) |  | 

### Return type

[**TicketMessage**](TicketMessage.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

