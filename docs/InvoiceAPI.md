# InvoiceAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createInvoice**](InvoiceAPI.md#createinvoice) | **POST** /api/v1/invoices | 
[**deleteInvoice**](InvoiceAPI.md#deleteinvoice) | **DELETE** /api/v1/invoices/{id} | 
[**downloadInvoicePdf**](InvoiceAPI.md#downloadinvoicepdf) | **GET** /api/v1/invoices/{id}/pdf | 
[**getInvoice**](InvoiceAPI.md#getinvoice) | **GET** /api/v1/invoices/{id} | 
[**getInvoicePdfUrl**](InvoiceAPI.md#getinvoicepdfurl) | **GET** /api/v1/invoices/{id}/pdf-url | 
[**getInvoices**](InvoiceAPI.md#getinvoices) | **GET** /api/v1/invoices/ | 
[**invoiceRestore**](InvoiceAPI.md#invoicerestore) | **POST** /api/v1/invoices/{id}/restore | 
[**updateInvoice**](InvoiceAPI.md#updateinvoice) | **PUT** /api/v1/invoices/{id} | 


# **createInvoice**
```swift
    open class func createInvoice(invoiceCreate: InvoiceCreate, completion: @escaping (_ data: Invoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let invoiceCreate = InvoiceCreate(attachments: 123, billingPeriodEnd: Date(), billingPeriodStart: Date(), cancellationDate: Date(), cancellationInvoiceId: "cancellationInvoiceId_example", cancellationReason: "cancellationReason_example", contractId: 123, currency: CurrencyCode(), customerId: "customerId_example", discountAmount: "discountAmount_example", discountDays: 123, discountPercentage: "discountPercentage_example", documentType: DocumentType(), dunningLevel: 123, inputVatAmount: "inputVatAmount_example", inputVatDeductible: false, inputVatPercentage: "inputVatPercentage_example", introductionText: "introductionText_example", invoiceType: InvoiceType(), isCancelled: false, isDraft: false, isEuAcquisition: false, isEuDelivery: false, isIntraCommunityAcquisition: false, isReverseCharge: false, issueDate: Date(), ledgerAccount: "ledgerAccount_example", lineItems: 123, margin25a: false, margin25aGross: "margin25aGross_example", margin25aPurchasePrice: "margin25aPurchasePrice_example", notes: "notes_example", orderNumber: "orderNumber_example", originalPdfPath: "originalPdfPath_example", paidAmount: "paidAmount_example", paymentDueDate: Date(), paymentStatus: PaymentStatus(), paymentTermsText: "paymentTermsText_example", precedingSalesVoucherId: "precedingSalesVoucherId_example", precedingSalesVoucherType: PrecedingSalesVoucherType(), receiptConfirmationAvailable: false, relatedInvoiceId: 123, relationshipType: "relationshipType_example", senderSnapshot: 123, sentAt: Date(), servicePeriodEnd: Date(), servicePeriodStart: Date(), status: InvoiceStatus(), subtotal: "subtotal_example", supplierId: "supplierId_example", taxExemptionReason: "taxExemptionReason_example", totalAmount: "totalAmount_example", totalTax: "totalTax_example", vatCountry: CountryCode(), vatSpecialCase: "vatSpecialCase_example") // InvoiceCreate | 

InvoiceAPI.createInvoice(invoiceCreate: invoiceCreate) { (response, error) in
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
 **invoiceCreate** | [**InvoiceCreate**](InvoiceCreate.md) |  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteInvoice**
```swift
    open class func deleteInvoice(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = "id_example" // String | 

InvoiceAPI.deleteInvoice(id: id) { (response, error) in
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
 **id** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **downloadInvoicePdf**
```swift
    open class func downloadInvoicePdf(id: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = "id_example" // String | 

InvoiceAPI.downloadInvoicePdf(id: id) { (response, error) in
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
 **id** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getInvoice**
```swift
    open class func getInvoice(id: String, completion: @escaping (_ data: Invoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = "id_example" // String | 

InvoiceAPI.getInvoice(id: id) { (response, error) in
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
 **id** | **String** |  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getInvoicePdfUrl**
```swift
    open class func getInvoicePdfUrl(id: String, completion: @escaping (_ data: InvoicePdfUrlResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = "id_example" // String | 

InvoiceAPI.getInvoicePdfUrl(id: id) { (response, error) in
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
 **id** | **String** |  | 

### Return type

[**InvoicePdfUrlResponse**](InvoicePdfUrlResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getInvoices**
```swift
    open class func getInvoices(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Invoice]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

InvoiceAPI.getInvoices(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[Invoice]**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **invoiceRestore**
```swift
    open class func invoiceRestore(id: String, completion: @escaping (_ data: Invoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = "id_example" // String | 

InvoiceAPI.invoiceRestore(id: id) { (response, error) in
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
 **id** | **String** |  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateInvoice**
```swift
    open class func updateInvoice(id: String, body: AnyCodable, completion: @escaping (_ data: Invoice?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = "id_example" // String | 
let body =  // AnyCodable | 

InvoiceAPI.updateInvoice(id: id, body: body) { (response, error) in
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
 **id** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

