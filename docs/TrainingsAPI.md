# TrainingsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMyTrainings**](TrainingsAPI.md#getmytrainings) | **GET** /api/v1/trainings/me | 
[**getTrainingContent**](TrainingsAPI.md#gettrainingcontent) | **GET** /api/v1/trainings/content/{code} | 
[**getTrainingOverview**](TrainingsAPI.md#gettrainingoverview) | **GET** /api/v1/trainings/overview | 
[**submitTrainingResult**](TrainingsAPI.md#submittrainingresult) | **POST** /api/v1/trainings/submit-result | 


# **getMyTrainings**
```swift
    open class func getMyTrainings(completion: @escaping (_ data: [MyTrainingItem]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


TrainingsAPI.getMyTrainings() { (response, error) in
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

[**[MyTrainingItem]**](MyTrainingItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTrainingContent**
```swift
    open class func getTrainingContent(code: String, completion: @escaping (_ data: TrainingContent?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let code = "code_example" // String | Training code, e.g. data_privacy

TrainingsAPI.getTrainingContent(code: code) { (response, error) in
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
 **code** | **String** | Training code, e.g. data_privacy | 

### Return type

[**TrainingContent**](TrainingContent.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTrainingOverview**
```swift
    open class func getTrainingOverview(completion: @escaping (_ data: [HrTrainingOverview]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


TrainingsAPI.getTrainingOverview() { (response, error) in
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

[**[HrTrainingOverview]**](HrTrainingOverview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **submitTrainingResult**
```swift
    open class func submitTrainingResult(submitResultDto: SubmitResultDto, completion: @escaping (_ data: SubmitResultResponse?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let submitResultDto = SubmitResultDto(answers: [123], assignmentId: 123, score: 123, trainingCode: "trainingCode_example") // SubmitResultDto | 

TrainingsAPI.submitTrainingResult(submitResultDto: submitResultDto) { (response, error) in
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
 **submitResultDto** | [**SubmitResultDto**](SubmitResultDto.md) |  | 

### Return type

[**SubmitResultResponse**](SubmitResultResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

