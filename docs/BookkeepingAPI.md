# BookkeepingAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**allocatePaymentApi**](BookkeepingAPI.md#allocatepaymentapi) | **POST** /api/v1/payments/allocate | Allocate a payment to an invoice
[**bwaReportApi**](BookkeepingAPI.md#bwareportapi) | **GET** /api/v1/bookkeeping/bwa | Get BWA (Betriebswirtschaftliche Auswertung) report
[**elsterStatusApi**](BookkeepingAPI.md#elsterstatusapi) | **GET** /api/v1/bookkeeping/elster/status | 
[**elsterValidateApi**](BookkeepingAPI.md#elstervalidateapi) | **POST** /api/v1/bookkeeping/ustva/elster-validate | 
[**elsterXmlApi**](BookkeepingAPI.md#elsterxmlapi) | **GET** /api/v1/bookkeeping/ustva/elster-xml | 
[**getCashflow**](BookkeepingAPI.md#getcashflow) | **GET** /api/v1/bookkeeping/cashflow | GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
[**getLiquidity**](BookkeepingAPI.md#getliquidity) | **GET** /api/v1/bookkeeping/liquidity | GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
[**getOpenInvoicesApi**](BookkeepingAPI.md#getopeninvoicesapi) | **GET** /api/v1/payments/open-invoices/{customer_id} | Get open invoices for a customer
[**getVerfahrensdokumentation**](BookkeepingAPI.md#getverfahrensdokumentation) | **GET** /api/v1/bookkeeping/verfahrensdokumentation | GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
[**runDunningApi**](BookkeepingAPI.md#rundunningapi) | **POST** /api/v1/bookkeeping/dunning | 


# **allocatePaymentApi**
```swift
    open class func allocatePaymentApi(allocatePaymentRequest: AllocatePaymentRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Allocate a payment to an invoice

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let allocatePaymentRequest = AllocatePaymentRequest(amount: 123, invoiceId: "invoiceId_example", paymentId: 123) // AllocatePaymentRequest | 

// Allocate a payment to an invoice
BookkeepingAPI.allocatePaymentApi(allocatePaymentRequest: allocatePaymentRequest) { (response, error) in
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
 **allocatePaymentRequest** | [**AllocatePaymentRequest**](AllocatePaymentRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bwaReportApi**
```swift
    open class func bwaReportApi(year: Int? = nil, month: Int? = nil, completion: @escaping (_ data: BWAReport?, _ error: Error?) -> Void)
```

Get BWA (Betriebswirtschaftliche Auswertung) report

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let month = 987 // Int |  (optional)

// Get BWA (Betriebswirtschaftliche Auswertung) report
BookkeepingAPI.bwaReportApi(year: year, month: month) { (response, error) in
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
 **year** | **Int** |  | [optional] 
 **month** | **Int** |  | [optional] 

### Return type

[**BWAReport**](BWAReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **elsterStatusApi**
```swift
    open class func elsterStatusApi(completion: @escaping (_ data: ElsterStatus?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


BookkeepingAPI.elsterStatusApi() { (response, error) in
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

[**ElsterStatus**](ElsterStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **elsterValidateApi**
```swift
    open class func elsterValidateApi(zeitraum: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let zeitraum = "zeitraum_example" // String | 

BookkeepingAPI.elsterValidateApi(zeitraum: zeitraum) { (response, error) in
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
 **zeitraum** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **elsterXmlApi**
```swift
    open class func elsterXmlApi(zeitraum: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let zeitraum = "zeitraum_example" // String | 

BookkeepingAPI.elsterXmlApi(zeitraum: zeitraum) { (response, error) in
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
 **zeitraum** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCashflow**
```swift
    open class func getCashflow(year: Int? = nil, month: Int? = nil, completion: @escaping (_ data: CashflowReport?, _ error: Error?) -> Void)
```

GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int |  (optional)
let month = 987 // Int |  (optional)

// GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
BookkeepingAPI.getCashflow(year: year, month: month) { (response, error) in
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
 **year** | **Int** |  | [optional] 
 **month** | **Int** |  | [optional] 

### Return type

[**CashflowReport**](CashflowReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getLiquidity**
```swift
    open class func getLiquidity(completion: @escaping (_ data: LiquidityPosition?, _ error: Error?) -> Void)
```

GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
BookkeepingAPI.getLiquidity() { (response, error) in
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

[**LiquidityPosition**](LiquidityPosition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getOpenInvoicesApi**
```swift
    open class func getOpenInvoicesApi(customerId: String, completion: @escaping (_ data: [Invoice]?, _ error: Error?) -> Void)
```

Get open invoices for a customer

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let customerId = "customerId_example" // String | 

// Get open invoices for a customer
BookkeepingAPI.getOpenInvoicesApi(customerId: customerId) { (response, error) in
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
 **customerId** | **String** |  | 

### Return type

[**[Invoice]**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getVerfahrensdokumentation**
```swift
    open class func getVerfahrensdokumentation(completion: @escaping (_ data: Verfahrensdokumentation?, _ error: Error?) -> Void)
```

GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
BookkeepingAPI.getVerfahrensdokumentation() { (response, error) in
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

[**Verfahrensdokumentation**](Verfahrensdokumentation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **runDunningApi**
```swift
    open class func runDunningApi(completion: @escaping (_ data: DunningResult?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


BookkeepingAPI.runDunningApi() { (response, error) in
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

[**DunningResult**](DunningResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

