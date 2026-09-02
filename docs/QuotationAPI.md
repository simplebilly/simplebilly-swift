# QuotationAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createQuotation**](QuotationAPI.md#createquotation) | **POST** /api/v1/quotations | 
[**deleteQuotation**](QuotationAPI.md#deletequotation) | **DELETE** /api/v1/quotations/{quotation_id} | 
[**downloadQuotationPdf**](QuotationAPI.md#downloadquotationpdf) | **GET** /api/v1/quotations/{quotation_id}/pdf | 
[**getQuotation**](QuotationAPI.md#getquotation) | **GET** /api/v1/quotations/{quotation_id} | 
[**listQuotations**](QuotationAPI.md#listquotations) | **GET** /api/v1/quotations/ | 
[**pursueQuotation**](QuotationAPI.md#pursuequotation) | **POST** /api/v1/quotations/{quotation_id}/pursue | 
[**quotationRestore**](QuotationAPI.md#quotationrestore) | **POST** /api/v1/quotations/{quotation_id}/restore | 
[**updateQuotation**](QuotationAPI.md#updatequotation) | **PUT** /api/v1/quotations/{quotation_id} | 


# **createQuotation**
```swift
    open class func createQuotation(quotationCreate: QuotationCreate, completion: @escaping (_ data: Quotation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotationCreate = QuotationCreate(address: 123, contactId: "contactId_example", contactName: "contactName_example", currency: "currency_example", expirationDate: Date(), files: 123, introduction: "introduction_example", lineItems: 123, precedingSalesVoucherId: "precedingSalesVoucherId_example", precedingSalesVoucherType: PrecedingSalesVoucherType(), quotationNumber: "quotationNumber_example", remark: "remark_example", taxCondition: "taxCondition_example", title: "title_example", voucherDate: Date(), voucherStatus: VoucherStatus()) // QuotationCreate | 

QuotationAPI.createQuotation(quotationCreate: quotationCreate) { (response, error) in
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
 **quotationCreate** | [**QuotationCreate**](QuotationCreate.md) |  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteQuotation**
```swift
    open class func deleteQuotation(quotationId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotationId = "quotationId_example" // String | 

QuotationAPI.deleteQuotation(quotationId: quotationId) { (response, error) in
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
 **quotationId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **downloadQuotationPdf**
```swift
    open class func downloadQuotationPdf(quotationId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotationId = "quotationId_example" // String | 

QuotationAPI.downloadQuotationPdf(quotationId: quotationId) { (response, error) in
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
 **quotationId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getQuotation**
```swift
    open class func getQuotation(quotationId: String, completion: @escaping (_ data: Quotation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotationId = "quotationId_example" // String | 

QuotationAPI.getQuotation(quotationId: quotationId) { (response, error) in
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
 **quotationId** | **String** |  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listQuotations**
```swift
    open class func listQuotations(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Quotation]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

QuotationAPI.listQuotations(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[Quotation]**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pursueQuotation**
```swift
    open class func pursueQuotation(quotationId: String, completion: @escaping (_ data: OrderConfirmation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotationId = "quotationId_example" // String | 

QuotationAPI.pursueQuotation(quotationId: quotationId) { (response, error) in
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
 **quotationId** | **String** |  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **quotationRestore**
```swift
    open class func quotationRestore(quotationId: String, completion: @escaping (_ data: Quotation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotationId = "quotationId_example" // String | 

QuotationAPI.quotationRestore(quotationId: quotationId) { (response, error) in
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
 **quotationId** | **String** |  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateQuotation**
```swift
    open class func updateQuotation(quotationId: String, body: AnyCodable, completion: @escaping (_ data: Quotation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotationId = "quotationId_example" // String | 
let body =  // AnyCodable | 

QuotationAPI.updateQuotation(quotationId: quotationId, body: body) { (response, error) in
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
 **quotationId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

