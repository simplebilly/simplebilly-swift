# CreateSepaDirectDebitAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSepaDirectDebitApi**](CreateSepaDirectDebitAPI.md#createsepadirectdebitapi) | **POST** /api/v1/bookkeeping/sepa-direct-debit | 


# **createSepaDirectDebitApi**
```swift
    open class func createSepaDirectDebitApi(creditorName: String, creditorIban: String, creditorId: String, mandateId: String, mandateDate: String, debtorName: String, debtorIban: String, amount: String, collectionDate: String, creditorBic: String? = nil, debtorBic: String? = nil, description: String? = nil, completion: @escaping (_ data: SepaDirectDebitResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let creditorName = "creditorName_example" // String | 
let creditorIban = "creditorIban_example" // String | 
let creditorId = "creditorId_example" // String | 
let mandateId = "mandateId_example" // String | 
let mandateDate = "mandateDate_example" // String | 
let debtorName = "debtorName_example" // String | 
let debtorIban = "debtorIban_example" // String | 
let amount = "amount_example" // String | 
let collectionDate = "collectionDate_example" // String | 
let creditorBic = "creditorBic_example" // String |  (optional)
let debtorBic = "debtorBic_example" // String |  (optional)
let description = "description_example" // String |  (optional)

CreateSepaDirectDebitAPI.createSepaDirectDebitApi(creditorName: creditorName, creditorIban: creditorIban, creditorId: creditorId, mandateId: mandateId, mandateDate: mandateDate, debtorName: debtorName, debtorIban: debtorIban, amount: amount, collectionDate: collectionDate, creditorBic: creditorBic, debtorBic: debtorBic, description: description) { (response, error) in
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
 **creditorName** | **String** |  | 
 **creditorIban** | **String** |  | 
 **creditorId** | **String** |  | 
 **mandateId** | **String** |  | 
 **mandateDate** | **String** |  | 
 **debtorName** | **String** |  | 
 **debtorIban** | **String** |  | 
 **amount** | **String** |  | 
 **collectionDate** | **String** |  | 
 **creditorBic** | **String** |  | [optional] 
 **debtorBic** | **String** |  | [optional] 
 **description** | **String** |  | [optional] 

### Return type

[**SepaDirectDebitResponse**](SepaDirectDebitResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

