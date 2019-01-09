# IO.Swagger.Api.DefaultApi

All URIs are relative to *https://FES production url*

Method | HTTP request | Description
------------- | ------------- | -------------
[**FesFdlePermitDownloadPost**](DefaultApi.md#fesfdlepermitdownloadpost) | **POST** /fes/fdle/permit/download | 
[**RootGet**](DefaultApi.md#rootget) | **GET** / | 

<a name="fesfdlepermitdownloadpost"></a>
# **FesFdlePermitDownloadPost**
> byte[] FesFdlePermitDownloadPost (string authorization, CwpRequest body)



This service allows authorized client to download permit results in .csv format for given decision date.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class FesFdlePermitDownloadPostExample
    {
        public void main()
        {

            var apiInstance = new DefaultApi();
            var authorization = authorization_example;  // string | The service expects valid user name and password supplied in the Request header for authorization purpose. 
            var body = new CwpRequest(); // CwpRequest | The service accepts
 decision date as JSON string in the request. <br>When submitting, <li>
 The decision date <b>must be in <i>MM/DD/YYYY</i></b>  format. <li>
 The decision date <b><i>cannot be current or future date</i></b>.
  (optional) 

            try
            {
                byte[] result = apiInstance.FesFdlePermitDownloadPost(authorization, body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.FesFdlePermitDownloadPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| The service expects valid user name and password supplied in the Request header for authorization purpose.  | 
 **body** | [**CwpRequest**](CwpRequest.md)| The service accepts
 decision date as JSON string in the request. &lt;br&gt;When submitting, &lt;li&gt;
 The decision date &lt;b&gt;must be in &lt;i&gt;MM/DD/YYYY&lt;/i&gt;&lt;/b&gt;  format. &lt;li&gt;
 The decision date &lt;b&gt;&lt;i&gt;cannot be current or future date&lt;/i&gt;&lt;/b&gt;.
  | [optional] 

### Return type

**byte[]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="rootget"></a>
# **RootGet**
> void RootGet ()



This method is not supported by this service.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class RootGetExample
    {
        public void main()
        {

            var apiInstance = new DefaultApi();

            try
            {
                apiInstance.RootGet();
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.RootGet: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

