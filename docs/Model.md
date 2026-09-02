# Model

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backupCodes** | **[String]** |  | 
**createdAt** | **Date** |  | 
**deletedAt** | **Date** |  | [optional] 
**email** | **String** |  | 
**emailVerified** | **Bool** |  | 
**id** | **UUID** |  | 
**isActive** | **Bool** |  | 
**isTotpEnabled** | **Bool** |  | 
**lastLogin** | **Date** |  | [optional] 
**name** | **String** |  | 
**oauthId** | **String** |  | [optional] 
**oauthProvider** | **String** |  | [optional] 
**passwordChangedAt** | **Date** | Set on password change; auth/refresh tokens issued before this timestamp are rejected by the auth middleware. | [optional] 
**passwordHash** | **String** |  | 
**picture** | **String** |  | [optional] 
**privacyAcceptedAt** | **Date** | When the user accepted the data privacy policy (GDPR consent record). | [optional] 
**totpSecret** | **String** |  | [optional] 
**updatedAt** | **Date** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


