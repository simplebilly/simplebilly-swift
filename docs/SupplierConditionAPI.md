# SupplierConditionAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSupplierCondition**](SupplierConditionAPI.md#createsuppliercondition) | **POST** /api/v1/supplier-conditions | 
[**deleteSupplierCondition**](SupplierConditionAPI.md#deletesuppliercondition) | **DELETE** /api/v1/supplier-conditions/{supplier_condition_id} | 
[**getSupplierCondition**](SupplierConditionAPI.md#getsuppliercondition) | **GET** /api/v1/supplier-conditions/{supplier_condition_id} | 
[**listSupplierConditions**](SupplierConditionAPI.md#listsupplierconditions) | **GET** /api/v1/supplier-conditions/ | 
[**updateSupplierCondition**](SupplierConditionAPI.md#updatesuppliercondition) | **PUT** /api/v1/supplier-conditions/{supplier_condition_id} | 


# **createSupplierCondition**
```swift
    open class func createSupplierCondition(supplierConditionCreate: SupplierConditionCreate, completion: @escaping (_ data: SupplierCondition?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierConditionCreate = SupplierConditionCreate(currency: "currency_example", deliveryTerms: "deliveryTerms_example", earlyPaymentDiscountPercent: "earlyPaymentDiscountPercent_example", isDefault: false, minimumOrderValue: "minimumOrderValue_example", notes: "notes_example", paymentDueDays: 123, paymentTerms: "paymentTerms_example", supplierContactId: "supplierContactId_example", supplierName: "supplierName_example", volumeDiscountTiers: 123) // SupplierConditionCreate | 

SupplierConditionAPI.createSupplierCondition(supplierConditionCreate: supplierConditionCreate) { (response, error) in
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
 **supplierConditionCreate** | [**SupplierConditionCreate**](SupplierConditionCreate.md) |  | 

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteSupplierCondition**
```swift
    open class func deleteSupplierCondition(supplierConditionId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierConditionId = "supplierConditionId_example" // String | 

SupplierConditionAPI.deleteSupplierCondition(supplierConditionId: supplierConditionId) { (response, error) in
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
 **supplierConditionId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSupplierCondition**
```swift
    open class func getSupplierCondition(supplierConditionId: String, completion: @escaping (_ data: SupplierCondition?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierConditionId = "supplierConditionId_example" // String | 

SupplierConditionAPI.getSupplierCondition(supplierConditionId: supplierConditionId) { (response, error) in
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
 **supplierConditionId** | **String** |  | 

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listSupplierConditions**
```swift
    open class func listSupplierConditions(page: Int? = nil, pageSize: Int? = nil, supplierContactId: String? = nil, search: String? = nil, completion: @escaping (_ data: [SupplierCondition]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let supplierContactId = "supplierContactId_example" // String |  (optional)
let search = "search_example" // String |  (optional)

SupplierConditionAPI.listSupplierConditions(page: page, pageSize: pageSize, supplierContactId: supplierContactId, search: search) { (response, error) in
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
 **supplierContactId** | **String** |  | [optional] 
 **search** | **String** |  | [optional] 

### Return type

[**[SupplierCondition]**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateSupplierCondition**
```swift
    open class func updateSupplierCondition(supplierConditionId: String, supplierConditionUpdate: SupplierConditionUpdate, completion: @escaping (_ data: SupplierCondition?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let supplierConditionId = "supplierConditionId_example" // String | 
let supplierConditionUpdate = SupplierConditionUpdate(currency: "currency_example", deliveryTerms: "deliveryTerms_example", earlyPaymentDiscountPercent: "earlyPaymentDiscountPercent_example", isDefault: false, minimumOrderValue: "minimumOrderValue_example", notes: "notes_example", paymentDueDays: 123, paymentTerms: "paymentTerms_example", supplierContactId: "supplierContactId_example", supplierName: "supplierName_example", volumeDiscountTiers: 123) // SupplierConditionUpdate | 

SupplierConditionAPI.updateSupplierCondition(supplierConditionId: supplierConditionId, supplierConditionUpdate: supplierConditionUpdate) { (response, error) in
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
 **supplierConditionId** | **String** |  | 
 **supplierConditionUpdate** | [**SupplierConditionUpdate**](SupplierConditionUpdate.md) |  | 

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

