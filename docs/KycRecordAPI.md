# KycRecordAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createKycRecord**](KycRecordAPI.md#createkycrecord) | **POST** /api/v1/kyc-records | 
[**deleteKycRecord**](KycRecordAPI.md#deletekycrecord) | **DELETE** /api/v1/kyc-records/{id} | 
[**getKycRecord**](KycRecordAPI.md#getkycrecord) | **GET** /api/v1/kyc-records/{id} | 
[**getKycRecords**](KycRecordAPI.md#getkycrecords) | **GET** /api/v1/kyc-records/ | 
[**updateKycRecord**](KycRecordAPI.md#updatekycrecord) | **PUT** /api/v1/kyc-records/{id} | 


# **createKycRecord**
```swift
    open class func createKycRecord(kycRecordCreate: KycRecordCreate, completion: @escaping (_ data: KycRecord?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let kycRecordCreate = KycRecordCreate(customerId: "customerId_example", customerName: "customerName_example", kycDate: Date(), notes: "notes_example", retentionUntil: Date(), riskAssessment: "riskAssessment_example") // KycRecordCreate | 

KycRecordAPI.createKycRecord(kycRecordCreate: kycRecordCreate) { (response, error) in
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
 **kycRecordCreate** | [**KycRecordCreate**](KycRecordCreate.md) |  | 

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteKycRecord**
```swift
    open class func deleteKycRecord(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

KycRecordAPI.deleteKycRecord(id: id) { (response, error) in
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

# **getKycRecord**
```swift
    open class func getKycRecord(id: UUID, completion: @escaping (_ data: KycRecord?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

KycRecordAPI.getKycRecord(id: id) { (response, error) in
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

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getKycRecords**
```swift
    open class func getKycRecords(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [KycRecord]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

KycRecordAPI.getKycRecords(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[KycRecord]**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateKycRecord**
```swift
    open class func updateKycRecord(id: UUID, kycRecordUpdate: KycRecordUpdate, completion: @escaping (_ data: KycRecord?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let kycRecordUpdate = KycRecordUpdate(customerId: "customerId_example", customerName: "customerName_example", kycDate: Date(), notes: "notes_example", retentionUntil: Date(), riskAssessment: "riskAssessment_example") // KycRecordUpdate | 

KycRecordAPI.updateKycRecord(id: id, kycRecordUpdate: kycRecordUpdate) { (response, error) in
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
 **kycRecordUpdate** | [**KycRecordUpdate**](KycRecordUpdate.md) |  | 

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

