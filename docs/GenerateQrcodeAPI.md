# GenerateQrcodeAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generateQrcodeApi**](GenerateQrcodeAPI.md#generateqrcodeapi) | **GET** /api/v1/invoices/{id}/qrcode | 


# **generateQrcodeApi**
```swift
    open class func generateQrcodeApi(iban: String, id: String, holderName: String? = nil, bic: String? = nil, amount: String? = nil, reference: String? = nil, purpose: String? = nil, completion: @escaping (_ data: QRCodeResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let iban = "iban_example" // String | 
let id = "id_example" // String | 
let holderName = "holderName_example" // String |  (optional)
let bic = "bic_example" // String |  (optional)
let amount = "amount_example" // String |  (optional)
let reference = "reference_example" // String |  (optional)
let purpose = "purpose_example" // String |  (optional)

GenerateQrcodeAPI.generateQrcodeApi(iban: iban, id: id, holderName: holderName, bic: bic, amount: amount, reference: reference, purpose: purpose) { (response, error) in
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
 **iban** | **String** |  | 
 **id** | **String** |  | 
 **holderName** | **String** |  | [optional] 
 **bic** | **String** |  | [optional] 
 **amount** | **String** |  | [optional] 
 **reference** | **String** |  | [optional] 
 **purpose** | **String** |  | [optional] 

### Return type

[**QRCodeResponse**](QRCodeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

