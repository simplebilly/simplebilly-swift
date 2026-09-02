# SilentPartnerAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSilentPartner**](SilentPartnerAPI.md#createsilentpartner) | **POST** /api/v1/silent-partners | 
[**deleteSilentPartner**](SilentPartnerAPI.md#deletesilentpartner) | **DELETE** /api/v1/silent-partners/{id} | 
[**getSilentPartner**](SilentPartnerAPI.md#getsilentpartner) | **GET** /api/v1/silent-partners/{id} | 
[**getSilentPartners**](SilentPartnerAPI.md#getsilentpartners) | **GET** /api/v1/silent-partners/ | 
[**updateSilentPartner**](SilentPartnerAPI.md#updatesilentpartner) | **PUT** /api/v1/silent-partners/{id} | 


# **createSilentPartner**
```swift
    open class func createSilentPartner(silentPartnerCreate: SilentPartnerCreate, completion: @escaping (_ data: SilentPartner?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let silentPartnerCreate = SilentPartnerCreate(contractDate: Date(), einlage: "einlage_example", gewinnquotePct: "gewinnquotePct_example", gewinnvortrag: "gewinnvortrag_example", instrumentType: InstrumentType(), kestPflichtig: false, name: "name_example", notes: "notes_example", verlustVerrechnungskonto: "verlustVerrechnungskonto_example", verlustbeteiligung: false) // SilentPartnerCreate | 

SilentPartnerAPI.createSilentPartner(silentPartnerCreate: silentPartnerCreate) { (response, error) in
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
 **silentPartnerCreate** | [**SilentPartnerCreate**](SilentPartnerCreate.md) |  | 

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteSilentPartner**
```swift
    open class func deleteSilentPartner(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

SilentPartnerAPI.deleteSilentPartner(id: id) { (response, error) in
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

# **getSilentPartner**
```swift
    open class func getSilentPartner(id: UUID, completion: @escaping (_ data: SilentPartner?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

SilentPartnerAPI.getSilentPartner(id: id) { (response, error) in
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

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSilentPartners**
```swift
    open class func getSilentPartners(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [SilentPartner]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

SilentPartnerAPI.getSilentPartners(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[SilentPartner]**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateSilentPartner**
```swift
    open class func updateSilentPartner(id: UUID, silentPartnerUpdate: SilentPartnerUpdate, completion: @escaping (_ data: SilentPartner?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let silentPartnerUpdate = SilentPartnerUpdate(contractDate: Date(), einlage: "einlage_example", gewinnquotePct: "gewinnquotePct_example", gewinnvortrag: "gewinnvortrag_example", instrumentType: InstrumentType(), kestPflichtig: false, name: "name_example", notes: "notes_example", verlustVerrechnungskonto: "verlustVerrechnungskonto_example", verlustbeteiligung: false) // SilentPartnerUpdate | 

SilentPartnerAPI.updateSilentPartner(id: id, silentPartnerUpdate: silentPartnerUpdate) { (response, error) in
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
 **silentPartnerUpdate** | [**SilentPartnerUpdate**](SilentPartnerUpdate.md) |  | 

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

