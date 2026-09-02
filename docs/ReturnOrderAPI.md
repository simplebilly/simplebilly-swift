# ReturnOrderAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createReturnOrder**](ReturnOrderAPI.md#createreturnorder) | **POST** /api/v1/returns | 
[**deleteReturnOrder**](ReturnOrderAPI.md#deletereturnorder) | **DELETE** /api/v1/returns/{return_order_id} | 
[**getReturnOrder**](ReturnOrderAPI.md#getreturnorder) | **GET** /api/v1/returns/{return_order_id} | 
[**listReturnOrders**](ReturnOrderAPI.md#listreturnorders) | **GET** /api/v1/returns/ | 
[**returnLogisticsQueue**](ReturnOrderAPI.md#returnlogisticsqueue) | **GET** /api/v1/returns/logistics-queue | 
[**returnLogisticsSummary**](ReturnOrderAPI.md#returnlogisticssummary) | **GET** /api/v1/returns/logistics-summary | Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
[**updateReturnOrder**](ReturnOrderAPI.md#updatereturnorder) | **PUT** /api/v1/returns/{return_order_id} | 
[**updateReturnOrderStatus**](ReturnOrderAPI.md#updatereturnorderstatus) | **PUT** /api/v1/returns/{return_order_id}/status | 


# **createReturnOrder**
```swift
    open class func createReturnOrder(returnOrder: ReturnOrder, completion: @escaping (_ data: ReturnOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let returnOrder = ReturnOrder(customerContactId: "customerContactId_example", customerName: "customerName_example", lineItems: 123, notes: "notes_example", orderId: "orderId_example", orderNumber: "orderNumber_example", returnNumber: "returnNumber_example", returnReason: "returnReason_example", status: ReturnOrderStatus(), warehouseId: "warehouseId_example") // ReturnOrder | 

ReturnOrderAPI.createReturnOrder(returnOrder: returnOrder) { (response, error) in
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
 **returnOrder** | [**ReturnOrder**](ReturnOrder.md) |  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteReturnOrder**
```swift
    open class func deleteReturnOrder(returnOrderId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let returnOrderId = "returnOrderId_example" // String | 

ReturnOrderAPI.deleteReturnOrder(returnOrderId: returnOrderId) { (response, error) in
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
 **returnOrderId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getReturnOrder**
```swift
    open class func getReturnOrder(returnOrderId: String, completion: @escaping (_ data: ReturnOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let returnOrderId = "returnOrderId_example" // String | 

ReturnOrderAPI.getReturnOrder(returnOrderId: returnOrderId) { (response, error) in
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
 **returnOrderId** | **String** |  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listReturnOrders**
```swift
    open class func listReturnOrders(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, customerName: String? = nil, orderNumber: String? = nil, completion: @escaping (_ data: [ReturnOrder]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let customerName = "customerName_example" // String |  (optional)
let orderNumber = "orderNumber_example" // String |  (optional)

ReturnOrderAPI.listReturnOrders(page: page, pageSize: pageSize, status: status, customerName: customerName, orderNumber: orderNumber) { (response, error) in
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
 **customerName** | **String** |  | [optional] 
 **orderNumber** | **String** |  | [optional] 

### Return type

[**[ReturnOrder]**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **returnLogisticsQueue**
```swift
    open class func returnLogisticsQueue(completion: @escaping (_ data: [ReturnLogisticsQueueItem]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


ReturnOrderAPI.returnLogisticsQueue() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

[**[ReturnLogisticsQueueItem]**](ReturnLogisticsQueueItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **returnLogisticsSummary**
```swift
    open class func returnLogisticsSummary(completion: @escaping (_ data: ReturnLogisticsSummary?, _ error: Error?) -> Void)
```

Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
ReturnOrderAPI.returnLogisticsSummary() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

[**ReturnLogisticsSummary**](ReturnLogisticsSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateReturnOrder**
```swift
    open class func updateReturnOrder(returnOrderId: String, body: AnyCodable, completion: @escaping (_ data: ReturnOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let returnOrderId = "returnOrderId_example" // String | 
let body =  // AnyCodable | 

ReturnOrderAPI.updateReturnOrder(returnOrderId: returnOrderId, body: body) { (response, error) in
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
 **returnOrderId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateReturnOrderStatus**
```swift
    open class func updateReturnOrderStatus(returnOrderId: String, returnOrderStatusUpdate: ReturnOrderStatusUpdate, completion: @escaping (_ data: ReturnOrder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let returnOrderId = "returnOrderId_example" // String | 
let returnOrderStatusUpdate = ReturnOrderStatusUpdate(status: "status_example") // ReturnOrderStatusUpdate | 

ReturnOrderAPI.updateReturnOrderStatus(returnOrderId: returnOrderId, returnOrderStatusUpdate: returnOrderStatusUpdate) { (response, error) in
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
 **returnOrderId** | **String** |  | 
 **returnOrderStatusUpdate** | [**ReturnOrderStatusUpdate**](ReturnOrderStatusUpdate.md) |  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

