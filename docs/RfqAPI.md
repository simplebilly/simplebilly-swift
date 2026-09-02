# RfqAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convertRfq**](RfqAPI.md#convertrfq) | **POST** /api/v1/rfqs/{rfq_id}/convert | Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as &#x60;converted&#x60;.
[**createRfq**](RfqAPI.md#createrfq) | **POST** /api/v1/rfqs | 
[**deleteRfq**](RfqAPI.md#deleterfq) | **DELETE** /api/v1/rfqs/{rfq_id} | 
[**getRfq**](RfqAPI.md#getrfq) | **GET** /api/v1/rfqs/{rfq_id} | 
[**listRfqs**](RfqAPI.md#listrfqs) | **GET** /api/v1/rfqs/ | 
[**updateRfq**](RfqAPI.md#updaterfq) | **PUT** /api/v1/rfqs/{rfq_id} | 
[**updateRfqStatus**](RfqAPI.md#updaterfqstatus) | **PUT** /api/v1/rfqs/{rfq_id}/status | 


# **convertRfq**
```swift
    open class func convertRfq(rfqId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let rfqId = "rfqId_example" // String | 

// Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.
RfqAPI.convertRfq(rfqId: rfqId) { (response, error) in
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
 **rfqId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createRfq**
```swift
    open class func createRfq(rfq: Rfq, completion: @escaping (_ data: Rfq?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let rfq = Rfq(currency: "currency_example", lineItems: 123, notes: "notes_example", requestedDate: Date(), responseDate: Date(), rfqNumber: "rfqNumber_example", status: RfqStatus(), supplierContactId: "supplierContactId_example", supplierName: "supplierName_example") // Rfq | 

RfqAPI.createRfq(rfq: rfq) { (response, error) in
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
 **rfq** | [**Rfq**](Rfq.md) |  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteRfq**
```swift
    open class func deleteRfq(rfqId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let rfqId = "rfqId_example" // String | 

RfqAPI.deleteRfq(rfqId: rfqId) { (response, error) in
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
 **rfqId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRfq**
```swift
    open class func getRfq(rfqId: String, completion: @escaping (_ data: Rfq?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let rfqId = "rfqId_example" // String | 

RfqAPI.getRfq(rfqId: rfqId) { (response, error) in
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
 **rfqId** | **String** |  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRfqs**
```swift
    open class func listRfqs(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, supplierName: String? = nil, completion: @escaping (_ data: [Rfq]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let supplierName = "supplierName_example" // String |  (optional)

RfqAPI.listRfqs(page: page, pageSize: pageSize, status: status, supplierName: supplierName) { (response, error) in
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

### Return type

[**[Rfq]**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateRfq**
```swift
    open class func updateRfq(rfqId: String, body: AnyCodable, completion: @escaping (_ data: Rfq?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let rfqId = "rfqId_example" // String | 
let body =  // AnyCodable | 

RfqAPI.updateRfq(rfqId: rfqId, body: body) { (response, error) in
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
 **rfqId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateRfqStatus**
```swift
    open class func updateRfqStatus(rfqId: String, rfqStatusUpdate: RfqStatusUpdate, completion: @escaping (_ data: Rfq?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let rfqId = "rfqId_example" // String | 
let rfqStatusUpdate = RfqStatusUpdate(status: "status_example") // RfqStatusUpdate | 

RfqAPI.updateRfqStatus(rfqId: rfqId, rfqStatusUpdate: rfqStatusUpdate) { (response, error) in
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
 **rfqId** | **String** |  | 
 **rfqStatusUpdate** | [**RfqStatusUpdate**](RfqStatusUpdate.md) |  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

