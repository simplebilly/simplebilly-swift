# ProductVariant

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**barcode** | **String** |  | [optional] 
**imageLink** | **String** |  | [optional] 
**isActive** | **Bool** |  | [optional] 
**name** | **String** | Human-readable variant label, e.g. \&quot;Red / M\&quot;. | [optional] 
**optionValues** | **AnyCodable** | Option name → value map, e.g. &#x60;{\&quot;Color\&quot;: \&quot;Red\&quot;, \&quot;Size\&quot;: \&quot;M\&quot;}&#x60;. | [optional] 
**price** | **String** | Explicit override price for this variant (takes precedence over parent price + delta). | [optional] 
**priceDelta** | **String** | Price adjustment relative to the parent product&#39;s &#x60;default_price&#x60;. | [optional] 
**productId** | **UUID** | The parent product this variant belongs to. References the product entity. | 
**sku** | **String** | Variant-specific SKU (must be unique per tenant). | 
**stockQuantity** | **Int64** | Variant-level stock (optional — may be tracked on the parent only). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


