# ApiResponseGdprExportData

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activityLog** | [GdprActivity] |  | 
**apiKeys** | [GdprApiKey] | Key identifiers and names only — never a usable credential. | 
**billing** | [GdprBillingInfo] |  | 
**exportedAt** | **Date** |  | 
**generatedByAi** | **Bool** | Honesty field: this document is a plain data dump, never AI-generated. | 
**notifications** | [GdprNotification] |  | 
**refreshTokens** | [GdprRefreshToken] | Session records: metadata only, never the token hash. | 
**tenants** | [GdprTenant] |  | 
**usageEvents** | [GdprUsageEvent] |  | 
**user** | [**GdprUser**](GdprUser.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


