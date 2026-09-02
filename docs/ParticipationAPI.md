# ParticipationAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createParticipation**](ParticipationAPI.md#createparticipation) | **POST** /api/v1/participations | 
[**deleteParticipation**](ParticipationAPI.md#deleteparticipation) | **DELETE** /api/v1/participations/{id} | 
[**getParticipation**](ParticipationAPI.md#getparticipation) | **GET** /api/v1/participations/{id} | 
[**getParticipations**](ParticipationAPI.md#getparticipations) | **GET** /api/v1/participations/ | 
[**updateParticipation**](ParticipationAPI.md#updateparticipation) | **PUT** /api/v1/participations/{id} | 


# **createParticipation**
```swift
    open class func createParticipation(participationCreate: ParticipationCreate, completion: @escaping (_ data: Participation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let participationCreate = ParticipationCreate(acquiredAt: Date(), boardAppointment: false, companyName: "companyName_example", controlAgreement: false, legalForm: "legalForm_example", ownershipPct: "ownershipPct_example", purposeVehicle: false, votingMajority: false) // ParticipationCreate | 

ParticipationAPI.createParticipation(participationCreate: participationCreate) { (response, error) in
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
 **participationCreate** | [**ParticipationCreate**](ParticipationCreate.md) |  | 

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteParticipation**
```swift
    open class func deleteParticipation(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ParticipationAPI.deleteParticipation(id: id) { (response, error) in
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

# **getParticipation**
```swift
    open class func getParticipation(id: UUID, completion: @escaping (_ data: Participation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

ParticipationAPI.getParticipation(id: id) { (response, error) in
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

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getParticipations**
```swift
    open class func getParticipations(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Participation]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

ParticipationAPI.getParticipations(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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

[**[Participation]**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateParticipation**
```swift
    open class func updateParticipation(id: UUID, participationUpdate: ParticipationUpdate, completion: @escaping (_ data: Participation?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let participationUpdate = ParticipationUpdate(acquiredAt: Date(), boardAppointment: false, companyName: "companyName_example", controlAgreement: false, legalForm: "legalForm_example", ownershipPct: "ownershipPct_example", purposeVehicle: false, votingMajority: false) // ParticipationUpdate | 

ParticipationAPI.updateParticipation(id: id, participationUpdate: participationUpdate) { (response, error) in
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
 **participationUpdate** | [**ParticipationUpdate**](ParticipationUpdate.md) |  | 

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

