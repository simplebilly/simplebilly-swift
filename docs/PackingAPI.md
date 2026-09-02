# PackingAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**completePacking**](PackingAPI.md#completepacking) | **POST** /api/v1/packing/{order_number}/complete | Mark packing as complete and transition order to shipped
[**getPackingQueue**](PackingAPI.md#getpackingqueue) | **GET** /api/v1/packing/queue | Get the packing queue - orders ready for packing
[**printDeliveryNote**](PackingAPI.md#printdeliverynote) | **POST** /api/v1/packing/{order_number}/print-delivery-note | Print delivery note (Lieferschein) for an order
[**printLabel**](PackingAPI.md#printlabel) | **POST** /api/v1/packing/{order_number}/print-label | Print shipping label for an order
[**recordPackingVideo**](PackingAPI.md#recordpackingvideo) | **POST** /api/v1/packing/{order_number}/record-video | Record video of packing process


# **completePacking**
```swift
    open class func completePacking(orderNumber: String, packingCompleteRequest: PackingCompleteRequest, completion: @escaping (_ data: PackingCompleteResponse?, _ error: Error?) -> Void)
```

Mark packing as complete and transition order to shipped

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderNumber = "orderNumber_example" // String | 
let packingCompleteRequest = PackingCompleteRequest(notes: "notes_example", orderNumber: "orderNumber_example", shipmentId: "shipmentId_example", videoUrl: "videoUrl_example") // PackingCompleteRequest | 

// Mark packing as complete and transition order to shipped
PackingAPI.completePacking(orderNumber: orderNumber, packingCompleteRequest: packingCompleteRequest) { (response, error) in
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
 **orderNumber** | **String** |  | 
 **packingCompleteRequest** | [**PackingCompleteRequest**](PackingCompleteRequest.md) |  | 

### Return type

[**PackingCompleteResponse**](PackingCompleteResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPackingQueue**
```swift
    open class func getPackingQueue(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, completion: @escaping (_ data: PackingQueue?, _ error: Error?) -> Void)
```

Get the packing queue - orders ready for packing

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)

// Get the packing queue - orders ready for packing
PackingAPI.getPackingQueue(page: page, pageSize: pageSize, search: search) { (response, error) in
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

### Return type

[**PackingQueue**](PackingQueue.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **printDeliveryNote**
```swift
    open class func printDeliveryNote(orderNumber: String, completion: @escaping (_ data: PrintDeliveryNoteResponse?, _ error: Error?) -> Void)
```

Print delivery note (Lieferschein) for an order

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderNumber = "orderNumber_example" // String | 

// Print delivery note (Lieferschein) for an order
PackingAPI.printDeliveryNote(orderNumber: orderNumber) { (response, error) in
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
 **orderNumber** | **String** |  | 

### Return type

[**PrintDeliveryNoteResponse**](PrintDeliveryNoteResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **printLabel**
```swift
    open class func printLabel(orderNumber: String, completion: @escaping (_ data: PrintLabelResponse?, _ error: Error?) -> Void)
```

Print shipping label for an order

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderNumber = "orderNumber_example" // String | 

// Print shipping label for an order
PackingAPI.printLabel(orderNumber: orderNumber) { (response, error) in
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
 **orderNumber** | **String** |  | 

### Return type

[**PrintLabelResponse**](PrintLabelResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **recordPackingVideo**
```swift
    open class func recordPackingVideo(orderNumber: String, body: AnyCodable, completion: @escaping (_ data: PackingVideoResponse?, _ error: Error?) -> Void)
```

Record video of packing process

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderNumber = "orderNumber_example" // String | 
let body =  // AnyCodable | 

// Record video of packing process
PackingAPI.recordPackingVideo(orderNumber: orderNumber, body: body) { (response, error) in
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
 **orderNumber** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**PackingVideoResponse**](PackingVideoResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

