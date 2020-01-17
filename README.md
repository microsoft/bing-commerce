
# Overview

This repostitory contains the swagger and open api specifications for the [Bing for Commerce Platforms](http://commerce.bing.com), including the search and ingestion services. This can help you write your application and services to target the Bing for Commerce Services.

For more details about the proejct, please refer to the [Bing for Commerce API Documentation](https://commerce.bing.com/docs/product-search/).

# Generating The Libraries
 Although you can totally use the swagger specs as a guide to manually call our services, it would be a lot easier if you tried using a tool like [AutoRest](https://github.com/Azure/AutoRest) or [Swagger Codegen](https://swagger.io/tools/swagger-codegen/) to generate a library that you can use with the language of your choice. To take some burden off your shoulders, and to make it easier to write your applications, we have already genrated the libraries for:
* [dotnet](https://github.com/microsoft/bing-ecommerce-sdk-for-net).
* [Java](https://github.com/microsoft/bing-ecommerce-sdk-for-java).
* [Python](https://github.com/microsoft/bing-ecommerce-sdk-for-python).

# Authentication
Bing for Commerce APIs use Bearer Tokens for authentication. You can use the [Bing for Commerce Portal Documentation](https://commerce.bing.com/docs/Portal%20Documentation/#manage-keys-and-tokens) for help creating one.

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
