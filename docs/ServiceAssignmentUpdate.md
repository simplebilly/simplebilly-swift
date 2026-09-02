# ServiceAssignmentUpdate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**employeeId** | **UUID** | References the employees entity. | [optional] 
**jobId** | **UUID** | References the service_jobs entity. | [optional] 
**notes** | **String** |  | [optional] 
**scheduledDate** | **Date** | Work day the assignment is scheduled for. | [optional] 
**scheduledEnd** | **String** | Planned end time of the assignment. | [optional] 
**scheduledStart** | **String** | Planned start time of the assignment. | [optional] 
**status** | [**ServiceAssignmentStatus**](ServiceAssignmentStatus.md) | Assignment lifecycle status: \&quot;planned\&quot;, \&quot;confirmed\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot; or \&quot;cancelled\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


