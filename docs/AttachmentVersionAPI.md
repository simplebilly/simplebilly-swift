# AttachmentVersionAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAttachmentVersion**](AttachmentVersionAPI.md#createattachmentversion) | **POST** /api/v1/attachments/{attachment_id}/versions | 
[**listAttachmentVersions**](AttachmentVersionAPI.md#listattachmentversions) | **GET** /api/v1/attachments/{attachment_id}/versions | 
[**restoreAttachmentVersion**](AttachmentVersionAPI.md#restoreattachmentversion) | **POST** /api/v1/attachments/{attachment_id}/versions/{version_id}/restore | 


# **createAttachmentVersion**
```swift
    open class func createAttachmentVersion(attachmentId: UUID, newVersionRequest: NewVersionRequest, completion: @escaping (_ data: AttachmentVersion?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attachmentId = 987 // UUID | 
let newVersionRequest = NewVersionRequest(fileName: "fileName_example", fileSize: 123, mimeType: "mimeType_example", originalName: "originalName_example", sha256Hash: "sha256Hash_example") // NewVersionRequest | 

AttachmentVersionAPI.createAttachmentVersion(attachmentId: attachmentId, newVersionRequest: newVersionRequest) { (response, error) in
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
 **newVersionRequest** | [**NewVersionRequest**](NewVersionRequest.md) |  | 

### Return type

[**AttachmentVersion**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAttachmentVersions**
```swift
    open class func listAttachmentVersions(attachmentId: UUID, completion: @escaping (_ data: [AttachmentVersion]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attachmentId = 987 // UUID | 

AttachmentVersionAPI.listAttachmentVersions(attachmentId: attachmentId) { (response, error) in
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

### Return type

[**[AttachmentVersion]**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restoreAttachmentVersion**
```swift
    open class func restoreAttachmentVersion(attachmentId: UUID, versionId: UUID, completion: @escaping (_ data: Attachment?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let attachmentId = 987 // UUID | 
let versionId = 987 // UUID | 

AttachmentVersionAPI.restoreAttachmentVersion(attachmentId: attachmentId, versionId: versionId) { (response, error) in
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
 **versionId** | **UUID** |  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

