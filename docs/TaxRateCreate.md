# TaxRateCreate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countryCode** | **String** | ISO 3166-1 alpha-2 country code. | 
**effectiveFrom** | **Date** | Date this rate took effect; &#x60;None&#x60; &#x3D; not date-bound. | [optional] 
**isDefault** | **Bool** | Default rate for the country (one per country); fallback for lookups when no dated rate applies. | 
**name** | **String** | Human name, e.g. \&quot;VAT\&quot;. | 
**ratePercent** | **Int64** | Rate in hundredths of a percent: 1900 &#x3D; 19.00%. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


