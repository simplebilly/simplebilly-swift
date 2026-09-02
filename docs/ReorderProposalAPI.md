# ReorderProposalAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**applyReorderProposal**](ReorderProposalAPI.md#applyreorderproposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order.
[**getReorderProposal**](ReorderProposalAPI.md#getreorderproposal) | **GET** /api/v1/reorder-proposals | 


# **applyReorderProposal**
```swift
    open class func applyReorderProposal(configuredOnly: Bool? = nil, warehouseId: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let configuredOnly = true // Bool | Only include products with a reorder point configured (`min_stock`). (optional)
let warehouseId = "warehouseId_example" // String | Limit to a single warehouse id. (optional)

// Convert a reorder proposal into a draft purchase order.
ReorderProposalAPI.applyReorderProposal(configuredOnly: configuredOnly, warehouseId: warehouseId) { (response, error) in
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
 **configuredOnly** | **Bool** | Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] 
 **warehouseId** | **String** | Limit to a single warehouse id. | [optional] 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getReorderProposal**
```swift
    open class func getReorderProposal(configuredOnly: Bool? = nil, warehouseId: String? = nil, completion: @escaping (_ data: ReorderProposalResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let configuredOnly = true // Bool | Only include products with a reorder point configured (`min_stock`). (optional)
let warehouseId = "warehouseId_example" // String | Limit to a single warehouse id. (optional)

ReorderProposalAPI.getReorderProposal(configuredOnly: configuredOnly, warehouseId: warehouseId) { (response, error) in
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
 **configuredOnly** | **Bool** | Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] 
 **warehouseId** | **String** | Limit to a single warehouse id. | [optional] 

### Return type

[**ReorderProposalResponse**](ReorderProposalResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

