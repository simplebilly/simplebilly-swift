# Absence

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**absenceType** | [**AbsenceType**](AbsenceType.md) | One of \&quot;vacation\&quot;, \&quot;sick\&quot;, \&quot;sabbatical\&quot;, \&quot;parental\&quot;, \&quot;other\&quot;. | [optional] 
**approvedAt** | **Date** |  | [optional] 
**approvedBy** | **UUID** | References the user entity. | [optional] 
**createdAt** | **Date** |  | [optional] 
**deletedAt** | **Date** |  | [optional] 
**employeeId** | **UUID** | References the employee entity. | [optional] 
**endDate** | **Date** |  | [optional] 
**id** | **UUID** |  | [optional] 
**notes** | **String** |  | [optional] 
**startDate** | **Date** |  | [optional] 
**status** | [**AbsenceStatus**](AbsenceStatus.md) | One of \&quot;pending\&quot;, \&quot;approved\&quot;, \&quot;rejected\&quot;, \&quot;cancelled\&quot;. | [optional] 
**tenantId** | **UUID** |  | [optional] 
**updatedAt** | **Date** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


