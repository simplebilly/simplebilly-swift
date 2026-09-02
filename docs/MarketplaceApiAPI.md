# MarketplaceApiAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createConnectionApi**](MarketplaceApiAPI.md#createconnectionapi) | **POST** /api/v1/marketplace/connections | Create a new connection (for API-key based platforms)
[**deleteConnectionApi**](MarketplaceApiAPI.md#deleteconnectionapi) | **DELETE** /api/v1/marketplace/connections/{connection_id} | Soft-delete a connection
[**getConnectionApi**](MarketplaceApiAPI.md#getconnectionapi) | **GET** /api/v1/marketplace/connections/{connection_id} | Get a single connection
[**getSyncDirectionApi**](MarketplaceApiAPI.md#getsyncdirectionapi) | **GET** /api/v1/marketplace/connections/{connection_id}/directions | Get current sync direction configuration for a connection
[**getSyncLogsApi**](MarketplaceApiAPI.md#getsynclogsapi) | **GET** /api/v1/marketplace/connections/{connection_id}/logs | Get sync logs for a connection
[**listConnectionsApi**](MarketplaceApiAPI.md#listconnectionsapi) | **GET** /api/v1/marketplace/connections | List connections for the current tenant
[**listPlatformsApi**](MarketplaceApiAPI.md#listplatformsapi) | **GET** /api/v1/marketplace/platforms | List all supported platforms
[**oauthAuthorizeApi**](MarketplaceApiAPI.md#oauthauthorizeapi) | **POST** /api/v1/marketplace/oauth/authorize | OAuth: initiate authorization flow
[**oauthCallbackApi**](MarketplaceApiAPI.md#oauthcallbackapi) | **POST** /api/v1/marketplace/oauth/callback | OAuth: handle callback after authorization
[**triggerSyncApi**](MarketplaceApiAPI.md#triggersyncapi) | **POST** /api/v1/marketplace/connections/{connection_id}/sync | Trigger sync for a connection
[**updateConnectionApi**](MarketplaceApiAPI.md#updateconnectionapi) | **PUT** /api/v1/marketplace/connections/{connection_id} | Update a connection
[**updateSyncDirectionApi**](MarketplaceApiAPI.md#updatesyncdirectionapi) | **PUT** /api/v1/marketplace/connections/{connection_id}/directions | Update per-entity sync direction configuration for a connection
[**webhookReceiverApi**](MarketplaceApiAPI.md#webhookreceiverapi) | **POST** /api/v1/marketplace/webhook/{platform}/{connection_id} | Webhook receiver


# **createConnectionApi**
```swift
    open class func createConnectionApi(createConnectionRequest: CreateConnectionRequest, completion: @escaping (_ data: MarketplaceConnection?, _ error: Error?) -> Void)
```

Create a new connection (for API-key based platforms)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let createConnectionRequest = CreateConnectionRequest(apiKey: "apiKey_example", apiSecret: "apiSecret_example", config: 123, label: "label_example", platform: "platform_example", shopDomain: "shopDomain_example") // CreateConnectionRequest | 

// Create a new connection (for API-key based platforms)
MarketplaceApiAPI.createConnectionApi(createConnectionRequest: createConnectionRequest) { (response, error) in
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
 **createConnectionRequest** | [**CreateConnectionRequest**](CreateConnectionRequest.md) |  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteConnectionApi**
```swift
    open class func deleteConnectionApi(connectionId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Soft-delete a connection

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let connectionId = "connectionId_example" // String | 

// Soft-delete a connection
MarketplaceApiAPI.deleteConnectionApi(connectionId: connectionId) { (response, error) in
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
 **connectionId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getConnectionApi**
```swift
    open class func getConnectionApi(connectionId: String, completion: @escaping (_ data: MarketplaceConnection?, _ error: Error?) -> Void)
```

Get a single connection

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let connectionId = "connectionId_example" // String | 

// Get a single connection
MarketplaceApiAPI.getConnectionApi(connectionId: connectionId) { (response, error) in
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
 **connectionId** | **String** |  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSyncDirectionApi**
```swift
    open class func getSyncDirectionApi(connectionId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Get current sync direction configuration for a connection

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let connectionId = "connectionId_example" // String | 

// Get current sync direction configuration for a connection
MarketplaceApiAPI.getSyncDirectionApi(connectionId: connectionId) { (response, error) in
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
 **connectionId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSyncLogsApi**
```swift
    open class func getSyncLogsApi(connectionId: String, completion: @escaping (_ data: [SyncLog]?, _ error: Error?) -> Void)
```

Get sync logs for a connection

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let connectionId = "connectionId_example" // String | 

// Get sync logs for a connection
MarketplaceApiAPI.getSyncLogsApi(connectionId: connectionId) { (response, error) in
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
 **connectionId** | **String** |  | 

### Return type

[**[SyncLog]**](SyncLog.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listConnectionsApi**
```swift
    open class func listConnectionsApi(completion: @escaping (_ data: [MarketplaceConnection]?, _ error: Error?) -> Void)
```

List connections for the current tenant

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List connections for the current tenant
MarketplaceApiAPI.listConnectionsApi() { (response, error) in
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

[**[MarketplaceConnection]**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPlatformsApi**
```swift
    open class func listPlatformsApi(completion: @escaping (_ data: [PlatformInfo]?, _ error: Error?) -> Void)
```

List all supported platforms

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List all supported platforms
MarketplaceApiAPI.listPlatformsApi() { (response, error) in
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

[**[PlatformInfo]**](PlatformInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauthAuthorizeApi**
```swift
    open class func oauthAuthorizeApi(oAuthAuthorizeRequest: OAuthAuthorizeRequest, completion: @escaping (_ data: OAuthAuthorizeResponse?, _ error: Error?) -> Void)
```

OAuth: initiate authorization flow

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let oAuthAuthorizeRequest = OAuthAuthorizeRequest(config: 123, platform: "platform_example", redirectUri: "redirectUri_example") // OAuthAuthorizeRequest | 

// OAuth: initiate authorization flow
MarketplaceApiAPI.oauthAuthorizeApi(oAuthAuthorizeRequest: oAuthAuthorizeRequest) { (response, error) in
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
 **oAuthAuthorizeRequest** | [**OAuthAuthorizeRequest**](OAuthAuthorizeRequest.md) |  | 

### Return type

[**OAuthAuthorizeResponse**](OAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauthCallbackApi**
```swift
    open class func oauthCallbackApi(oAuthCallbackRequest: OAuthCallbackRequest, completion: @escaping (_ data: MarketplaceConnection?, _ error: Error?) -> Void)
```

OAuth: handle callback after authorization

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let oAuthCallbackRequest = OAuthCallbackRequest(code: "code_example", config: 123, connectionId: "connectionId_example", platform: "platform_example", shopDomain: "shopDomain_example", state: "state_example") // OAuthCallbackRequest | 

// OAuth: handle callback after authorization
MarketplaceApiAPI.oauthCallbackApi(oAuthCallbackRequest: oAuthCallbackRequest) { (response, error) in
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
 **oAuthCallbackRequest** | [**OAuthCallbackRequest**](OAuthCallbackRequest.md) |  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **triggerSyncApi**
```swift
    open class func triggerSyncApi(connectionId: String, syncType: String? = nil, direction: String? = nil, completion: @escaping (_ data: SyncSummary?, _ error: Error?) -> Void)
```

Trigger sync for a connection

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let connectionId = "connectionId_example" // String | 
let syncType = "syncType_example" // String |  (optional)
let direction = "direction_example" // String |  (optional)

// Trigger sync for a connection
MarketplaceApiAPI.triggerSyncApi(connectionId: connectionId, syncType: syncType, direction: direction) { (response, error) in
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
 **connectionId** | **String** |  | 
 **syncType** | **String** |  | [optional] 
 **direction** | **String** |  | [optional] 

### Return type

[**SyncSummary**](SyncSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateConnectionApi**
```swift
    open class func updateConnectionApi(connectionId: String, updateConnectionRequest: UpdateConnectionRequest, completion: @escaping (_ data: MarketplaceConnection?, _ error: Error?) -> Void)
```

Update a connection

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let connectionId = "connectionId_example" // String | 
let updateConnectionRequest = UpdateConnectionRequest(apiKey: "apiKey_example", apiSecret: "apiSecret_example", config: 123, isActive: false, label: "label_example", shopDomain: "shopDomain_example") // UpdateConnectionRequest | 

// Update a connection
MarketplaceApiAPI.updateConnectionApi(connectionId: connectionId, updateConnectionRequest: updateConnectionRequest) { (response, error) in
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
 **connectionId** | **String** |  | 
 **updateConnectionRequest** | [**UpdateConnectionRequest**](UpdateConnectionRequest.md) |  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateSyncDirectionApi**
```swift
    open class func updateSyncDirectionApi(connectionId: String, updateSyncDirectionRequest: UpdateSyncDirectionRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Update per-entity sync direction configuration for a connection

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let connectionId = "connectionId_example" // String | 
let updateSyncDirectionRequest = UpdateSyncDirectionRequest(directions: "TODO") // UpdateSyncDirectionRequest | 

// Update per-entity sync direction configuration for a connection
MarketplaceApiAPI.updateSyncDirectionApi(connectionId: connectionId, updateSyncDirectionRequest: updateSyncDirectionRequest) { (response, error) in
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
 **connectionId** | **String** |  | 
 **updateSyncDirectionRequest** | [**UpdateSyncDirectionRequest**](UpdateSyncDirectionRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhookReceiverApi**
```swift
    open class func webhookReceiverApi(platform: String, connectionId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Webhook receiver

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let platform = "platform_example" // String | 
let connectionId = "connectionId_example" // String | 

// Webhook receiver
MarketplaceApiAPI.webhookReceiverApi(platform: platform, connectionId: connectionId) { (response, error) in
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
 **platform** | **String** |  | 
 **connectionId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

