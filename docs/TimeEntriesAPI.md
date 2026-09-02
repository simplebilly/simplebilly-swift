# TimeEntriesAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clockInTimeEntry**](TimeEntriesAPI.md#clockintimeentry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile).
[**clockOutTimeEntry**](TimeEntriesAPI.md#clockouttimeentry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.
[**getLaborCosts**](TimeEntriesAPI.md#getlaborcosts) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.
[**listTimeEntries**](TimeEntriesAPI.md#listtimeentries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters.


# **clockInTimeEntry**
```swift
    open class func clockInTimeEntry(timeEntryClockIn: TimeEntryClockIn, completion: @escaping (_ data: TimeEntryDto?, _ error: Error?) -> Void)
```

Clock in for the authenticated user (resolved via their employee profile).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let timeEntryClockIn = TimeEntryClockIn(notes: "notes_example") // TimeEntryClockIn | 

// Clock in for the authenticated user (resolved via their employee profile).
TimeEntriesAPI.clockInTimeEntry(timeEntryClockIn: timeEntryClockIn) { (response, error) in
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
 **timeEntryClockIn** | [**TimeEntryClockIn**](TimeEntryClockIn.md) |  | 

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clockOutTimeEntry**
```swift
    open class func clockOutTimeEntry(id: UUID, timeEntryClockOut: TimeEntryClockOut, completion: @escaping (_ data: TimeEntryDto?, _ error: Error?) -> Void)
```

Clock out an entry: the entry's owner, or anyone with `time_entries:write`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let id = 987 // UUID | 
let timeEntryClockOut = TimeEntryClockOut(clockOut: Date(), hours: "hours_example") // TimeEntryClockOut | 

// Clock out an entry: the entry's owner, or anyone with `time_entries:write`.
TimeEntriesAPI.clockOutTimeEntry(id: id, timeEntryClockOut: timeEntryClockOut) { (response, error) in
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
 **timeEntryClockOut** | [**TimeEntryClockOut**](TimeEntryClockOut.md) |  | 

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getLaborCosts**
```swift
    open class func getLaborCosts(from: Date, to: Date, groupBy: String, completion: @escaping (_ data: [LaborCostRow]?, _ error: Error?) -> Void)
```

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let from = Date() // Date | 
let to = Date() // Date | 
let groupBy = "groupBy_example" // String | One of \"employee\", \"order\" or \"day\".

// Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.
TimeEntriesAPI.getLaborCosts(from: from, to: to, groupBy: groupBy) { (response, error) in
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
 **from** | **Date** |  | 
 **to** | **Date** |  | 
 **groupBy** | **String** | One of \&quot;employee\&quot;, \&quot;order\&quot; or \&quot;day\&quot;. | 

### Return type

[**[LaborCostRow]**](LaborCostRow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTimeEntries**
```swift
    open class func listTimeEntries(from: Date? = nil, to: Date? = nil, active: Bool? = nil, employeeId: UUID? = nil, completion: @escaping (_ data: [TimeEntryDto]?, _ error: Error?) -> Void)
```

List time entries with optional date-range / active / employee filters.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let from = Date() // Date |  (optional)
let to = Date() // Date |  (optional)
let active = true // Bool | Only currently running shifts (clock_in set, clock_out null). (optional)
let employeeId = 987 // UUID |  (optional)

// List time entries with optional date-range / active / employee filters.
TimeEntriesAPI.listTimeEntries(from: from, to: to, active: active, employeeId: employeeId) { (response, error) in
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
 **from** | **Date** |  | [optional] 
 **to** | **Date** |  | [optional] 
 **active** | **Bool** | Only currently running shifts (clock_in set, clock_out null). | [optional] 
 **employeeId** | **UUID** |  | [optional] 

### Return type

[**[TimeEntryDto]**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

