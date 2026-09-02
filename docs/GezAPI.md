# GezAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gezApi**](GezAPI.md#gezapi) | **GET** /api/v1/bookkeeping/gez | 


# **gezApi**
```swift
    open class func gezApi(jahr: Int? = nil, betriebsstaetten: String? = nil, kfz: Int64? = nil, hotelzimmer: Int64? = nil, beschaefigte: Int64? = nil, completion: @escaping (_ data: GezReport?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let jahr = 987 // Int |  (optional)
let betriebsstaetten = "betriebsstaetten_example" // String | Liste der Betriebsstätten als JSON, z.B. `[{\"name\":\"Filiale 1\",\"beschaefigte\":12}]`. (optional)
let kfz = 987 // Int64 | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). (optional)
let hotelzimmer = 987 // Int64 | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. (optional)
let beschaefigte = 987 // Int64 | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen). (optional)

GezAPI.gezApi(jahr: jahr, betriebsstaetten: betriebsstaetten, kfz: kfz, hotelzimmer: hotelzimmer, beschaefigte: beschaefigte) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jahr** | **Int** |  | [optional] 
 **betriebsstaetten** | **String** | Liste der Betriebsstätten als JSON, z.B. &#x60;[{\&quot;name\&quot;:\&quot;Filiale 1\&quot;,\&quot;beschaefigte\&quot;:12}]&#x60;. | [optional] 
 **kfz** | **Int64** | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional] 
 **hotelzimmer** | **Int64** | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional] 
 **beschaefigte** | **Int64** | Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional] 

### Return type

[**GezReport**](GezReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

