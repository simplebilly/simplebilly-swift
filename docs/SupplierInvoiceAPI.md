# SupplierInvoiceAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSupplierInvoice**](SupplierInvoiceAPI.md#createsupplierinvoice) | **POST** /api/v1/supplier-invoices | 
[**deleteSupplierInvoice**](SupplierInvoiceAPI.md#deletesupplierinvoice) | **DELETE** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**getSupplierInvoice**](SupplierInvoiceAPI.md#getsupplierinvoice) | **GET** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**listSupplierInvoices**](SupplierInvoiceAPI.md#listsupplierinvoices) | **GET** /api/v1/supplier-invoices/ | 
[**updateSupplierInvoice**](SupplierInvoiceAPI.md#updatesupplierinvoice) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**updateSupplierInvoiceStatus**](SupplierInvoiceAPI.md#updatesupplierinvoicestatus) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id}/status | 


# **createSupplierInvoice**
```swift
    open class func createSupplierInvoice(supplierInvoice: SupplierInvoice, completion: @escaping (_ data: SupplierInvoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierInvoice = SupplierInvoice(currency: "currency_example", goodsReceiptId: "goodsReceiptId_example", invoiceDate: Date(), invoiceNumber: "invoiceNumber_example", lineItems: 123, notes: "notes_example", purchaseOrderId: "purchaseOrderId_example", status: SupplierInvoiceStatus(), supplierContactId: "supplierContactId_example", supplierName: "supplierName_example", totalGrossAmount: "totalGrossAmount_example", totalNetAmount: "totalNetAmount_example") // SupplierInvoice | 

SupplierInvoiceAPI.createSupplierInvoice(supplierInvoice: supplierInvoice) { (response, error) in
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
 **supplierInvoice** | [**SupplierInvoice**](SupplierInvoice.md) |  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteSupplierInvoice**
```swift
    open class func deleteSupplierInvoice(supplierInvoiceId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierInvoiceId = "supplierInvoiceId_example" // String | 

SupplierInvoiceAPI.deleteSupplierInvoice(supplierInvoiceId: supplierInvoiceId) { (response, error) in
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
 **supplierInvoiceId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSupplierInvoice**
```swift
    open class func getSupplierInvoice(supplierInvoiceId: String, completion: @escaping (_ data: SupplierInvoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierInvoiceId = "supplierInvoiceId_example" // String | 

SupplierInvoiceAPI.getSupplierInvoice(supplierInvoiceId: supplierInvoiceId) { (response, error) in
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
 **supplierInvoiceId** | **String** |  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listSupplierInvoices**
```swift
    open class func listSupplierInvoices(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, purchaseOrderId: String? = nil, supplierName: String? = nil, completion: @escaping (_ data: [SupplierInvoice]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let purchaseOrderId = "purchaseOrderId_example" // String |  (optional)
let supplierName = "supplierName_example" // String |  (optional)

SupplierInvoiceAPI.listSupplierInvoices(page: page, pageSize: pageSize, status: status, purchaseOrderId: purchaseOrderId, supplierName: supplierName) { (response, error) in
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
 **purchaseOrderId** | **String** |  | [optional] 
 **supplierName** | **String** |  | [optional] 

### Return type

[**[SupplierInvoice]**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateSupplierInvoice**
```swift
    open class func updateSupplierInvoice(supplierInvoiceId: String, body: AnyCodable, completion: @escaping (_ data: SupplierInvoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierInvoiceId = "supplierInvoiceId_example" // String | 
let body =  // AnyCodable | 

SupplierInvoiceAPI.updateSupplierInvoice(supplierInvoiceId: supplierInvoiceId, body: body) { (response, error) in
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
 **supplierInvoiceId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateSupplierInvoiceStatus**
```swift
    open class func updateSupplierInvoiceStatus(supplierInvoiceId: String, supplierInvoiceStatusUpdate: SupplierInvoiceStatusUpdate, completion: @escaping (_ data: SupplierInvoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierInvoiceId = "supplierInvoiceId_example" // String | 
let supplierInvoiceStatusUpdate = SupplierInvoiceStatusUpdate(status: "status_example") // SupplierInvoiceStatusUpdate | 

SupplierInvoiceAPI.updateSupplierInvoiceStatus(supplierInvoiceId: supplierInvoiceId, supplierInvoiceStatusUpdate: supplierInvoiceStatusUpdate) { (response, error) in
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
 **supplierInvoiceId** | **String** |  | 
 **supplierInvoiceStatusUpdate** | [**SupplierInvoiceStatusUpdate**](SupplierInvoiceStatusUpdate.md) |  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

