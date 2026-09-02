# PostingCategoryAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPostingCategory**](PostingCategoryAPI.md#createpostingcategory) | **POST** /api/v1/posting-categories | 
[**deletePostingCategory**](PostingCategoryAPI.md#deletepostingcategory) | **DELETE** /api/v1/posting-categories/{category_id} | 
[**listPostingCategories**](PostingCategoryAPI.md#listpostingcategories) | **GET** /api/v1/posting-categories | 
[**seedPostingCategories**](PostingCategoryAPI.md#seedpostingcategories) | **POST** /api/v1/posting-categories/seed/{skr_version} | 
[**updatePostingCategory**](PostingCategoryAPI.md#updatepostingcategory) | **PUT** /api/v1/posting-categories/{category_id} | 


# **createPostingCategory**
```swift
    open class func createPostingCategory(body: AnyCodable, completion: @escaping (_ data: PostingCategory?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let body =  // AnyCodable | 

PostingCategoryAPI.createPostingCategory(body: body) { (response, error) in
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
 **body** | **AnyCodable** |  | 

### Return type

[**PostingCategory**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePostingCategory**
```swift
    open class func deletePostingCategory(categoryId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let categoryId = "categoryId_example" // String | 

PostingCategoryAPI.deletePostingCategory(categoryId: categoryId) { (response, error) in
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
 **categoryId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPostingCategories**
```swift
    open class func listPostingCategories(completion: @escaping (_ data: [PostingCategory]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


PostingCategoryAPI.listPostingCategories() { (response, error) in
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

[**[PostingCategory]**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **seedPostingCategories**
```swift
    open class func seedPostingCategories(skrVersion: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let skrVersion = "skrVersion_example" // String | 

PostingCategoryAPI.seedPostingCategories(skrVersion: skrVersion) { (response, error) in
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
 **skrVersion** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePostingCategory**
```swift
    open class func updatePostingCategory(categoryId: String, body: AnyCodable, completion: @escaping (_ data: PostingCategory?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let categoryId = "categoryId_example" // String | 
let body =  // AnyCodable | 

PostingCategoryAPI.updatePostingCategory(categoryId: categoryId, body: body) { (response, error) in
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
 **categoryId** | **String** |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**PostingCategory**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

