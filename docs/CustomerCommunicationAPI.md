# CustomerCommunicationAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createCommunication**](CustomerCommunicationAPI.md#createcommunication) | **POST** /api/v1/communications | 
[**customercommunicationRestore**](CustomerCommunicationAPI.md#customercommunicationrestore) | **POST** /api/v1/communications/{communication_id}/restore | 
[**deleteCommunication**](CustomerCommunicationAPI.md#deletecommunication) | **DELETE** /api/v1/communications/{communication_id} | 
[**getCommunication**](CustomerCommunicationAPI.md#getcommunication) | **GET** /api/v1/communications/{communication_id} | 
[**getContactHistory**](CustomerCommunicationAPI.md#getcontacthistory) | **GET** /api/v1/contacts/{contact_id}/communications | 
[**listCommunications**](CustomerCommunicationAPI.md#listcommunications) | **GET** /api/v1/communications/ | 
[**updateCommunication**](CustomerCommunicationAPI.md#updatecommunication) | **PUT** /api/v1/communications/{communication_id} | 


# **createCommunication**
```swift
    open class func createCommunication(customerCommunicationCreate: CustomerCommunicationCreate, completion: @escaping (_ data: CustomerCommunication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let customerCommunicationCreate = CustomerCommunicationCreate(body: "body_example", channel: CommunicationChannel(), contactId: "contactId_example", counterparty: "counterparty_example", direction: CommunicationDirection(), occurredAt: Date(), subject: "subject_example", tags: 123) // CustomerCommunicationCreate | 

CustomerCommunicationAPI.createCommunication(customerCommunicationCreate: customerCommunicationCreate) { (response, error) in
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
 **customerCommunicationCreate** | [**CustomerCommunicationCreate**](CustomerCommunicationCreate.md) |  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **customercommunicationRestore**
```swift
    open class func customercommunicationRestore(communicationId: String, completion: @escaping (_ data: CustomerCommunication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let communicationId = "communicationId_example" // String | 

CustomerCommunicationAPI.customercommunicationRestore(communicationId: communicationId) { (response, error) in
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
 **communicationId** | **String** |  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteCommunication**
```swift
    open class func deleteCommunication(communicationId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let communicationId = "communicationId_example" // String | 

CustomerCommunicationAPI.deleteCommunication(communicationId: communicationId) { (response, error) in
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
 **communicationId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCommunication**
```swift
    open class func getCommunication(communicationId: String, completion: @escaping (_ data: CustomerCommunication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let communicationId = "communicationId_example" // String | 

CustomerCommunicationAPI.getCommunication(communicationId: communicationId) { (response, error) in
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
 **communicationId** | **String** |  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getContactHistory**
```swift
    open class func getContactHistory(contactId: String, completion: @escaping (_ data: ContactHistoryResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let contactId = "contactId_example" // String | 

CustomerCommunicationAPI.getContactHistory(contactId: contactId) { (response, error) in
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
 **contactId** | **String** |  | 

### Return type

[**ContactHistoryResponse**](ContactHistoryResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listCommunications**
```swift
    open class func listCommunications(page: Int? = nil, pageSize: Int? = nil, contactId: String? = nil, channel: CommunicationChannel? = nil, direction: CommunicationDirection? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [CustomerCommunication]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let contactId = "contactId_example" // String | Filter history to a single contact. (optional)
let channel = CommunicationChannel() // CommunicationChannel |  (optional)
let direction = CommunicationDirection() // CommunicationDirection |  (optional)
let from = Date() // Date | Only include communications after this ISO date (inclusive). (optional)
let to = Date() // Date | Only include communications before this ISO date (inclusive). (optional)

CustomerCommunicationAPI.listCommunications(page: page, pageSize: pageSize, contactId: contactId, channel: channel, direction: direction, from: from, to: to) { (response, error) in
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
 **contactId** | **String** | Filter history to a single contact. | [optional] 
 **channel** | [**CommunicationChannel**](.md) |  | [optional] 
 **direction** | [**CommunicationDirection**](.md) |  | [optional] 
 **from** | **Date** | Only include communications after this ISO date (inclusive). | [optional] 
 **to** | **Date** | Only include communications before this ISO date (inclusive). | [optional] 

### Return type

[**[CustomerCommunication]**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateCommunication**
```swift
    open class func updateCommunication(communicationId: String, customerCommunicationUpdate: CustomerCommunicationUpdate, completion: @escaping (_ data: CustomerCommunication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let communicationId = "communicationId_example" // String | 
let customerCommunicationUpdate = CustomerCommunicationUpdate(body: "body_example", channel: CommunicationChannel(), contactId: "contactId_example", counterparty: "counterparty_example", direction: CommunicationDirection(), occurredAt: Date(), subject: "subject_example", tags: 123) // CustomerCommunicationUpdate | 

CustomerCommunicationAPI.updateCommunication(communicationId: communicationId, customerCommunicationUpdate: customerCommunicationUpdate) { (response, error) in
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
 **communicationId** | **String** |  | 
 **customerCommunicationUpdate** | [**CustomerCommunicationUpdate**](CustomerCommunicationUpdate.md) |  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

