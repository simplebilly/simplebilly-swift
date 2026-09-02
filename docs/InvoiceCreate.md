# InvoiceCreate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **AnyCodable** |  | [optional] 
**billingPeriodEnd** | **Date** |  | [optional] 
**billingPeriodStart** | **Date** |  | [optional] 
**cancellationDate** | **Date** |  | [optional] 
**cancellationInvoiceId** | **String** | References the invoice entity. | [optional] 
**cancellationReason** | **String** |  | [optional] 
**contractId** | **UUID** | References the contract entity. | [optional] 
**currency** | [**CurrencyCode**](CurrencyCode.md) |  | 
**customerId** | **String** | References the customer entity. | [optional] 
**discountAmount** | **String** |  | [optional] 
**discountDays** | **Int** |  | [optional] 
**discountPercentage** | **String** |  | [optional] 
**documentType** | [**DocumentType**](DocumentType.md) |  | [optional] 
**dunningLevel** | **Int** |  | [optional] 
**inputVatAmount** | **String** |  | [optional] 
**inputVatDeductible** | **Bool** |  | [optional] 
**inputVatPercentage** | **String** |  | [optional] 
**introductionText** | **String** |  | [optional] 
**invoiceType** | [**InvoiceType**](InvoiceType.md) |  | 
**isCancelled** | **Bool** |  | [optional] 
**isDraft** | **Bool** |  | [optional] 
**isEuAcquisition** | **Bool** |  | [optional] 
**isEuDelivery** | **Bool** |  | [optional] 
**isIntraCommunityAcquisition** | **Bool** |  | [optional] 
**isReverseCharge** | **Bool** |  | [optional] 
**issueDate** | **Date** |  | 
**ledgerAccount** | **String** |  | [optional] 
**lineItems** | **AnyCodable** |  | 
**margin25a** | **Bool** |  | [optional] 
**margin25aGross** | **String** |  | [optional] 
**margin25aPurchasePrice** | **String** |  | [optional] 
**notes** | **String** |  | [optional] 
**orderNumber** | **String** |  | [optional] 
**originalPdfPath** | **String** |  | [optional] 
**paidAmount** | **String** |  | [optional] 
**paymentDueDate** | **Date** |  | [optional] 
**paymentStatus** | [**PaymentStatus**](PaymentStatus.md) |  | [optional] 
**paymentTermsText** | **String** |  | [optional] 
**precedingSalesVoucherId** | **String** | References the preceding sales voucher entity. | [optional] 
**precedingSalesVoucherType** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] 
**receiptConfirmationAvailable** | **Bool** |  | [optional] 
**relatedInvoiceId** | **UUID** | References the invoice entity. | [optional] 
**relationshipType** | **String** |  | [optional] 
**senderSnapshot** | **AnyCodable** |  | [optional] 
**sentAt** | **Date** |  | [optional] 
**servicePeriodEnd** | **Date** |  | [optional] 
**servicePeriodStart** | **Date** |  | [optional] 
**status** | [**InvoiceStatus**](InvoiceStatus.md) |  | 
**subtotal** | **String** |  | 
**supplierId** | **String** | References the supplier entity. | [optional] 
**taxExemptionReason** | **String** |  | [optional] 
**totalAmount** | **String** |  | 
**totalTax** | **String** |  | 
**vatCountry** | [**CountryCode**](CountryCode.md) |  | [optional] 
**vatSpecialCase** | **String** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


