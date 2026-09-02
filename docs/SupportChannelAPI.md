# SupportChannelAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createChannelApi**](SupportChannelAPI.md#createchannelapi) | **POST** /api/v1/support/channels | 
[**deleteChannelApi**](SupportChannelAPI.md#deletechannelapi) | **DELETE** /api/v1/support/channels/{channel_id} | 
[**listChannelsApi**](SupportChannelAPI.md#listchannelsapi) | **GET** /api/v1/support/channels | 
[**updateChannelApi**](SupportChannelAPI.md#updatechannelapi) | **PUT** /api/v1/support/channels/{channel_id} | 


# **createChannelApi**
```swift
    open class func createChannelApi(createChannelDto: CreateChannelDto, completion: @escaping (_ data: SupportChannel?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let createChannelDto = CreateChannelDto(channelType: "channelType_example", config: 123, name: "name_example") // CreateChannelDto | 

SupportChannelAPI.createChannelApi(createChannelDto: createChannelDto) { (response, error) in
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
 **createChannelDto** | [**CreateChannelDto**](CreateChannelDto.md) |  | 

### Return type

[**SupportChannel**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteChannelApi**
```swift
    open class func deleteChannelApi(channelId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let channelId = 987 // UUID | 

SupportChannelAPI.deleteChannelApi(channelId: channelId) { (response, error) in
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
 **channelId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listChannelsApi**
```swift
    open class func listChannelsApi(completion: @escaping (_ data: [SupportChannel]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


SupportChannelAPI.listChannelsApi() { (response, error) in
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

[**[SupportChannel]**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateChannelApi**
```swift
    open class func updateChannelApi(channelId: UUID, updateChannelDto: UpdateChannelDto, completion: @escaping (_ data: SupportChannel?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let channelId = 987 // UUID | 
let updateChannelDto = UpdateChannelDto(config: 123, isActive: false, name: "name_example") // UpdateChannelDto | 

SupportChannelAPI.updateChannelApi(channelId: channelId, updateChannelDto: updateChannelDto) { (response, error) in
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
 **channelId** | **UUID** |  | 
 **updateChannelDto** | [**UpdateChannelDto**](UpdateChannelDto.md) |  | 

### Return type

[**SupportChannel**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

