# JobApplicationAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**applyPublic**](JobApplicationAPI.md#applypublic) | **POST** /api/v1/public/jobs/{posting_id}/apply | 
[**deleteJobApplication**](JobApplicationAPI.md#deletejobapplication) | **DELETE** /api/v1/job-applications/{application_id} | 
[**downloadCv**](JobApplicationAPI.md#downloadcv) | **GET** /api/v1/job-applications/{application_id}/cv | 
[**getJobApplication**](JobApplicationAPI.md#getjobapplication) | **GET** /api/v1/job-applications/{application_id} | 
[**inboundEmail**](JobApplicationAPI.md#inboundemail) | **POST** /api/v1/public/jobs/inbound-email | Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with &#x60;from&#x60;, &#x60;subject&#x60;, &#x60;body-plain&#x60; and one or more &#x60;attachment-N&#x60; file fields. The subject may reference a posting as &#x60;[JOB-&lt;posting_id&gt;]&#x60;; without one the application lands in the general inbox.
[**listJobApplications**](JobApplicationAPI.md#listjobapplications) | **GET** /api/v1/job-applications | 
[**listPublicPostings**](JobApplicationAPI.md#listpublicpostings) | **GET** /api/v1/public/jobs | 
[**scoreJobApplication**](JobApplicationAPI.md#scorejobapplication) | **POST** /api/v1/job-applications/{application_id}/score | 
[**updateJobApplicationStatus**](JobApplicationAPI.md#updatejobapplicationstatus) | **PATCH** /api/v1/job-applications/{application_id}/status | 


# **applyPublic**
```swift
    open class func applyPublic(postingId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let postingId = 987 // UUID | 

JobApplicationAPI.applyPublic(postingId: postingId) { (response, error) in
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
 **postingId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteJobApplication**
```swift
    open class func deleteJobApplication(applicationId: UUID, completion: @escaping (_ data: JobApplication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let applicationId = 987 // UUID | 

JobApplicationAPI.deleteJobApplication(applicationId: applicationId) { (response, error) in
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
 **applicationId** | **UUID** |  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **downloadCv**
```swift
    open class func downloadCv(applicationId: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let applicationId = 987 // UUID | 

JobApplicationAPI.downloadCv(applicationId: applicationId) { (response, error) in
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
 **applicationId** | **UUID** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getJobApplication**
```swift
    open class func getJobApplication(applicationId: UUID, completion: @escaping (_ data: JobApplication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let applicationId = 987 // UUID | 

JobApplicationAPI.getJobApplication(applicationId: applicationId) { (response, error) in
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
 **applicationId** | **UUID** |  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **inboundEmail**
```swift
    open class func inboundEmail(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.
JobApplicationAPI.inboundEmail() { (response, error) in
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

# **listJobApplications**
```swift
    open class func listJobApplications(postingId: UUID? = nil, status: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: [JobApplication]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let postingId = 987 // UUID |  (optional)
let status = "status_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

JobApplicationAPI.listJobApplications(postingId: postingId, status: status, page: page, pageSize: pageSize) { (response, error) in
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
 **postingId** | **UUID** |  | [optional] 
 **status** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**[JobApplication]**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPublicPostings**
```swift
    open class func listPublicPostings(completion: @escaping (_ data: [PublicPosting]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


JobApplicationAPI.listPublicPostings() { (response, error) in
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

[**[PublicPosting]**](PublicPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **scoreJobApplication**
```swift
    open class func scoreJobApplication(applicationId: UUID, completion: @escaping (_ data: JobApplication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let applicationId = 987 // UUID | 

JobApplicationAPI.scoreJobApplication(applicationId: applicationId) { (response, error) in
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
 **applicationId** | **UUID** |  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateJobApplicationStatus**
```swift
    open class func updateJobApplicationStatus(applicationId: UUID, applicationStatusDto: ApplicationStatusDto, completion: @escaping (_ data: JobApplication?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let applicationId = 987 // UUID | 
let applicationStatusDto = ApplicationStatusDto(postingId: 123, status: "status_example") // ApplicationStatusDto | 

JobApplicationAPI.updateJobApplicationStatus(applicationId: applicationId, applicationStatusDto: applicationStatusDto) { (response, error) in
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
 **applicationId** | **UUID** |  | 
 **applicationStatusDto** | [**ApplicationStatusDto**](ApplicationStatusDto.md) |  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

