# DeliveryAppointmentAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDeliveryAppointment**](DeliveryAppointmentAPI.md#createdeliveryappointment) | **POST** /api/v1/delivery-appointments | 
[**deleteDeliveryAppointment**](DeliveryAppointmentAPI.md#deletedeliveryappointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} | 
[**getDeliveryAppointment**](DeliveryAppointmentAPI.md#getdeliveryappointment) | **GET** /api/v1/delivery-appointments/{appointment_id} | 
[**getPublicDeliveryAppointmentStatus**](DeliveryAppointmentAPI.md#getpublicdeliveryappointmentstatus) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
[**listDeliveryAppointments**](DeliveryAppointmentAPI.md#listdeliveryappointments) | **GET** /api/v1/delivery-appointments | 
[**requestPublicDeliveryAppointment**](DeliveryAppointmentAPI.md#requestpublicdeliveryappointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request.
[**updateDeliveryAppointment**](DeliveryAppointmentAPI.md#updatedeliveryappointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} | 
[**updateDeliveryAppointmentStatus**](DeliveryAppointmentAPI.md#updatedeliveryappointmentstatus) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status | 


# **createDeliveryAppointment**
```swift
    open class func createDeliveryAppointment(deliveryAppointmentCreate: DeliveryAppointmentCreate, completion: @escaping (_ data: DeliveryAppointment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let deliveryAppointmentCreate = DeliveryAppointmentCreate(email: "email_example", notes: "notes_example", phone: "phone_example", requestedDate: Date(), status: DeliveryAppointmentStatus(), supplierName: "supplierName_example", timeSlot: "timeSlot_example", warehouseId: "warehouseId_example") // DeliveryAppointmentCreate | 

DeliveryAppointmentAPI.createDeliveryAppointment(deliveryAppointmentCreate: deliveryAppointmentCreate) { (response, error) in
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
 **deliveryAppointmentCreate** | [**DeliveryAppointmentCreate**](DeliveryAppointmentCreate.md) |  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteDeliveryAppointment**
```swift
    open class func deleteDeliveryAppointment(appointmentId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let appointmentId = "appointmentId_example" // String | 

DeliveryAppointmentAPI.deleteDeliveryAppointment(appointmentId: appointmentId) { (response, error) in
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
 **appointmentId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDeliveryAppointment**
```swift
    open class func getDeliveryAppointment(appointmentId: String, completion: @escaping (_ data: DeliveryAppointment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let appointmentId = "appointmentId_example" // String | 

DeliveryAppointmentAPI.getDeliveryAppointment(appointmentId: appointmentId) { (response, error) in
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
 **appointmentId** | **String** |  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPublicDeliveryAppointmentStatus**
```swift
    open class func getPublicDeliveryAppointmentStatus(appointmentId: String, email: String, token: String, completion: @escaping (_ data: PublicDeliveryAppointmentStatusResponse?, _ error: Error?) -> Void)
```

Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let appointmentId = "appointmentId_example" // String | 
let email = "email_example" // String | 
let token = "token_example" // String | 

// Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
DeliveryAppointmentAPI.getPublicDeliveryAppointmentStatus(appointmentId: appointmentId, email: email, token: token) { (response, error) in
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
 **appointmentId** | **String** |  | 
 **email** | **String** |  | 
 **token** | **String** |  | 

### Return type

[**PublicDeliveryAppointmentStatusResponse**](PublicDeliveryAppointmentStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listDeliveryAppointments**
```swift
    open class func listDeliveryAppointments(page: Int? = nil, pageSize: Int? = nil, status: String? = nil, warehouseId: String? = nil, from: Date? = nil, to: Date? = nil, completion: @escaping (_ data: [DeliveryAppointment]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let status = "status_example" // String |  (optional)
let warehouseId = "warehouseId_example" // String |  (optional)
let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)

DeliveryAppointmentAPI.listDeliveryAppointments(page: page, pageSize: pageSize, status: status, warehouseId: warehouseId, from: from, to: to) { (response, error) in
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
 **warehouseId** | **String** |  | [optional] 
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 

### Return type

[**[DeliveryAppointment]**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **requestPublicDeliveryAppointment**
```swift
    open class func requestPublicDeliveryAppointment(publicDeliveryAppointmentRequest: PublicDeliveryAppointmentRequest, completion: @escaping (_ data: PublicDeliveryAppointmentResponse?, _ error: Error?) -> Void)
```

Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let publicDeliveryAppointmentRequest = PublicDeliveryAppointmentRequest(email: "email_example", notes: "notes_example", requestedDate: Date(), supplierName: "supplierName_example", timeSlot: "timeSlot_example", warehouseCode: "warehouseCode_example") // PublicDeliveryAppointmentRequest | 

// Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.
DeliveryAppointmentAPI.requestPublicDeliveryAppointment(publicDeliveryAppointmentRequest: publicDeliveryAppointmentRequest) { (response, error) in
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
 **publicDeliveryAppointmentRequest** | [**PublicDeliveryAppointmentRequest**](PublicDeliveryAppointmentRequest.md) |  | 

### Return type

[**PublicDeliveryAppointmentResponse**](PublicDeliveryAppointmentResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateDeliveryAppointment**
```swift
    open class func updateDeliveryAppointment(appointmentId: String, body: AnyCodable, completion: @escaping (_ data: DeliveryAppointment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let appointmentId = "appointmentId_example" // String | 
let body =  // AnyCodable | 

DeliveryAppointmentAPI.updateDeliveryAppointment(appointmentId: appointmentId, body: body) { (response, error) in
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
 **appointmentId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateDeliveryAppointmentStatus**
```swift
    open class func updateDeliveryAppointmentStatus(appointmentId: String, appointmentStatusUpdate: AppointmentStatusUpdate, completion: @escaping (_ data: DeliveryAppointment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let appointmentId = "appointmentId_example" // String | 
let appointmentStatusUpdate = AppointmentStatusUpdate(status: "status_example") // AppointmentStatusUpdate | 

DeliveryAppointmentAPI.updateDeliveryAppointmentStatus(appointmentId: appointmentId, appointmentStatusUpdate: appointmentStatusUpdate) { (response, error) in
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
 **appointmentId** | **String** |  | 
 **appointmentStatusUpdate** | [**AppointmentStatusUpdate**](AppointmentStatusUpdate.md) |  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

