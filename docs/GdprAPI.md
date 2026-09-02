# GdprAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**acceptDpa**](GdprAPI.md#acceptdpa) | **PUT** /api/v1/gdpr/dpa | Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
[**accountErasure**](GdprAPI.md#accounterasure) | **POST** /api/v1/gdpr/account-erasure | Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
[**erasureContact**](GdprAPI.md#erasurecontact) | **POST** /api/v1/gdpr/erasure/{contact_id} | Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on &#x60;contacts&#x60; already records who/when.
[**exportContactData**](GdprAPI.md#exportcontactdata) | **GET** /api/v1/gdpr/export/{contact_id} | Art. 15 data-subject access export for a contact.
[**exportGdpr**](GdprAPI.md#exportgdpr) | **GET** /api/v1/gdpr/export | Export the current user&#39;s personal data (GDPR Art. 15/20).
[**getDpa**](GdprAPI.md#getdpa) | **GET** /api/v1/gdpr/dpa | Current DPA acceptance status (from tenant_settings).


# **acceptDpa**
```swift
    open class func acceptDpa(dpaAcceptRequest: DpaAcceptRequest, completion: @escaping (_ data: DpaStatus?, _ error: Error?) -> Void)
```

Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let dpaAcceptRequest = DpaAcceptRequest(acceptedByName: "acceptedByName_example", version: "version_example") // DpaAcceptRequest | 

// Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
GdprAPI.acceptDpa(dpaAcceptRequest: dpaAcceptRequest) { (response, error) in
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
 **dpaAcceptRequest** | [**DpaAcceptRequest**](DpaAcceptRequest.md) |  | 

### Return type

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountErasure**
```swift
    open class func accountErasure(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).

Anonymizes every contact, anonymizes personal fields on bookkeeping records (orders/invoices/payments keep amounts and dates for GoBD), removes the tenant linkage of the (global, saasy-framework) users and marks the erasure on `tenant_settings.gdpr_erased_at`. No row is physically deleted. The audit triggers on the touched tables record who/when.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
GdprAPI.accountErasure() { (response, error) in
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

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **erasureContact**
```swift
    open class func erasureContact(contactId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let contactId = "contactId_example" // String | 

// Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.
GdprAPI.erasureContact(contactId: contactId) { (response, error) in
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
 **contactId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportContactData**
```swift
    open class func exportContactData(contactId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Art. 15 data-subject access export for a contact.

Returns the contact itself plus the tenant-scoped rows linked to it.  ## Relations The `customers`/`orders`/`invoices`/`payments` tables have no FK to `contacts`; they are linked through the `customer_id` column, which per the app's conventions holds one of: - the admin customer's `customer_id` (a UUID, often the same value as   the contact's `contact_id`/`customer_number`), - the buyer's email for shop orders, or - the marketplace's external customer id for plugin orders.  The export therefore matches the contact's identifiers (`contact_id`, `customer_number`, `external_id`, `email`) plus any resolved customer ids against `customer_id`. `delivery_notes` and `customer_communications` reference contacts directly via `contact_id`. Soft-deleted rows are included (their data is still processed and retained for GoBD). Relations that genuinely do not exist for a contact stay empty but the key is always present.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let contactId = "contactId_example" // String | 

// Art. 15 data-subject access export for a contact.
GdprAPI.exportContactData(contactId: contactId) { (response, error) in
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
 **contactId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportGdpr**
```swift
    open class func exportGdpr(completion: @escaping (_ data: ApiResponseGdprExport?, _ error: Error?) -> Void)
```

Export the current user's personal data (GDPR Art. 15/20).

No admin permission required: a user always exports their own data.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Export the current user's personal data (GDPR Art. 15/20).
GdprAPI.exportGdpr() { (response, error) in
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

[**ApiResponseGdprExport**](ApiResponseGdprExport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDpa**
```swift
    open class func getDpa(completion: @escaping (_ data: DpaStatus?, _ error: Error?) -> Void)
```

Current DPA acceptance status (from tenant_settings).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Current DPA acceptance status (from tenant_settings).
GdprAPI.getDpa() { (response, error) in
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

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

