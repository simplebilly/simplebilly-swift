# ZugferdAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generateZugferdApi**](ZugferdAPI.md#generatezugferdapi) | **GET** /api/v1/invoices/{id}/zugferd | 


# **generateZugferdApi**
```swift
    open class func generateZugferdApi(id: String, supplierName: String? = nil, supplierStreet: String? = nil, supplierCity: String? = nil, supplierZip: String? = nil, supplierCountry: String? = nil, supplierVatId: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = "id_example" // String | 
let supplierName = "supplierName_example" // String |  (optional)
let supplierStreet = "supplierStreet_example" // String |  (optional)
let supplierCity = "supplierCity_example" // String |  (optional)
let supplierZip = "supplierZip_example" // String |  (optional)
let supplierCountry = "supplierCountry_example" // String |  (optional)
let supplierVatId = "supplierVatId_example" // String |  (optional)

ZugferdAPI.generateZugferdApi(id: id, supplierName: supplierName, supplierStreet: supplierStreet, supplierCity: supplierCity, supplierZip: supplierZip, supplierCountry: supplierCountry, supplierVatId: supplierVatId) { (response, error) in
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
 **id** | **String** |  | 
 **supplierName** | **String** |  | [optional] 
 **supplierStreet** | **String** |  | [optional] 
 **supplierCity** | **String** |  | [optional] 
 **supplierZip** | **String** |  | [optional] 
 **supplierCountry** | **String** |  | [optional] 
 **supplierVatId** | **String** |  | [optional] 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

