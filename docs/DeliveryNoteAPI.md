# DeliveryNoteAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDeliveryNote**](DeliveryNoteAPI.md#createdeliverynote) | **POST** /api/v1/delivery-notes | 
[**deleteDeliveryNote**](DeliveryNoteAPI.md#deletedeliverynote) | **DELETE** /api/v1/delivery-notes/{delivery_note_id} | 
[**deliverynoteRestore**](DeliveryNoteAPI.md#deliverynoterestore) | **POST** /api/v1/delivery-notes/{delivery_note_id}/restore | 
[**downloadDeliveryNotePdf**](DeliveryNoteAPI.md#downloaddeliverynotepdf) | **GET** /api/v1/delivery-notes/{delivery_note_id}/pdf | 
[**getDeliveryNote**](DeliveryNoteAPI.md#getdeliverynote) | **GET** /api/v1/delivery-notes/{delivery_note_id} | 
[**listDeliveryNotes**](DeliveryNoteAPI.md#listdeliverynotes) | **GET** /api/v1/delivery-notes/ | 
[**pursueDeliveryNote**](DeliveryNoteAPI.md#pursuedeliverynote) | **POST** /api/v1/delivery-notes/{delivery_note_id}/pursue | 


# **createDeliveryNote**
```swift
    open class func createDeliveryNote(deliveryNoteCreate: DeliveryNoteCreate, completion: @escaping (_ data: DeliveryNote?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryNoteCreate = DeliveryNoteCreate(address: 123, contactId: "contactId_example", contactName: "contactName_example", currency: "currency_example", deliveryDate: Date(), deliveryNoteNumber: "deliveryNoteNumber_example", files: 123, introduction: "introduction_example", lineItems: 123, precedingSalesVoucherId: "precedingSalesVoucherId_example", precedingSalesVoucherType: PrecedingSalesVoucherType(), remark: "remark_example", shippingDate: Date(), shippingMethod: "shippingMethod_example", title: "title_example", voucherDate: Date(), voucherStatus: VoucherStatus()) // DeliveryNoteCreate | 

DeliveryNoteAPI.createDeliveryNote(deliveryNoteCreate: deliveryNoteCreate) { (response, error) in
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
 **deliveryNoteCreate** | [**DeliveryNoteCreate**](DeliveryNoteCreate.md) |  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteDeliveryNote**
```swift
    open class func deleteDeliveryNote(deliveryNoteId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryNoteId = "deliveryNoteId_example" // String | 

DeliveryNoteAPI.deleteDeliveryNote(deliveryNoteId: deliveryNoteId) { (response, error) in
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
 **deliveryNoteId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deliverynoteRestore**
```swift
    open class func deliverynoteRestore(deliveryNoteId: String, completion: @escaping (_ data: DeliveryNote?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryNoteId = "deliveryNoteId_example" // String | 

DeliveryNoteAPI.deliverynoteRestore(deliveryNoteId: deliveryNoteId) { (response, error) in
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
 **deliveryNoteId** | **String** |  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **downloadDeliveryNotePdf**
```swift
    open class func downloadDeliveryNotePdf(deliveryNoteId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryNoteId = "deliveryNoteId_example" // String | 

DeliveryNoteAPI.downloadDeliveryNotePdf(deliveryNoteId: deliveryNoteId) { (response, error) in
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
 **deliveryNoteId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDeliveryNote**
```swift
    open class func getDeliveryNote(deliveryNoteId: String, completion: @escaping (_ data: DeliveryNote?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryNoteId = "deliveryNoteId_example" // String | 

DeliveryNoteAPI.getDeliveryNote(deliveryNoteId: deliveryNoteId) { (response, error) in
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
 **deliveryNoteId** | **String** |  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listDeliveryNotes**
```swift
    open class func listDeliveryNotes(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [DeliveryNote]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

DeliveryNoteAPI.listDeliveryNotes(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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
 **includeDeleted** | **Bool** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**[DeliveryNote]**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pursueDeliveryNote**
```swift
    open class func pursueDeliveryNote(deliveryNoteId: String, completion: @escaping (_ data: Invoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryNoteId = "deliveryNoteId_example" // String | 

DeliveryNoteAPI.pursueDeliveryNote(deliveryNoteId: deliveryNoteId) { (response, error) in
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
 **deliveryNoteId** | **String** |  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

