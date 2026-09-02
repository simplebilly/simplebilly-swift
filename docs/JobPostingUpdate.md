# JobPostingUpdate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **String** |  | [optional] 
**department** | **String** |  | [optional] 
**description** | **String** | What the job is; markdown/HTML. | [optional] 
**employmentType** | [**EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional] 
**location** | **String** |  | [optional] 
**remote** | **Bool** |  | [optional] 
**requiredSkills** | **AnyCodable** | List of required skill names (JSON array of strings). | [optional] 
**requirements** | **String** | Structured profile of the required candidate (skills, experience). | [optional] 
**salaryMax** | **Int** |  | [optional] 
**salaryMin** | **Int** |  | [optional] 
**status** | [**JobPostingStatus**](JobPostingStatus.md) | draft | published | closed | [optional] 
**title** | **String** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


