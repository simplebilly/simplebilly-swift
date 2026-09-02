# AttachmentAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**attachmentRestore**](AttachmentAPI.md#attachmentrestore) | **POST** /api/v1/attachments/{id}/restore | 
[**createAttachment**](AttachmentAPI.md#createattachment) | **POST** /api/v1/attachments | 
[**deleteAttachment**](AttachmentAPI.md#deleteattachment) | **DELETE** /api/v1/attachments/{id} | 
[**getAttachment**](AttachmentAPI.md#getattachment) | **GET** /api/v1/attachments/{id} | 
[**listAttachments**](AttachmentAPI.md#listattachments) | **GET** /api/v1/attachments/ | 
[**saveAttachmentOcrText**](AttachmentAPI.md#saveattachmentocrtext) | **PUT** /api/v1/attachments/{attachment_id}/ocr-text | Persist client-side OCR output for an attachment.


# **attachmentRestore**
```swift
    open class func attachmentRestore(id: UUID, completion: @escaping (_ data: Attachment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

AttachmentAPI.attachmentRestore(id: id) { (response, error) in
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

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createAttachment**
```swift
    open class func createAttachment(attachmentCreate: AttachmentCreate, completion: @escaping (_ data: Attachment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attachmentCreate = AttachmentCreate(contactId: "contactId_example", fileName: "fileName_example", fileSize: 123, mimeType: "mimeType_example", originalName: "originalName_example", pdfaPath: "pdfaPath_example", sha256Hash: "sha256Hash_example", uploadedBy: 123) // AttachmentCreate | 

AttachmentAPI.createAttachment(attachmentCreate: attachmentCreate) { (response, error) in
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
 **attachmentCreate** | [**AttachmentCreate**](AttachmentCreate.md) |  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAttachment**
```swift
    open class func deleteAttachment(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

AttachmentAPI.deleteAttachment(id: id) { (response, error) in
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

# **getAttachment**
```swift
    open class func getAttachment(id: UUID, completion: @escaping (_ data: Attachment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

AttachmentAPI.getAttachment(id: id) { (response, error) in
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

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAttachments**
```swift
    open class func listAttachments(page: Int? = nil, pageSize: Int? = nil, contactId: String? = nil, completion: @escaping (_ data: [Attachment]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let contactId = "contactId_example" // String |  (optional)

AttachmentAPI.listAttachments(page: page, pageSize: pageSize, contactId: contactId) { (response, error) in
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
 **contactId** | **String** |  | [optional] 

### Return type

[**[Attachment]**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **saveAttachmentOcrText**
```swift
    open class func saveAttachmentOcrText(attachmentId: UUID, ocrTextRequest: OcrTextRequest, completion: @escaping (_ data: Attachment?, _ error: Error?) -> Void)
```

Persist client-side OCR output for an attachment.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attachmentId = 987 // UUID | 
let ocrTextRequest = OcrTextRequest(ocrText: "ocrText_example") // OcrTextRequest | 

// Persist client-side OCR output for an attachment.
AttachmentAPI.saveAttachmentOcrText(attachmentId: attachmentId, ocrTextRequest: ocrTextRequest) { (response, error) in
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
 **attachmentId** | **UUID** |  | 
 **ocrTextRequest** | [**OcrTextRequest**](OcrTextRequest.md) |  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

