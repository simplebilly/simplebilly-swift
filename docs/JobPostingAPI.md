# JobPostingAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createJobPosting**](JobPostingAPI.md#createjobposting) | **POST** /api/v1/job-postings | 
[**deleteJobPosting**](JobPostingAPI.md#deletejobposting) | **DELETE** /api/v1/job-postings/{id} | 
[**getJobPosting**](JobPostingAPI.md#getjobposting) | **GET** /api/v1/job-postings/{id} | 
[**listJobPostings**](JobPostingAPI.md#listjobpostings) | **GET** /api/v1/job-postings | 
[**updateJobPosting**](JobPostingAPI.md#updatejobposting) | **PUT** /api/v1/job-postings/{id} | 


# **createJobPosting**
```swift
    open class func createJobPosting(jobPostingCreate: JobPostingCreate, completion: @escaping (_ data: JobPosting?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let jobPostingCreate = JobPostingCreate(currency: "currency_example", department: "department_example", description: "description_example", employmentType: EmploymentType(), location: "location_example", remote: false, requiredSkills: 123, requirements: "requirements_example", salaryMax: 123, salaryMin: 123, status: JobPostingStatus(), title: "title_example") // JobPostingCreate | 

JobPostingAPI.createJobPosting(jobPostingCreate: jobPostingCreate) { (response, error) in
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
 **jobPostingCreate** | [**JobPostingCreate**](JobPostingCreate.md) |  | 

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteJobPosting**
```swift
    open class func deleteJobPosting(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

JobPostingAPI.deleteJobPosting(id: id) { (response, error) in
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

# **getJobPosting**
```swift
    open class func getJobPosting(id: UUID, completion: @escaping (_ data: JobPosting?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

JobPostingAPI.getJobPosting(id: id) { (response, error) in
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

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listJobPostings**
```swift
    open class func listJobPostings(status: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: [JobPosting]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let status = "status_example" // String |  (optional)
let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)

JobPostingAPI.listJobPostings(status: status, page: page, pageSize: pageSize) { (response, error) in
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
 **status** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] 
 **pageSize** | **Int** |  | [optional] 

### Return type

[**[JobPosting]**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateJobPosting**
```swift
    open class func updateJobPosting(id: UUID, jobPostingUpdate: JobPostingUpdate, completion: @escaping (_ data: JobPosting?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let jobPostingUpdate = JobPostingUpdate(currency: "currency_example", department: "department_example", description: "description_example", employmentType: EmploymentType(), location: "location_example", remote: false, requiredSkills: 123, requirements: "requirements_example", salaryMax: 123, salaryMin: 123, status: JobPostingStatus(), title: "title_example") // JobPostingUpdate | 

JobPostingAPI.updateJobPosting(id: id, jobPostingUpdate: jobPostingUpdate) { (response, error) in
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
 **jobPostingUpdate** | [**JobPostingUpdate**](JobPostingUpdate.md) |  | 

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

