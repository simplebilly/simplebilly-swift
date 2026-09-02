# JobPostingCreate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **String** |  | [optional] 
**department** | **String** |  | [optional] 
**description** | **String** | What the job is; markdown/HTML. | 
**employmentType** | [**EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional] 
**location** | **String** |  | [optional] 
**remote** | **Bool** |  | 
**requiredSkills** | **AnyCodable** | List of required skill names (JSON array of strings). | 
**requirements** | **String** | Structured profile of the required candidate (skills, experience). | [optional] 
**salaryMax** | **Int** |  | [optional] 
**salaryMin** | **Int** |  | [optional] 
**status** | [**JobPostingStatus**](JobPostingStatus.md) | draft | published | closed | 
**title** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


