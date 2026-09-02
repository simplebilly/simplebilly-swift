# BudgetsAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**budgetsApi**](BudgetsAPI.md#budgetsapi) | **GET** /api/v1/bookkeeping/budgets | 
[**upsertBudgetGoalApi**](BudgetsAPI.md#upsertbudgetgoalapi) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} | 


# **budgetsApi**
```swift
    open class func budgetsApi(year: Int, month: Int, completion: @escaping (_ data: BudgetErgebnis?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let year = 987 // Int | 
let month = 987 // Int | 

BudgetsAPI.budgetsApi(year: year, month: month) { (response, error) in
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
 **year** | **Int** |  | 
 **month** | **Int** |  | 

### Return type

[**BudgetErgebnis**](BudgetErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsertBudgetGoalApi**
```swift
    open class func upsertBudgetGoalApi(category: String, budgetGoalRequest: BudgetGoalRequest, completion: @escaping (_ data: Budget?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let category = "category_example" // String | 
let budgetGoalRequest = BudgetGoalRequest(monthlyGoal: "monthlyGoal_example", year: 123) // BudgetGoalRequest | 

BudgetsAPI.upsertBudgetGoalApi(category: category, budgetGoalRequest: budgetGoalRequest) { (response, error) in
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
 **category** | **String** |  | 
 **budgetGoalRequest** | [**BudgetGoalRequest**](BudgetGoalRequest.md) |  | 

### Return type

[**Budget**](Budget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

