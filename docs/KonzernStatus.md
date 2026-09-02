# KonzernStatus

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**groessenbefreit** | **Bool** |  | 
**kapitalmarktorientiert** | **Bool** |  | 
**konzernabschlusspflicht** | **Bool** |  | 
**missingGroupFigures** | **Bool** | Keine group_figures-Zeile für das Jahr vorhanden → keine Größenbefreiung. | 
**mutterunternehmen** | **Bool** | Mutterunternehmen: mindestens eine beherrschte Beteiligung (§ 290 Abs. 1 HGB). | 
**parentName** | **String** | Mutterunternehmen für die Zwischenholding-Befreiung (§ 291 HGB). | [optional] 
**parentSitus** | **String** |  | [optional] 
**participations** | [KonzernBeteiligung] |  | 
**thresholds** | [**KonzernThresholds**](KonzernThresholds.md) |  | 
**year** | **Int** |  | 
**zwischenholdingBefreit** | **Bool** |  | 
**zwischenholdingHinweis** | **String** | Hinweis zu den § 291-Voraussetzungen (EU/EWR-Sitz, geprüfter Konzernabschluss). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


