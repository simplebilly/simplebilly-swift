# VoucherAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createVoucher**](VoucherAPI.md#createvoucher) | **POST** /api/v1/vouchers | 
[**deleteVoucher**](VoucherAPI.md#deletevoucher) | **DELETE** /api/v1/vouchers/{voucher_id} | 
[**getVoucher**](VoucherAPI.md#getvoucher) | **GET** /api/v1/vouchers/{voucher_id} | 
[**listVouchers**](VoucherAPI.md#listvouchers) | **GET** /api/v1/vouchers/ | 
[**updateVoucher**](VoucherAPI.md#updatevoucher) | **PUT** /api/v1/vouchers/{voucher_id} | 
[**voucherRestore**](VoucherAPI.md#voucherrestore) | **POST** /api/v1/vouchers/{voucher_id}/restore | 


# **createVoucher**
```swift
    open class func createVoucher(voucherCreate: VoucherCreate, completion: @escaping (_ data: Voucher?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let voucherCreate = VoucherCreate(categoryId: "categoryId_example", contactId: "contactId_example", contactName: "contactName_example", currency: "currency_example", description: "description_example", fileAttachments: 123, lineItems: 123, metadata: 123, notes: "notes_example", openAmount: "openAmount_example", paidDate: Date(), paymentStatus: PaymentStatus(), taxAmounts: 123, taxCondition: "taxCondition_example", totalGrossAmount: "totalGrossAmount_example", totalNetAmount: "totalNetAmount_example", voucherDate: Date(), voucherNumber: "voucherNumber_example", voucherStatus: VoucherStatus(), voucherType: VoucherType()) // VoucherCreate | 

VoucherAPI.createVoucher(voucherCreate: voucherCreate) { (response, error) in
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
 **voucherCreate** | [**VoucherCreate**](VoucherCreate.md) |  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteVoucher**
```swift
    open class func deleteVoucher(voucherId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let voucherId = "voucherId_example" // String | 

VoucherAPI.deleteVoucher(voucherId: voucherId) { (response, error) in
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
 **voucherId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getVoucher**
```swift
    open class func getVoucher(voucherId: String, completion: @escaping (_ data: Voucher?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let voucherId = "voucherId_example" // String | 

VoucherAPI.getVoucher(voucherId: voucherId) { (response, error) in
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
 **voucherId** | **String** |  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listVouchers**
```swift
    open class func listVouchers(page: Int? = nil, pageSize: Int? = nil, voucherType: String? = nil, voucherStatus: String? = nil, contactName: String? = nil, dateFrom: Date? = nil, dateTo: Date? = nil, completion: @escaping (_ data: [Voucher]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let voucherType = "voucherType_example" // String |  (optional)
let voucherStatus = "voucherStatus_example" // String |  (optional)
let contactName = "contactName_example" // String |  (optional)
let dateFrom = Date() // Date |  (optional)
let dateTo = Date() // Date |  (optional)

VoucherAPI.listVouchers(page: page, pageSize: pageSize, voucherType: voucherType, voucherStatus: voucherStatus, contactName: contactName, dateFrom: dateFrom, dateTo: dateTo) { (response, error) in
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
 **voucherType** | **String** |  | [optional] 
 **voucherStatus** | **String** |  | [optional] 
 **contactName** | **String** |  | [optional] 
 **dateFrom** | **Date** |  | [optional] 
 **dateTo** | **Date** |  | [optional] 

### Return type

[**[Voucher]**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateVoucher**
```swift
    open class func updateVoucher(voucherId: String, body: AnyCodable, completion: @escaping (_ data: Voucher?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let voucherId = "voucherId_example" // String | 
let body =  // AnyCodable | 

VoucherAPI.updateVoucher(voucherId: voucherId, body: body) { (response, error) in
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
 **voucherId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **voucherRestore**
```swift
    open class func voucherRestore(voucherId: String, completion: @escaping (_ data: Voucher?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let voucherId = "voucherId_example" // String | 

VoucherAPI.voucherRestore(voucherId: voucherId) { (response, error) in
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
 **voucherId** | **String** |  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

