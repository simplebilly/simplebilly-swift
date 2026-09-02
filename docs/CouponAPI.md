# CouponAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**couponRestore**](CouponAPI.md#couponrestore) | **POST** /api/v1/coupons/{coupon_id}/restore | 
[**createCoupon**](CouponAPI.md#createcoupon) | **POST** /api/v1/coupons | 
[**deleteCoupon**](CouponAPI.md#deletecoupon) | **DELETE** /api/v1/coupons/{coupon_id} | 
[**getCoupon**](CouponAPI.md#getcoupon) | **GET** /api/v1/coupons/{coupon_id} | 
[**listCoupons**](CouponAPI.md#listcoupons) | **GET** /api/v1/coupons/ | 
[**updateCoupon**](CouponAPI.md#updatecoupon) | **PUT** /api/v1/coupons/{coupon_id} | 


# **couponRestore**
```swift
    open class func couponRestore(couponId: String, completion: @escaping (_ data: Coupon?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let couponId = "couponId_example" // String | 

CouponAPI.couponRestore(couponId: couponId) { (response, error) in
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
 **couponId** | **String** |  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createCoupon**
```swift
    open class func createCoupon(couponCreate: CouponCreate, completion: @escaping (_ data: Coupon?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let couponCreate = CouponCreate(code: "code_example", description: "description_example", discountType: DiscountType(), discountValue: "discountValue_example", expiresAt: Date(), isActive: false, isCombineable: false, maxDiscountAmount: "maxDiscountAmount_example", maxUses: 123, maxUsesPerCustomer: 123, minOrderAmount: "minOrderAmount_example", productIds: 123, startsAt: Date()) // CouponCreate | 

CouponAPI.createCoupon(couponCreate: couponCreate) { (response, error) in
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
 **couponCreate** | [**CouponCreate**](CouponCreate.md) |  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteCoupon**
```swift
    open class func deleteCoupon(couponId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let couponId = "couponId_example" // String | 

CouponAPI.deleteCoupon(couponId: couponId) { (response, error) in
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
 **couponId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCoupon**
```swift
    open class func getCoupon(couponId: String, completion: @escaping (_ data: Coupon?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let couponId = "couponId_example" // String | 

CouponAPI.getCoupon(couponId: couponId) { (response, error) in
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
 **couponId** | **String** |  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listCoupons**
```swift
    open class func listCoupons(page: Int? = nil, pageSize: Int? = nil, isActive: Bool? = nil, code: String? = nil, discountType: String? = nil, completion: @escaping (_ data: [Coupon]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let isActive = true // Bool |  (optional)
let code = "code_example" // String |  (optional)
let discountType = "discountType_example" // String |  (optional)

CouponAPI.listCoupons(page: page, pageSize: pageSize, isActive: isActive, code: code, discountType: discountType) { (response, error) in
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
 **isActive** | **Bool** |  | [optional] 
 **code** | **String** |  | [optional] 
 **discountType** | **String** |  | [optional] 

### Return type

[**[Coupon]**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateCoupon**
```swift
    open class func updateCoupon(couponId: String, couponUpdate: CouponUpdate, completion: @escaping (_ data: Coupon?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let couponId = "couponId_example" // String | 
let couponUpdate = CouponUpdate(code: "code_example", description: "description_example", discountType: DiscountType(), discountValue: "discountValue_example", expiresAt: Date(), isActive: false, isCombineable: false, maxDiscountAmount: "maxDiscountAmount_example", maxUses: 123, maxUsesPerCustomer: 123, minOrderAmount: "minOrderAmount_example", productIds: 123, startsAt: Date()) // CouponUpdate | 

CouponAPI.updateCoupon(couponId: couponId, couponUpdate: couponUpdate) { (response, error) in
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
 **couponId** | **String** |  | 
 **couponUpdate** | [**CouponUpdate**](CouponUpdate.md) |  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

