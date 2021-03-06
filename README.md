# swagger-java-client

Customer API
- API version: 1.0.0
  - Build date: 2021-03-27T15:01:41.112Z

This is a customer API, it provides REST API for customer

  For more information, please visit [http://www.pluralsight.com](http://www.pluralsight.com)

*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>io.swagger</groupId>
  <artifactId>swagger-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-java-client:1.0.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/swagger-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import io.swagger.client.*;
import io.swagger.client.auth.*;
import io.swagger.client.model.*;
import io.swagger.client.api.DefaultApi;

import java.io.File;
import java.util.*;

public class DefaultApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        
        // Configure HTTP basic authorization: BasicAuth
        HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
        BasicAuth.setUsername("YOUR USERNAME");
        BasicAuth.setPassword("YOUR PASSWORD");

        DefaultApi apiInstance = new DefaultApi();
        Customer body = new Customer(); // Customer | the new customer data in JSON format
        try {
            Integer result = apiInstance.customerPost(body);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DefaultApi#customerPost");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *http://api.globalmantics.com/crm/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**customerPost**](docs/DefaultApi.md#customerPost) | **POST** /customer | This is to create a request for customer&#39;s data
*DefaultApi* | [**deleteCustomer**](docs/DefaultApi.md#deleteCustomer) | **DELETE** /customer/{customerId} | delete a scpeific customer with the ID.
*DefaultApi* | [**getCustomer**](docs/DefaultApi.md#getCustomer) | **GET** /customer | This is to read customer&#39;s data
*DefaultApi* | [**updateCustomer**](docs/DefaultApi.md#updateCustomer) | **PUT** /customer/{customerId} | update existing customer


## Documentation for Models

 - [Customer](docs/Customer.md)
 - [CustomerAdress](docs/CustomerAdress.md)
 - [CustomerContacts](docs/CustomerContacts.md)


## Documentation for Authorization

Authentication schemes defined for the API:
### BasicAuth

- **Type**: HTTP basic authentication


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

rajdeepmukh@gmail.com

