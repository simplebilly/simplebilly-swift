# Activity

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activityType** | [**ActivityType**](ActivityType.md) | One of: call | email | meeting | task | note | 
**assignedTo** | **String** | User responsible (&#x60;employee.employee_id&#x60;). | [optional] 
**contactId** | **String** | Contact this activity belongs to (&#x60;contact.contact_id&#x60;). References the contact entity. | [optional] 
**description** | **String** |  | [optional] 
**dueDate** | **Date** | Follow-up / Wiedervorlage date. Open activities with a due date in the past are overdue. | [optional] 
**reminderDate** | **Date** | When to remind about the follow-up. | [optional] 
**status** | [**ActivityStatus**](ActivityStatus.md) | One of: open | done | cancelled | 
**subject** | **String** | Short subject line. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


