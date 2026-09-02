# SubmitResultDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**answers** | **[Int]** | Selected answer indices (required for scored builtin trainings). | 
**assignmentId** | **UUID** |  | [optional] 
**score** | **Int** | Score 0–100. Only trusted for plugin trainings without server-side scoring; builtin trainings are always re-scored from &#x60;answers&#x60;. | 
**trainingCode** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


