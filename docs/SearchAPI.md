# SearchAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**globalSearch**](SearchAPI.md#globalsearch) | **GET** /api/v1/search | GET /api/v1/search?q&#x3D;...
[**myPermissions**](SearchAPI.md#mypermissions) | **GET** /api/v1/me/permissions | GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.


# **globalSearch**
```swift
    open class func globalSearch(q: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

GET /api/v1/search?q=...

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let q = "q_example" // String | Search text (min 2 chars)

// GET /api/v1/search?q=...
SearchAPI.globalSearch(q: q) { (response, error) in
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
 **q** | **String** | Search text (min 2 chars) | 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **myPermissions**
```swift
    open class func myPermissions(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.
SearchAPI.myPermissions() { (response, error) in
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

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

