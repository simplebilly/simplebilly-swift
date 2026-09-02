# ProformaInvoiceAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convertProformaToInvoice**](ProformaInvoiceAPI.md#convertproformatoinvoice) | **POST** /api/v1/proforma-invoices/{proforma_id}/convert | 
[**createProformaInvoice**](ProformaInvoiceAPI.md#createproformainvoice) | **POST** /api/v1/proforma-invoices | 
[**deleteProformaInvoice**](ProformaInvoiceAPI.md#deleteproformainvoice) | **DELETE** /api/v1/proforma-invoices/{proforma_id} | 
[**getProformaInvoice**](ProformaInvoiceAPI.md#getproformainvoice) | **GET** /api/v1/proforma-invoices/{proforma_id} | 
[**listProformaInvoices**](ProformaInvoiceAPI.md#listproformainvoices) | **GET** /api/v1/proforma-invoices/ | 
[**updateProformaInvoice**](ProformaInvoiceAPI.md#updateproformainvoice) | **PUT** /api/v1/proforma-invoices/{proforma_id} | 


# **convertProformaToInvoice**
```swift
    open class func convertProformaToInvoice(proformaId: String, completion: @escaping (_ data: ConvertResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let proformaId = "proformaId_example" // String | 

ProformaInvoiceAPI.convertProformaToInvoice(proformaId: proformaId) { (response, error) in
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
 **proformaId** | **String** |  | 

### Return type

[**ConvertResponse**](ConvertResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createProformaInvoice**
```swift
    open class func createProformaInvoice(proformaInvoice: ProformaInvoice, completion: @escaping (_ data: ProformaInvoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let proformaInvoice = ProformaInvoice(convertedAt: Date(), convertedToInvoiceId: "convertedToInvoiceId_example", currency: CurrencyCode(), customerId: "customerId_example", customerSnapshot: 123, issueDate: Date(), lineItems: 123, notes: "notes_example", orderNumber: "orderNumber_example", paymentDueDate: Date(), quotationId: "quotationId_example", status: ProformaInvoiceStatus(), subtotal: "subtotal_example", totalAmount: "totalAmount_example", totalTax: "totalTax_example") // ProformaInvoice | 

ProformaInvoiceAPI.createProformaInvoice(proformaInvoice: proformaInvoice) { (response, error) in
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
 **proformaInvoice** | [**ProformaInvoice**](ProformaInvoice.md) |  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProformaInvoice**
```swift
    open class func deleteProformaInvoice(proformaId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let proformaId = "proformaId_example" // String | 

ProformaInvoiceAPI.deleteProformaInvoice(proformaId: proformaId) { (response, error) in
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
 **proformaId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProformaInvoice**
```swift
    open class func getProformaInvoice(proformaId: String, completion: @escaping (_ data: ProformaInvoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let proformaId = "proformaId_example" // String | 

ProformaInvoiceAPI.getProformaInvoice(proformaId: proformaId) { (response, error) in
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
 **proformaId** | **String** |  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProformaInvoices**
```swift
    open class func listProformaInvoices(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, customerId: String? = nil, orderNumber: String? = nil, completion: @escaping (_ data: [ProformaInvoice]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let customerId = "customerId_example" // String |  (optional)
let orderNumber = "orderNumber_example" // String |  (optional)

ProformaInvoiceAPI.listProformaInvoices(page: page, pageSize: pageSize, status: status, customerId: customerId, orderNumber: orderNumber) { (response, error) in
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
 **status** | **String** |  | [optional] 
 **customerId** | **String** |  | [optional] 
 **orderNumber** | **String** |  | [optional] 

### Return type

[**[ProformaInvoice]**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProformaInvoice**
```swift
    open class func updateProformaInvoice(proformaId: String, body: AnyCodable, completion: @escaping (_ data: ProformaInvoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let proformaId = "proformaId_example" // String | 
let body =  // AnyCodable | 

ProformaInvoiceAPI.updateProformaInvoice(proformaId: proformaId, body: body) { (response, error) in
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
 **proformaId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

