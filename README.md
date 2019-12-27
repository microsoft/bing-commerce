
# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.


# Overview

This repostitory contains the swagger and open api specifications for the [Bing ECommerce Platforms](), including the search and ingestion services. This can help you write your application and services to target the Bing ECommerce Services.

# Generating The Libraries
 Although you can totally use the swagger specs as a guide to manually call our services, it would be a lot easier if you tried using a tool like [AutoRest](https://github.com/Azure/AutoRest) or [Swagger Codegen](https://swagger.io/tools/swagger-codegen/) to generate a library that you can use with the language of your choice. To take some burden off your shoulders, and to make it easier to write your applications, we have already genrated the libraries for:
* [dotnet](https://github.com/microsoft/bing-ecommerce-sdk-for-net).
* [Java](https://github.com/microsoft/bing-ecommerce-sdk-for-java).
* [Python](https://github.com/microsoft/bing-ecommerce-sdk-for-python).

# Authentication
In order to inject the authentication in the language of your choice, you will need to use an interceptor to add the required authentication to the request before sending it to the service. You can look at the [dotnet sdk](https://github.com/microsoft/bing-ecommerce-sdk-for-net/tree/master/src/search/src/AppIdCredentials.cs), [java sdk](https://github.com/microsoft/bing-ecommerce-sdk-for-java/tree/master/src/search/src/main/java/com/microsoft/bing/ecommerce/search/util) for exapmles on how you can accomplish that using appid. The services currently support two methods of authentication:
### Query parameter
For any of the existing APIs, you can add a parameter `appid` containing your Bing API Developer AppId. Example would be:
<pre>
https://www.bingapis.com/api/v1/retail/search/&lt;&lt;MY TENANT ID&gt;&gt;/indexes/&lt;&lt;MY INDEX ID&gt;&gt;?q=tshirts<b>&appid=&lt;&lt;MY APP ID&gt;&gt;</b>
</pre>

### JSON Web Token
You can use the portal to create a token, which you can then use it as a bearer token when issuing a request to any of our apis.