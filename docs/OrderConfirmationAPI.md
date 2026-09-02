# OrderConfirmationAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createConfirmation**](OrderConfirmationAPI.md#createconfirmation) | **POST** /api/v1/order-confirmations | 
[**deleteConfirmation**](OrderConfirmationAPI.md#deleteconfirmation) | **DELETE** /api/v1/order-confirmations/{confirmation_id} | 
[**downloadConfirmationPdf**](OrderConfirmationAPI.md#downloadconfirmationpdf) | **GET** /api/v1/order-confirmations/{confirmation_id}/pdf | 
[**getConfirmation**](OrderConfirmationAPI.md#getconfirmation) | **GET** /api/v1/order-confirmations/{confirmation_id} | 
[**listConfirmations**](OrderConfirmationAPI.md#listconfirmations) | **GET** /api/v1/order-confirmations/ | 
[**orderconfirmationRestore**](OrderConfirmationAPI.md#orderconfirmationrestore) | **POST** /api/v1/order-confirmations/{confirmation_id}/restore | 
[**pursueConfirmation**](OrderConfirmationAPI.md#pursueconfirmation) | **POST** /api/v1/order-confirmations/{confirmation_id}/pursue | 


# **createConfirmation**
```swift
    open class func createConfirmation(orderConfirmationCreate: OrderConfirmationCreate, completion: @escaping (_ data: OrderConfirmation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderConfirmationCreate = OrderConfirmationCreate(address: 123, confirmationNumber: "confirmationNumber_example", contactId: "contactId_example", contactName: "contactName_example", currency: "currency_example", files: 123, introduction: "introduction_example", lineItems: 123, precedingSalesVoucherId: "precedingSalesVoucherId_example", precedingSalesVoucherType: PrecedingSalesVoucherType(), remark: "remark_example", taxCondition: "taxCondition_example", title: "title_example", voucherDate: Date(), voucherStatus: VoucherStatus()) // OrderConfirmationCreate | 

OrderConfirmationAPI.createConfirmation(orderConfirmationCreate: orderConfirmationCreate) { (response, error) in
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
 **orderConfirmationCreate** | [**OrderConfirmationCreate**](OrderConfirmationCreate.md) |  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteConfirmation**
```swift
    open class func deleteConfirmation(confirmationId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let confirmationId = "confirmationId_example" // String | 

OrderConfirmationAPI.deleteConfirmation(confirmationId: confirmationId) { (response, error) in
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
 **confirmationId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **downloadConfirmationPdf**
```swift
    open class func downloadConfirmationPdf(confirmationId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let confirmationId = "confirmationId_example" // String | 

OrderConfirmationAPI.downloadConfirmationPdf(confirmationId: confirmationId) { (response, error) in
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
 **confirmationId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getConfirmation**
```swift
    open class func getConfirmation(confirmationId: String, completion: @escaping (_ data: OrderConfirmation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let confirmationId = "confirmationId_example" // String | 

OrderConfirmationAPI.getConfirmation(confirmationId: confirmationId) { (response, error) in
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
 **confirmationId** | **String** |  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listConfirmations**
```swift
    open class func listConfirmations(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [OrderConfirmation]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

OrderConfirmationAPI.listConfirmations(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[OrderConfirmation]**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderconfirmationRestore**
```swift
    open class func orderconfirmationRestore(confirmationId: String, completion: @escaping (_ data: OrderConfirmation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let confirmationId = "confirmationId_example" // String | 

OrderConfirmationAPI.orderconfirmationRestore(confirmationId: confirmationId) { (response, error) in
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
 **confirmationId** | **String** |  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pursueConfirmation**
```swift
    open class func pursueConfirmation(confirmationId: String, completion: @escaping (_ data: DeliveryNote?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let confirmationId = "confirmationId_example" // String | 

OrderConfirmationAPI.pursueConfirmation(confirmationId: confirmationId) { (response, error) in
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
 **confirmationId** | **String** |  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

