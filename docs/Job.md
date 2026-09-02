# Job

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **Int** |  | [optional] 
**jobType** | **String** | Discriminator the worker dispatches on (e.g. \&quot;webhook.deliver\&quot;). | 
**maxAttempts** | **Int** |  | 
**payload** | **AnyCodable** |  | [optional] 
**runAt** | **Date** | Earliest execution time; None &#x3D; run now. | [optional] 
**status** | [**JobStatus**](JobStatus.md) | pending | running | done | failed | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


