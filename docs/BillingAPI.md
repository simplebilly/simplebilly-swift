# BillingAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPlans**](BillingAPI.md#getplans) | **GET** /api/v1/plans | All canonical plans (free/starter/business/enterprise) — the single source of truth lives in &#x60;crate::saasy::plans&#x60;, matching marketing.
[**getQuotaApi**](BillingAPI.md#getquotaapi) | **GET** /api/v1/quota | Effective limits + current usage for the calling tenant.
[**getSubscriptionApi**](BillingAPI.md#getsubscriptionapi) | **GET** /api/v1/subscription | 
[**getUsageApi**](BillingAPI.md#getusageapi) | **GET** /api/v1/usage | 
[**paddleSubscriptionWebhook**](BillingAPI.md#paddlesubscriptionwebhook) | **POST** /api/webhooks/paddle/subscription | Paddle Billing subscription webhook. Verifies the &#x60;Paddle-Signature&#x60; header (HMAC-SHA256 over &#x60;\&quot;{ts}:{raw_body}\&quot;&#x60; with the webhook secret), then updates &#x60;billing_info&#x60; and &#x60;tenants.plan&#x60; for the tenant identified by the subscription &#x60;custom_data&#x60; (JSON &#x60;{\&quot;tenant_id\&quot;: \&quot;...\&quot;}&#x60; or a bare tenant UUID).
[**putQuotaApi**](BillingAPI.md#putquotaapi) | **PUT** /api/v1/quota | Write the per-tenant quota override (&#x60;admin:settings&#x60;). An empty object clears the override.


# **getPlans**
```swift
    open class func getPlans(completion: @escaping (_ data: ApiResponseVecPlan?, _ error: Error?) -> Void)
```

All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.
BillingAPI.getPlans() { (response, error) in
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

[**ApiResponseVecPlan**](ApiResponseVecPlan.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getQuotaApi**
```swift
    open class func getQuotaApi(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Effective limits + current usage for the calling tenant.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Effective limits + current usage for the calling tenant.
BillingAPI.getQuotaApi() { (response, error) in
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

# **getSubscriptionApi**
```swift
    open class func getSubscriptionApi(completion: @escaping (_ data: ApiResponseSubscriptionOverview?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


BillingAPI.getSubscriptionApi() { (response, error) in
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

[**ApiResponseSubscriptionOverview**](ApiResponseSubscriptionOverview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUsageApi**
```swift
    open class func getUsageApi(meter: String? = nil, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let meter = "meter_example" // String |  (optional)

BillingAPI.getUsageApi(meter: meter) { (response, error) in
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
 **meter** | **String** |  | [optional] 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paddleSubscriptionWebhook**
```swift
    open class func paddleSubscriptionWebhook(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).
BillingAPI.paddleSubscriptionWebhook() { (response, error) in
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

# **putQuotaApi**
```swift
    open class func putQuotaApi(quotaOverride: QuotaOverride, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Write the per-tenant quota override (`admin:settings`). An empty object clears the override.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let quotaOverride = QuotaOverride(features: QuotaOverrideFeatures(erp: false, fancyReports: false, taxAutomations: false), maxConnectors: 123, maxInvoicesPerMonth: 123, maxUsers: 123, metered: "TODO", plan: "plan_example") // QuotaOverride | 

// Write the per-tenant quota override (`admin:settings`). An empty object clears the override.
BillingAPI.putQuotaApi(quotaOverride: quotaOverride) { (response, error) in
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
 **quotaOverride** | [**QuotaOverride**](QuotaOverride.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

