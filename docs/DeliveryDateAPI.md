# DeliveryDateAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDeliveryDate**](DeliveryDateAPI.md#createdeliverydate) | **POST** /api/v1/delivery-dates | 
[**deleteDeliveryDate**](DeliveryDateAPI.md#deletedeliverydate) | **DELETE** /api/v1/delivery-dates/{delivery_date_id} | 
[**getDeliveryDate**](DeliveryDateAPI.md#getdeliverydate) | **GET** /api/v1/delivery-dates/{delivery_date_id} | 
[**getDeliveryPerformance**](DeliveryDateAPI.md#getdeliveryperformance) | **GET** /api/v1/delivery-dates/performance | On-time performance summary: how many promised delivery dates were met within a period.
[**listDeliveryDates**](DeliveryDateAPI.md#listdeliverydates) | **GET** /api/v1/delivery-dates/ | 
[**updateDeliveryDate**](DeliveryDateAPI.md#updatedeliverydate) | **PUT** /api/v1/delivery-dates/{delivery_date_id} | 
[**updateDeliveryDateStatus**](DeliveryDateAPI.md#updatedeliverydatestatus) | **PUT** /api/v1/delivery-dates/{delivery_date_id}/status | 


# **createDeliveryDate**
```swift
    open class func createDeliveryDate(deliveryDateCreate: DeliveryDateCreate, completion: @escaping (_ data: DeliveryDate?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryDateCreate = DeliveryDateCreate(customerId: "customerId_example", fulfilledDate: Date(), note: "note_example", orderNumber: "orderNumber_example", originalDate: Date(), productId: "productId_example", promisedDate: Date(), status: DeliveryDateStatus()) // DeliveryDateCreate | 

DeliveryDateAPI.createDeliveryDate(deliveryDateCreate: deliveryDateCreate) { (response, error) in
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
 **deliveryDateCreate** | [**DeliveryDateCreate**](DeliveryDateCreate.md) |  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteDeliveryDate**
```swift
    open class func deleteDeliveryDate(deliveryDateId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryDateId = "deliveryDateId_example" // String | 

DeliveryDateAPI.deleteDeliveryDate(deliveryDateId: deliveryDateId) { (response, error) in
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
 **deliveryDateId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDeliveryDate**
```swift
    open class func getDeliveryDate(deliveryDateId: String, completion: @escaping (_ data: DeliveryDate?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryDateId = "deliveryDateId_example" // String | 

DeliveryDateAPI.getDeliveryDate(deliveryDateId: deliveryDateId) { (response, error) in
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
 **deliveryDateId** | **String** |  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDeliveryPerformance**
```swift
    open class func getDeliveryPerformance(page: Int? = nil, pageSize: Int? = nil, orderNumber: String? = nil, status: String? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

On-time performance summary: how many promised delivery dates were met within a period.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let orderNumber = "orderNumber_example" // String |  (optional)
let status = "status_example" // String |  (optional)
let from = Date() // Date | Only dates on or after this date. (optional)
let to = Date() // Date | Only dates on or before this date. (optional)

// On-time performance summary: how many promised delivery dates were met within a period.
DeliveryDateAPI.getDeliveryPerformance(page: page, pageSize: pageSize, orderNumber: orderNumber, status: status, from: from, to: to) { (response, error) in
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
 **orderNumber** | **String** |  | [optional] 
 **status** | **String** |  | [optional] 
 **from** | **Date** | Only dates on or after this date. | [optional] 
 **to** | **Date** | Only dates on or before this date. | [optional] 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listDeliveryDates**
```swift
    open class func listDeliveryDates(page: Int? = nil, pageSize: Int? = nil, orderNumber: String? = nil, status: String? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [DeliveryDate]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let orderNumber = "orderNumber_example" // String |  (optional)
let status = "status_example" // String |  (optional)
let from = Date() // Date | Only dates on or after this date. (optional)
let to = Date() // Date | Only dates on or before this date. (optional)

DeliveryDateAPI.listDeliveryDates(page: page, pageSize: pageSize, orderNumber: orderNumber, status: status, from: from, to: to) { (response, error) in
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
 **orderNumber** | **String** |  | [optional] 
 **status** | **String** |  | [optional] 
 **from** | **Date** | Only dates on or after this date. | [optional] 
 **to** | **Date** | Only dates on or before this date. | [optional] 

### Return type

[**[DeliveryDate]**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateDeliveryDate**
```swift
    open class func updateDeliveryDate(deliveryDateId: String, body: AnyCodable, completion: @escaping (_ data: DeliveryDate?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryDateId = "deliveryDateId_example" // String | 
let body =  // AnyCodable | 

DeliveryDateAPI.updateDeliveryDate(deliveryDateId: deliveryDateId, body: body) { (response, error) in
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
 **deliveryDateId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateDeliveryDateStatus**
```swift
    open class func updateDeliveryDateStatus(deliveryDateId: String, deliveryDateStatusUpdate: DeliveryDateStatusUpdate, completion: @escaping (_ data: DeliveryDate?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryDateId = "deliveryDateId_example" // String | 
let deliveryDateStatusUpdate = DeliveryDateStatusUpdate(status: "status_example") // DeliveryDateStatusUpdate | 

DeliveryDateAPI.updateDeliveryDateStatus(deliveryDateId: deliveryDateId, deliveryDateStatusUpdate: deliveryDateStatusUpdate) { (response, error) in
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
 **deliveryDateId** | **String** |  | 
 **deliveryDateStatusUpdate** | [**DeliveryDateStatusUpdate**](DeliveryDateStatusUpdate.md) |  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

