# CatalogApi

All URIs are relative to *https://gb.ru/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCatalog**](CatalogApi.md#getCatalog) | **GET** /catalog | get catalog
[**updBook**](CatalogApi.md#updBook) | **POST** /book | update book


<a name="getCatalog"></a>
# **getCatalog**
> List&lt;Book&gt; getCatalog(author)

get catalog

Get list of products

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CatalogApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api_key
ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
api_key.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.setApiKeyPrefix("Token");

CatalogApi apiInstance = new CatalogApi();
String author = "author_example"; // String | Author for filter
try {
    List<Book> result = apiInstance.getCatalog(author);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CatalogApi#getCatalog");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **author** | **String**| Author for filter | [optional]

### Return type

[**List&lt;Book&gt;**](Book.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="updBook"></a>
# **updBook**
> List&lt;Book&gt; updBook(book)

update book

Update exist book or create new

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CatalogApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api_key
ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
api_key.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.setApiKeyPrefix("Token");

CatalogApi apiInstance = new CatalogApi();
Book book = new Book(); // Book | New book
try {
    List<Book> result = apiInstance.updBook(book);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CatalogApi#updBook");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **book** | [**Book**](Book.md)| New book |

### Return type

[**List&lt;Book&gt;**](Book.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

