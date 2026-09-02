# ShipmentAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createShipment**](ShipmentAPI.md#createshipment) | **POST** /api/v1/shipments | 
[**createShipmentFromOrder**](ShipmentAPI.md#createshipmentfromorder) | **POST** /api/v1/orders/{order_number}/shipments | Create a real shipment for an order: calls the configured carrier&#39;s label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
[**deleteShipment**](ShipmentAPI.md#deleteshipment) | **DELETE** /api/v1/shipments/{shipment_id} | 
[**getShipment**](ShipmentAPI.md#getshipment) | **GET** /api/v1/shipments/{shipment_id} | 
[**listShipments**](ShipmentAPI.md#listshipments) | **GET** /api/v1/shipments | 
[**trackOrderPublic**](ShipmentAPI.md#trackorderpublic) | **POST** /api/v1/public/track | Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
[**trackShipmentApi**](ShipmentAPI.md#trackshipmentapi) | **GET** /api/v1/shipments/{shipment_id}/tracking | 
[**updateShipmentStatus**](ShipmentAPI.md#updateshipmentstatus) | **PUT** /api/v1/shipments/{shipment_id}/status | 


# **createShipment**
```swift
    open class func createShipment(shipment: Shipment, completion: @escaping (_ data: Shipment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shipment = Shipment(deliveredAt: Date(), labelUrl: "labelUrl_example", lineItemsShipment: 123, orderId: "orderId_example", recipientAddress: 123, shipmentDate: Date(), shippingCarrier: "shippingCarrier_example", shippingCost: "shippingCost_example", shippingMethod: "shippingMethod_example", signedBy: "signedBy_example", status: "status_example", trackingEvents: 123, trackingNumber: "trackingNumber_example", trackingUrl: "trackingUrl_example", weightKg: 123) // Shipment | 

ShipmentAPI.createShipment(shipment: shipment) { (response, error) in
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
 **shipment** | [**Shipment**](Shipment.md) |  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createShipmentFromOrder**
```swift
    open class func createShipmentFromOrder(orderNumber: String, createShipmentRequest: CreateShipmentRequest, completion: @escaping (_ data: Shipment?, _ error: Error?) -> Void)
```

Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let orderNumber = "orderNumber_example" // String | 
let createShipmentRequest = CreateShipmentRequest(carrier: "carrier_example", service: "service_example", weightKg: 123) // CreateShipmentRequest | 

// Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
ShipmentAPI.createShipmentFromOrder(orderNumber: orderNumber, createShipmentRequest: createShipmentRequest) { (response, error) in
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
 **createShipmentRequest** | [**CreateShipmentRequest**](CreateShipmentRequest.md) |  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteShipment**
```swift
    open class func deleteShipment(shipmentId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shipmentId = "shipmentId_example" // String | 

ShipmentAPI.deleteShipment(shipmentId: shipmentId) { (response, error) in
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
 **shipmentId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getShipment**
```swift
    open class func getShipment(shipmentId: String, completion: @escaping (_ data: Shipment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shipmentId = "shipmentId_example" // String | 

ShipmentAPI.getShipment(shipmentId: shipmentId) { (response, error) in
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
 **shipmentId** | **String** |  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listShipments**
```swift
    open class func listShipments(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Shipment]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

ShipmentAPI.listShipments(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[Shipment]**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackOrderPublic**
```swift
    open class func trackOrderPublic(trackOrderRequest: TrackOrderRequest, completion: @escaping (_ data: TrackOrderResponse?, _ error: Error?) -> Void)
```

Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let trackOrderRequest = TrackOrderRequest(email: "email_example", orderNumber: "orderNumber_example") // TrackOrderRequest | 

// Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
ShipmentAPI.trackOrderPublic(trackOrderRequest: trackOrderRequest) { (response, error) in
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
 **trackOrderRequest** | [**TrackOrderRequest**](TrackOrderRequest.md) |  | 

### Return type

[**TrackOrderResponse**](TrackOrderResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trackShipmentApi**
```swift
    open class func trackShipmentApi(shipmentId: String, completion: @escaping (_ data: TrackingInfo?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shipmentId = "shipmentId_example" // String | 

ShipmentAPI.trackShipmentApi(shipmentId: shipmentId) { (response, error) in
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
 **shipmentId** | **String** |  | 

### Return type

[**TrackingInfo**](TrackingInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateShipmentStatus**
```swift
    open class func updateShipmentStatus(shipmentId: String, shipmentStatusUpdate: ShipmentStatusUpdate, completion: @escaping (_ data: Shipment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shipmentId = "shipmentId_example" // String | 
let shipmentStatusUpdate = ShipmentStatusUpdate(deliveredAt: "deliveredAt_example", signedBy: "signedBy_example", status: "status_example", trackingNumber: "trackingNumber_example") // ShipmentStatusUpdate | 

ShipmentAPI.updateShipmentStatus(shipmentId: shipmentId, shipmentStatusUpdate: shipmentStatusUpdate) { (response, error) in
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
 **shipmentId** | **String** |  | 
 **shipmentStatusUpdate** | [**ShipmentStatusUpdate**](ShipmentStatusUpdate.md) |  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

