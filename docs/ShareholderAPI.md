# ShareholderAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createShareholder**](ShareholderAPI.md#createshareholder) | **POST** /api/v1/shareholders | 
[**deleteShareholder**](ShareholderAPI.md#deleteshareholder) | **DELETE** /api/v1/shareholders/{id} | 
[**getShareholder**](ShareholderAPI.md#getshareholder) | **GET** /api/v1/shareholders/{id} | 
[**getShareholders**](ShareholderAPI.md#getshareholders) | **GET** /api/v1/shareholders/ | 
[**updateShareholder**](ShareholderAPI.md#updateshareholder) | **PUT** /api/v1/shareholders/{id} | 


# **createShareholder**
```swift
    open class func createShareholder(shareholderCreate: ShareholderCreate, completion: @escaping (_ data: Shareholder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let shareholderCreate = ShareholderCreate(address: "address_example", birthDate: Date(), email: "email_example", firstName: "firstName_example", lastName: "lastName_example", shareNumber: "shareNumber_example", shares: "shares_example") // ShareholderCreate | 

ShareholderAPI.createShareholder(shareholderCreate: shareholderCreate) { (response, error) in
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
 **shareholderCreate** | [**ShareholderCreate**](ShareholderCreate.md) |  | 

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteShareholder**
```swift
    open class func deleteShareholder(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ShareholderAPI.deleteShareholder(id: id) { (response, error) in
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
 **id** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getShareholder**
```swift
    open class func getShareholder(id: UUID, completion: @escaping (_ data: Shareholder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ShareholderAPI.getShareholder(id: id) { (response, error) in
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
 **id** | **UUID** |  | 

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getShareholders**
```swift
    open class func getShareholders(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Shareholder]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

ShareholderAPI.getShareholders(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[Shareholder]**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateShareholder**
```swift
    open class func updateShareholder(id: UUID, shareholderUpdate: ShareholderUpdate, completion: @escaping (_ data: Shareholder?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let shareholderUpdate = ShareholderUpdate(address: "address_example", birthDate: Date(), email: "email_example", firstName: "firstName_example", lastName: "lastName_example", shareNumber: "shareNumber_example", shares: "shares_example") // ShareholderUpdate | 

ShareholderAPI.updateShareholder(id: id, shareholderUpdate: shareholderUpdate) { (response, error) in
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
 **id** | **UUID** |  | 
 **shareholderUpdate** | [**ShareholderUpdate**](ShareholderUpdate.md) |  | 

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

