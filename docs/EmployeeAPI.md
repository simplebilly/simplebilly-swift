# EmployeeAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createEmployee**](EmployeeAPI.md#createemployee) | **POST** /api/v1/employees | 
[**deleteEmployee**](EmployeeAPI.md#deleteemployee) | **DELETE** /api/v1/employees/{id} | 
[**employeeRestore**](EmployeeAPI.md#employeerestore) | **POST** /api/v1/employees/{id}/restore | 
[**getEmployee**](EmployeeAPI.md#getemployee) | **GET** /api/v1/employees/{id} | 
[**getEmployeePayrollSummary**](EmployeeAPI.md#getemployeepayrollsummary) | **GET** /api/v1/employees/{id}/payroll-summary | 
[**getEmployees**](EmployeeAPI.md#getemployees) | **GET** /api/v1/employees/ | 
[**updateEmployee**](EmployeeAPI.md#updateemployee) | **PUT** /api/v1/employees/{id} | 


# **createEmployee**
```swift
    open class func createEmployee(employeeCreate: EmployeeCreate, completion: @escaping (_ data: Employee?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let employeeCreate = EmployeeCreate(address: "address_example", backupEmployeeId: 123, bic: "bic_example", city: "city_example", country: CountryCode(), dateOfBirth: Date(), departmentId: 123, email: "email_example", firstName: "firstName_example", gender: Gender(), hireDate: Date(), hourlyCost: "hourlyCost_example", iban: "iban_example", jobTitle: "jobTitle_example", lastLogin: Date(), lastName: "lastName_example", lastUpdated: Date(), monthlySalary: "monthlySalary_example", phone: "phone_example", state: "state_example", status: EmployeeStatus(), userId: 123, weeklyHours: "weeklyHours_example", zip: "zip_example") // EmployeeCreate | 

EmployeeAPI.createEmployee(employeeCreate: employeeCreate) { (response, error) in
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
 **employeeCreate** | [**EmployeeCreate**](EmployeeCreate.md) |  | 

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteEmployee**
```swift
    open class func deleteEmployee(id: UUID, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

EmployeeAPI.deleteEmployee(id: id) { (response, error) in
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

# **employeeRestore**
```swift
    open class func employeeRestore(id: UUID, completion: @escaping (_ data: Employee?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

EmployeeAPI.employeeRestore(id: id) { (response, error) in
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

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEmployee**
```swift
    open class func getEmployee(id: UUID, completion: @escaping (_ data: Employee?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 

EmployeeAPI.getEmployee(id: id) { (response, error) in
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

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEmployeePayrollSummary**
```swift
    open class func getEmployeePayrollSummary(id: UUID, year: Int? = nil, completion: @escaping (_ data: PayrollSummary?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let year = 987 // Int | Fiscal year for the breakdown; defaults to the current year. (optional)

EmployeeAPI.getEmployeePayrollSummary(id: id, year: year) { (response, error) in
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
 **year** | **Int** | Fiscal year for the breakdown; defaults to the current year. | [optional] 

### Return type

[**PayrollSummary**](PayrollSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEmployees**
```swift
    open class func getEmployees(page: Int? = nil, pageSize: Int? = nil, search: String? = nil, includeDeleted: Bool? = nil, completion: @escaping (_ data: [Employee]?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let page = 987 // Int |  (optional)
let pageSize = 987 // Int |  (optional)
let search = "search_example" // String |  (optional)
let includeDeleted = true // Bool | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

EmployeeAPI.getEmployees(page: page, pageSize: pageSize, search: search, includeDeleted: includeDeleted) { (response, error) in
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
 **search** | **String** |  | [optional] 
 **includeDeleted** | **Bool** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**[Employee]**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateEmployee**
```swift
    open class func updateEmployee(id: UUID, employeeUpdate: EmployeeUpdate, completion: @escaping (_ data: Employee?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let employeeUpdate = EmployeeUpdate(address: "address_example", backupEmployeeId: 123, bic: "bic_example", city: "city_example", country: CountryCode(), dateOfBirth: Date(), departmentId: 123, email: "email_example", firstName: "firstName_example", gender: Gender(), hireDate: Date(), hourlyCost: "hourlyCost_example", iban: "iban_example", jobTitle: "jobTitle_example", lastLogin: Date(), lastName: "lastName_example", lastUpdated: Date(), monthlySalary: "monthlySalary_example", phone: "phone_example", state: "state_example", status: EmployeeStatus(), userId: 123, weeklyHours: "weeklyHours_example", zip: "zip_example") // EmployeeUpdate | 

EmployeeAPI.updateEmployee(id: id, employeeUpdate: employeeUpdate) { (response, error) in
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
 **employeeUpdate** | [**EmployeeUpdate**](EmployeeUpdate.md) |  | 

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

