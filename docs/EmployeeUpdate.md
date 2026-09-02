# EmployeeUpdate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **String** |  | [optional] 
**backupEmployeeId** | **UUID** | References another employee who covers when this employee is absent. | [optional] 
**bic** | **String** |  | [optional] 
**city** | **String** |  | [optional] 
**country** | [**CountryCode**](CountryCode.md) |  | [optional] 
**dateOfBirth** | **Date** |  | [optional] 
**departmentId** | **UUID** | References the department entity. | [optional] 
**email** | **String** |  | [optional] 
**firstName** | **String** |  | [optional] 
**gender** | [**Gender**](Gender.md) | Gender for pay-transparency reporting: \&quot;male\&quot;, \&quot;female\&quot; or \&quot;diverse\&quot;. | [optional] 
**hireDate** | **Date** |  | [optional] 
**hourlyCost** | **String** | Hourly cost rate in EUR for labor-cost reporting; when unset the rate is derived from &#x60;monthly_salary / (weekly_hours * 4.33)&#x60;. | [optional] 
**iban** | **String** |  | [optional] 
**jobTitle** | **String** |  | [optional] 
**lastLogin** | **Date** |  | [optional] 
**lastName** | **String** |  | [optional] 
**lastUpdated** | **Date** |  | [optional] 
**monthlySalary** | **String** | Gross monthly salary in EUR for pay-transparency reporting. | [optional] 
**phone** | **String** |  | [optional] 
**state** | **String** |  | [optional] 
**status** | [**EmployeeStatus**](EmployeeStatus.md) |  | [optional] 
**userId** | **UUID** | References the user entity. | [optional] 
**weeklyHours** | **String** | Contractual weekly working hours for pay-transparency normalization. | [optional] 
**zip** | **String** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


