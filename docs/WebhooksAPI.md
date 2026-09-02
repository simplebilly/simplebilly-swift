# WebhooksAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSubscription**](WebhooksAPI.md#createsubscription) | **POST** /api/v1/webhook-subscriptions | Create a webhook subscription (outbound hook).
[**deleteSubscription**](WebhooksAPI.md#deletesubscription) | **DELETE** /api/v1/webhook-subscriptions/{subscription_id} | Delete a webhook subscription.
[**emitApi**](WebhooksAPI.md#emitapi) | **POST** /api/v1/webhooks/emit | Manually fire an event against matching hooks (for testing/flows).
[**listEvent**](WebhooksAPI.md#listevent) | **GET** /api/v1/webhook-events | List webhook events (inbound + outbound log).
[**listSubscriptions**](WebhooksAPI.md#listsubscriptions) | **GET** /api/v1/webhook-subscriptions | List webhook subscriptions for the tenant.
[**updateSubscription**](WebhooksAPI.md#updatesubscription) | **PUT** /api/v1/webhook-subscriptions/{subscription_id} | Update a webhook subscription.


# **createSubscription**
```swift
    open class func createSubscription(createSubscriptionRequest: CreateSubscriptionRequest, completion: @escaping (_ data: WebhookSubscription?, _ error: Error?) -> Void)
```

Create a webhook subscription (outbound hook).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let createSubscriptionRequest = CreateSubscriptionRequest(eventType: "eventType_example", isActive: false, name: "name_example", secret: "secret_example", url: "url_example") // CreateSubscriptionRequest | 

// Create a webhook subscription (outbound hook).
WebhooksAPI.createSubscription(createSubscriptionRequest: createSubscriptionRequest) { (response, error) in
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
 **createSubscriptionRequest** | [**CreateSubscriptionRequest**](CreateSubscriptionRequest.md) |  | 

### Return type

[**WebhookSubscription**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteSubscription**
```swift
    open class func deleteSubscription(subscriptionId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a webhook subscription.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let subscriptionId = "subscriptionId_example" // String | 

// Delete a webhook subscription.
WebhooksAPI.deleteSubscription(subscriptionId: subscriptionId) { (response, error) in
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
 **subscriptionId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emitApi**
```swift
    open class func emitApi(emitEventRequest: EmitEventRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Manually fire an event against matching hooks (for testing/flows).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let emitEventRequest = EmitEventRequest(eventType: "eventType_example", payload: 123) // EmitEventRequest | 

// Manually fire an event against matching hooks (for testing/flows).
WebhooksAPI.emitApi(emitEventRequest: emitEventRequest) { (response, error) in
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
 **emitEventRequest** | [**EmitEventRequest**](EmitEventRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listEvent**
```swift
    open class func listEvent(completion: @escaping (_ data: [WebhookEvent]?, _ error: Error?) -> Void)
```

List webhook events (inbound + outbound log).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List webhook events (inbound + outbound log).
WebhooksAPI.listEvent() { (response, error) in
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

[**[WebhookEvent]**](WebhookEvent.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listSubscriptions**
```swift
    open class func listSubscriptions(completion: @escaping (_ data: [WebhookSubscription]?, _ error: Error?) -> Void)
```

List webhook subscriptions for the tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List webhook subscriptions for the tenant.
WebhooksAPI.listSubscriptions() { (response, error) in
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

[**[WebhookSubscription]**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateSubscription**
```swift
    open class func updateSubscription(subscriptionId: String, updateSubscriptionRequest: UpdateSubscriptionRequest, completion: @escaping (_ data: WebhookSubscription?, _ error: Error?) -> Void)
```

Update a webhook subscription.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let subscriptionId = "subscriptionId_example" // String | 
let updateSubscriptionRequest = UpdateSubscriptionRequest(eventType: "eventType_example", isActive: false, name: "name_example", secret: "secret_example", url: "url_example") // UpdateSubscriptionRequest | 

// Update a webhook subscription.
WebhooksAPI.updateSubscription(subscriptionId: subscriptionId, updateSubscriptionRequest: updateSubscriptionRequest) { (response, error) in
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
 **subscriptionId** | **String** |  | 
 **updateSubscriptionRequest** | [**UpdateSubscriptionRequest**](UpdateSubscriptionRequest.md) |  | 

### Return type

[**WebhookSubscription**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

