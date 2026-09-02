# ContactAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**contactSchema**](ContactAPI.md#contactschema) | **GET** /api/v1/contacts/schema | Serve JSON Schema for client-side validation
[**contactTimeline**](ContactAPI.md#contacttimeline) | **GET** /api/v1/contacts/{contact_id}/timeline | Get the full per-contact timeline (Xentral §4.6/4.7).
[**createContact**](ContactAPI.md#createcontact) | **POST** /api/v1/contacts | Create contact
[**deleteContact**](ContactAPI.md#deletecontact) | **DELETE** /api/v1/contacts/{contact_id} | Soft-delete contact
[**getContact**](ContactAPI.md#getcontact) | **GET** /api/v1/contacts/{contact_id} | Get single contact
[**listContacts**](ContactAPI.md#listcontacts) | **GET** /api/v1/contacts | List contacts with search, type filter, and pagination
[**salesVolume**](ContactAPI.md#salesvolume) | **GET** /api/v1/contacts/sales-volume | Sales volume per contact
[**updateContact**](ContactAPI.md#updatecontact) | **PUT** /api/v1/contacts/{contact_id} | Update contact


# **contactSchema**
```swift
    open class func contactSchema(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Serve JSON Schema for client-side validation

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Serve JSON Schema for client-side validation
ContactAPI.contactSchema() { (response, error) in
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

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contactTimeline**
```swift
    open class func contactTimeline(contactId: String, completion: @escaping (_ data: ContactTimelineResponse?, _ error: Error?) -> Void)
```

Get the full per-contact timeline (Xentral §4.6/4.7).

Aggregates communications, quotations, orders, invoices and uploaded documents for a contact, merged into a single reverse-chronological feed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let contactId = "contactId_example" // String | 

// Get the full per-contact timeline (Xentral §4.6/4.7).
ContactAPI.contactTimeline(contactId: contactId) { (response, error) in
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

[**ContactTimelineResponse**](ContactTimelineResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createContact**
```swift
    open class func createContact(body: AnyCodable, completion: @escaping (_ data: Contact?, _ error: Error?) -> Void)
```

Create contact

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let body =  // AnyCodable | 

// Create contact
ContactAPI.createContact(body: body) { (response, error) in
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
 **body** | **AnyCodable** |  | 

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteContact**
```swift
    open class func deleteContact(contactId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Soft-delete contact

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let contactId = "contactId_example" // String | 

// Soft-delete contact
ContactAPI.deleteContact(contactId: contactId) { (response, error) in
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

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getContact**
```swift
    open class func getContact(contactId: String, completion: @escaping (_ data: Contact?, _ error: Error?) -> Void)
```

Get single contact

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let contactId = "contactId_example" // String | 

// Get single contact
ContactAPI.getContact(contactId: contactId) { (response, error) in
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

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listContacts**
```swift
    open class func listContacts(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, contactType: String? = nil, tag: String? = nil, completion: @escaping (_ data: [Contact]?, _ error: Error?) -> Void)
```

List contacts with search, type filter, and pagination

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let contactType = "contactType_example" // String |  (optional)
let tag = "tag_example" // String |  (optional)

// List contacts with search, type filter, and pagination
ContactAPI.listContacts(page: page, pageSize: pageSize, search: search, contactType: contactType, tag: tag) { (response, error) in
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
 **search** | **String** |  | [optional] 
 **contactType** | **String** |  | [optional] 
 **tag** | **String** |  | [optional] 

### Return type

[**[Contact]**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **salesVolume**
```swift
    open class func salesVolume(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, contactType: String? = nil, tag: String? = nil, completion: @escaping (_ data: SalesVolumeReport?, _ error: Error?) -> Void)
```

Sales volume per contact

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let contactType = "contactType_example" // String |  (optional)
let tag = "tag_example" // String |  (optional)

// Sales volume per contact
ContactAPI.salesVolume(page: page, pageSize: pageSize, search: search, contactType: contactType, tag: tag) { (response, error) in
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
 **search** | **String** |  | [optional] 
 **contactType** | **String** |  | [optional] 
 **tag** | **String** |  | [optional] 

### Return type

[**SalesVolumeReport**](SalesVolumeReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateContact**
```swift
    open class func updateContact(contactId: String, body: AnyCodable, completion: @escaping (_ data: Contact?, _ error: Error?) -> Void)
```

Update contact

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let contactId = "contactId_example" // String | 
let body =  // AnyCodable | 

// Update contact
ContactAPI.updateContact(contactId: contactId, body: body) { (response, error) in
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
 **body** | **AnyCodable** |  | 

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

