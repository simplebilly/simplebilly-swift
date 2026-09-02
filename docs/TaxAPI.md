# TaxAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTaxRate**](TaxAPI.md#createtaxrate) | **POST** /api/v1/tax-rates | Create a tax rate (&#x60;admin:settings&#x60;).
[**deleteTaxRate**](TaxAPI.md#deletetaxrate) | **DELETE** /api/v1/tax-rates/{id} | Delete a tax rate by id (&#x60;admin:settings&#x60;).
[**listTaxRates**](TaxAPI.md#listtaxrates) | **GET** /api/v1/tax-rates | List the calling tenant&#39;s tax rates.
[**updateTaxRate**](TaxAPI.md#updatetaxrate) | **PUT** /api/v1/tax-rates/{id} | Update a tax rate by id (&#x60;admin:settings&#x60;). Replaces all body fields.


# **createTaxRate**
```swift
    open class func createTaxRate(taxRateCreate: TaxRateCreate, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Create a tax rate (`admin:settings`).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let taxRateCreate = TaxRateCreate(countryCode: "countryCode_example", effectiveFrom: Date(), isDefault: false, name: "name_example", ratePercent: 123) // TaxRateCreate | 

// Create a tax rate (`admin:settings`).
TaxAPI.createTaxRate(taxRateCreate: taxRateCreate) { (response, error) in
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
 **taxRateCreate** | [**TaxRateCreate**](TaxRateCreate.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteTaxRate**
```swift
    open class func deleteTaxRate(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete a tax rate by id (`admin:settings`).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

// Delete a tax rate by id (`admin:settings`).
TaxAPI.deleteTaxRate(id: id) { (response, error) in
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTaxRates**
```swift
    open class func listTaxRates(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

List the calling tenant's tax rates.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List the calling tenant's tax rates.
TaxAPI.listTaxRates() { (response, error) in
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

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateTaxRate**
```swift
    open class func updateTaxRate(id: UUID, taxRateCreate: TaxRateCreate, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Update a tax rate by id (`admin:settings`). Replaces all body fields.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let taxRateCreate = TaxRateCreate(countryCode: "countryCode_example", effectiveFrom: Date(), isDefault: false, name: "name_example", ratePercent: 123) // TaxRateCreate | 

// Update a tax rate by id (`admin:settings`). Replaces all body fields.
TaxAPI.updateTaxRate(id: id, taxRateCreate: taxRateCreate) { (response, error) in
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
 **taxRateCreate** | [**TaxRateCreate**](TaxRateCreate.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

