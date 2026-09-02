# PurchaseOrderAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPurchaseOrder**](PurchaseOrderAPI.md#createpurchaseorder) | **POST** /api/v1/purchase-orders | 
[**deletePurchaseOrder**](PurchaseOrderAPI.md#deletepurchaseorder) | **DELETE** /api/v1/purchase-orders/{purchase_order_id} | 
[**getPurchaseOrder**](PurchaseOrderAPI.md#getpurchaseorder) | **GET** /api/v1/purchase-orders/{purchase_order_id} | 
[**listPurchaseOrders**](PurchaseOrderAPI.md#listpurchaseorders) | **GET** /api/v1/purchase-orders/ | 
[**matchInvoice**](PurchaseOrderAPI.md#matchinvoice) | **POST** /api/v1/purchase-orders/{purchase_order_id}/match-invoice | 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
[**updatePurchaseOrder**](PurchaseOrderAPI.md#updatepurchaseorder) | **PUT** /api/v1/purchase-orders/{purchase_order_id} | 
[**updatePurchaseOrderStatus**](PurchaseOrderAPI.md#updatepurchaseorderstatus) | **PUT** /api/v1/purchase-orders/{purchase_order_id}/status | 


# **createPurchaseOrder**
```swift
    open class func createPurchaseOrder(purchaseOrder: PurchaseOrder, completion: @escaping (_ data: PurchaseOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let purchaseOrder = PurchaseOrder(currency: "currency_example", deliveryAddress: 123, expectedDeliveryDate: Date(), lineItems: 123, notes: "notes_example", orderDate: Date(), poNumber: "poNumber_example", status: PurchaseOrderStatus(), supplierContactId: "supplierContactId_example", supplierName: "supplierName_example", totalGrossAmount: "totalGrossAmount_example", totalNetAmount: "totalNetAmount_example") // PurchaseOrder | 

PurchaseOrderAPI.createPurchaseOrder(purchaseOrder: purchaseOrder) { (response, error) in
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
 **purchaseOrder** | [**PurchaseOrder**](PurchaseOrder.md) |  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePurchaseOrder**
```swift
    open class func deletePurchaseOrder(purchaseOrderId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let purchaseOrderId = "purchaseOrderId_example" // String | 

PurchaseOrderAPI.deletePurchaseOrder(purchaseOrderId: purchaseOrderId) { (response, error) in
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
 **purchaseOrderId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPurchaseOrder**
```swift
    open class func getPurchaseOrder(purchaseOrderId: String, completion: @escaping (_ data: PurchaseOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let purchaseOrderId = "purchaseOrderId_example" // String | 

PurchaseOrderAPI.getPurchaseOrder(purchaseOrderId: purchaseOrderId) { (response, error) in
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
 **purchaseOrderId** | **String** |  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPurchaseOrders**
```swift
    open class func listPurchaseOrders(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, supplierName: String? = nil, search: String? = nil, completion: @escaping (_ data: [PurchaseOrder]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let supplierName = "supplierName_example" // String |  (optional)
let search = "search_example" // String |  (optional)

PurchaseOrderAPI.listPurchaseOrders(page: page, pageSize: pageSize, status: status, supplierName: supplierName, search: search) { (response, error) in
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
 **supplierName** | **String** |  | [optional] 
 **search** | **String** |  | [optional] 

### Return type

[**[PurchaseOrder]**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **matchInvoice**
```swift
    open class func matchInvoice(purchaseOrderId: String, invoiceMatchRequest: InvoiceMatchRequest, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let purchaseOrderId = "purchaseOrderId_example" // String | 
let invoiceMatchRequest = InvoiceMatchRequest(supplierInvoiceId: "supplierInvoiceId_example") // InvoiceMatchRequest | 

// 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
PurchaseOrderAPI.matchInvoice(purchaseOrderId: purchaseOrderId, invoiceMatchRequest: invoiceMatchRequest) { (response, error) in
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
 **purchaseOrderId** | **String** |  | 
 **invoiceMatchRequest** | [**InvoiceMatchRequest**](InvoiceMatchRequest.md) |  | 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePurchaseOrder**
```swift
    open class func updatePurchaseOrder(purchaseOrderId: String, body: AnyCodable, completion: @escaping (_ data: PurchaseOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let purchaseOrderId = "purchaseOrderId_example" // String | 
let body =  // AnyCodable | 

PurchaseOrderAPI.updatePurchaseOrder(purchaseOrderId: purchaseOrderId, body: body) { (response, error) in
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
 **purchaseOrderId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePurchaseOrderStatus**
```swift
    open class func updatePurchaseOrderStatus(purchaseOrderId: String, purchaseOrderStatusUpdate: PurchaseOrderStatusUpdate, completion: @escaping (_ data: PurchaseOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let purchaseOrderId = "purchaseOrderId_example" // String | 
let purchaseOrderStatusUpdate = PurchaseOrderStatusUpdate(status: "status_example") // PurchaseOrderStatusUpdate | 

PurchaseOrderAPI.updatePurchaseOrderStatus(purchaseOrderId: purchaseOrderId, purchaseOrderStatusUpdate: purchaseOrderStatusUpdate) { (response, error) in
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
 **purchaseOrderId** | **String** |  | 
 **purchaseOrderStatusUpdate** | [**PurchaseOrderStatusUpdate**](PurchaseOrderStatusUpdate.md) |  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

