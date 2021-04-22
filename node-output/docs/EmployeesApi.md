# IO.Swagger.Api.EmployeesApi

All URIs are relative to *https://virtserver.swaggerhub.com/arnoldchanliongco/Sample_API/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ApiEmployeesGet**](EmployeesApi.md#apiemployeesget) | **GET** /api/Employees | Gets the list of all Employees.
[**ApiEmployeesIdDelete**](EmployeesApi.md#apiemployeesiddelete) | **DELETE** /api/Employees/{id} | Deletes employee record from database.
[**ApiEmployeesIdGet**](EmployeesApi.md#apiemployeesidget) | **GET** /api/Employees/{id} | Gets employees by id.
[**ApiEmployeesIdPut**](EmployeesApi.md#apiemployeesidput) | **PUT** /api/Employees/{id} | Edits employee record based on id.
[**ApiEmployeesPost**](EmployeesApi.md#apiemployeespost) | **POST** /api/Employees | Creates an Employee.

<a name="apiemployeesget"></a>
# **ApiEmployeesGet**
> List<Employee> ApiEmployeesGet ()

Gets the list of all Employees.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ApiEmployeesGetExample
    {
        public void main()
        {
            var apiInstance = new EmployeesApi();

            try
            {
                // Gets the list of all Employees.
                List&lt;Employee&gt; result = apiInstance.ApiEmployeesGet();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling EmployeesApi.ApiEmployeesGet: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List<Employee>**](Employee.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="apiemployeesiddelete"></a>
# **ApiEmployeesIdDelete**
> void ApiEmployeesIdDelete (int? id)

Deletes employee record from database.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ApiEmployeesIdDeleteExample
    {
        public void main()
        {
            var apiInstance = new EmployeesApi();
            var id = 56;  // int? | 

            try
            {
                // Deletes employee record from database.
                apiInstance.ApiEmployeesIdDelete(id);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling EmployeesApi.ApiEmployeesIdDelete: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int?**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="apiemployeesidget"></a>
# **ApiEmployeesIdGet**
> Employee ApiEmployeesIdGet (int? id)

Gets employees by id.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ApiEmployeesIdGetExample
    {
        public void main()
        {
            var apiInstance = new EmployeesApi();
            var id = 56;  // int? | 

            try
            {
                // Gets employees by id.
                Employee result = apiInstance.ApiEmployeesIdGet(id);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling EmployeesApi.ApiEmployeesIdGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int?**|  | 

### Return type

[**Employee**](Employee.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="apiemployeesidput"></a>
# **ApiEmployeesIdPut**
> void ApiEmployeesIdPut (int? id, Employee body = null)

Edits employee record based on id.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ApiEmployeesIdPutExample
    {
        public void main()
        {
            var apiInstance = new EmployeesApi();
            var id = 56;  // int? | 
            var body = new Employee(); // Employee |  (optional) 

            try
            {
                // Edits employee record based on id.
                apiInstance.ApiEmployeesIdPut(id, body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling EmployeesApi.ApiEmployeesIdPut: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int?**|  | 
 **body** | [**Employee**](Employee.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="apiemployeespost"></a>
# **ApiEmployeesPost**
> Employee ApiEmployeesPost (Employee body = null)

Creates an Employee.

Sample request:        POST api/Employee      {        \"id\" : \"1\"        \"firstName\": \"Arnold\",        \"lastName\": \"Chanliongco\",        \"emailId\": \"arnoldchanliongco@gmail.com\"              }

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ApiEmployeesPostExample
    {
        public void main()
        {
            var apiInstance = new EmployeesApi();
            var body = new Employee(); // Employee |  (optional) 

            try
            {
                // Creates an Employee.
                Employee result = apiInstance.ApiEmployeesPost(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling EmployeesApi.ApiEmployeesPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Employee**](Employee.md)|  | [optional] 

### Return type

[**Employee**](Employee.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
