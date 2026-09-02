# LegalDocumentAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getLegalDocuments**](LegalDocumentAPI.md#getlegaldocuments) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
[**resetLegalDocuments**](LegalDocumentAPI.md#resetlegaldocuments) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
[**upsertLegalDocuments**](LegalDocumentAPI.md#upsertlegaldocuments) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list.


# **getLegalDocuments**
```swift
    open class func getLegalDocuments(completion: @escaping (_ data: [LegalDocument]?, _ error: Error?) -> Void)
```

List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
LegalDocumentAPI.getLegalDocuments() { (response, error) in
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

[**[LegalDocument]**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resetLegalDocuments**
```swift
    open class func resetLegalDocuments(legalDocumentReset: LegalDocumentReset, completion: @escaping (_ data: [LegalDocument]?, _ error: Error?) -> Void)
```

Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let legalDocumentReset = LegalDocumentReset(docType: "docType_example", lang: "lang_example") // LegalDocumentReset | 

// Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
LegalDocumentAPI.resetLegalDocuments(legalDocumentReset: legalDocumentReset) { (response, error) in
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
 **legalDocumentReset** | [**LegalDocumentReset**](LegalDocumentReset.md) |  | 

### Return type

[**[LegalDocument]**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsertLegalDocuments**
```swift
    open class func upsertLegalDocuments(legalDocumentUpsert: [LegalDocumentUpsert], completion: @escaping (_ data: [LegalDocument]?, _ error: Error?) -> Void)
```

Upsert legal documents per (doc_type, lang). Returns the full tenant list.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let legalDocumentUpsert = [LegalDocumentUpsert(content: "content_example", docType: "docType_example", lang: "lang_example", title: "title_example")] // [LegalDocumentUpsert] | 

// Upsert legal documents per (doc_type, lang). Returns the full tenant list.
LegalDocumentAPI.upsertLegalDocuments(legalDocumentUpsert: legalDocumentUpsert) { (response, error) in
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
 **legalDocumentUpsert** | [**[LegalDocumentUpsert]**](LegalDocumentUpsert.md) |  | 

### Return type

[**[LegalDocument]**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

