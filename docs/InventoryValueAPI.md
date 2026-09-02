# InventoryValueAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getInventoryValueApi**](InventoryValueAPI.md#getinventoryvalueapi) | **GET** /api/v1/bookkeeping/inventory-value | 
[**recordInventoryValueApi**](InventoryValueAPI.md#recordinventoryvalueapi) | **POST** /api/v1/bookkeeping/inventory-value/record | 


# **getInventoryValueApi**
```swift
    open class func getInventoryValueApi(completion: @escaping (_ data: CurrentInventoryValue?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


InventoryValueAPI.getInventoryValueApi() { (response, error) in
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

[**CurrentInventoryValue**](CurrentInventoryValue.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **recordInventoryValueApi**
```swift
    open class func recordInventoryValueApi(completion: @escaping (_ data: InventoryValuePoint?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


InventoryValueAPI.recordInventoryValueApi() { (response, error) in
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

[**InventoryValuePoint**](InventoryValuePoint.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

