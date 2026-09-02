# ComplianceTraining

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assignable** | **Bool** | Whether HR can assign this training as required for employees. | [optional] 
**code** | **String** | Stable code used by plugins and frontend players (e.g. \&quot;data_privacy\&quot;). | [optional] 
**createdAt** | **Date** |  | [optional] 
**deletedAt** | **Date** |  | [optional] 
**description** | **String** |  | [optional] 
**id** | **UUID** |  | [optional] 
**passScore** | **Int** | Minimum score (0–100) required to pass. | [optional] 
**pluginPlatform** | **String** | Marketplace plugin platform id when source &#x3D; Plugin. | [optional] 
**source** | [**TrainingSource**](TrainingSource.md) |  | [optional] 
**tenantId** | **UUID** |  | [optional] 
**title** | **String** |  | [optional] 
**updatedAt** | **Date** |  | [optional] 
**validityMonths** | **Int** | Certificate validity in months; null &#x3D; no expiry. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


