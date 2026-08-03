
# Getting Started with CoinGecko Demo API

## Building

Supported Java version is **8+**.

The generated code uses a few Maven dependencies e.g., Jackson, OkHttp,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on `File -> Import`.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=import0)

* In the import dialog, select `Existing Java Project` and click `Next`.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=import1)

* Browse to locate the folder containing the source code. Select the detected location of the project and click `Finish`.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=import2)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=import3)

* After successfully building the project, the client library needs to be installed as a Maven package in your local cache. Right-click on the project, select `Show in Local Terminal -> Terminal` or use `Ctrl + Alt + T` to open Terminal.

![Importing SDK into Eclipse - Step 5](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=openTerminal)

* In the terminal dialog, run the following command to install client library.

```
mvn install -Dmaven.test.skip=true -Dmaven.javadoc.skip=true
```

![Importing SDK into Eclipse - Step 6](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=installCommand)

## Installation

The following section explains how to use the CoinGeckoDemoApiLib library in a new project.

### 1. Starting a new project

For starting a new project, click the menu command `File > New > Project`.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=createNewProject0)

Next, choose `Maven > Maven Project` and click `Next`.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=createNewProject1)

Here, make sure to use the current workspace by choosing `Use default Workspace location`, as shown in the picture below and click `Next`.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=createNewProject2)

Following this, select the *quick start* project type to create a simple project with an existing class and a `main` method. To do this, choose `maven-archetype-quickstart` item from the list and click `Next`.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=createNewProject3)

In the last step, provide a `Group Id` and `Artifact Id` as shown in the picture below and click `Finish`.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=createNewProject4)

### 2. Add reference of the library project

The created Maven project manages its dependencies using its `pom.xml` file. In order to add a dependency on the *CoinGeckoDemoApiLib* client library, double click on the `pom.xml` file in the `Package Explorer`. Opening the `pom.xml` file will render a graphical view on the canvas. Here, switch to the `Dependencies` tab and click the `Add` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=testProject0)

Clicking the `Add` button will open a dialog where you need to specify CoinGeckoDemoApiLib in `Group Id`, coin-gecko-demo-api-lib in `Artifact Id` and 3.0.0 in the `Version` fields. Once added click `OK`. Save the `pom.xml` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=testProject1)

![Adding sample code](https://apidocs.io/illustration/java?workspaceFolder=CoinGecko%20Demo%20API-Java&workspaceName=CoinGeckoDemoApi&projectName=CoinGeckoDemoApiLib&rootNamespace=com.coingecko.api&groupId=CoinGeckoDemoApiLib&artifactId=coin-gecko-demo-api-lib&version=3.0.0&step=testProject2)

### 3. Write sample code

Once the `SimpleConsoleApp` is created, a file named `App.java` will be visible in the *Package Explorer* with a `main` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| loggingConfig | [`Consumer<ApiLoggingConfiguration.Builder>`](doc/api-logging-configuration-builder.md) | Set up Logging Configuration instance. |
| headerAuthCredentials | [`HeaderAuthCredentials`](doc/auth/custom-header-signature.md) | The Credentials Setter for Custom Header Signature |
| queryAuthCredentials | [`QueryAuthCredentials`](doc/auth/custom-query-parameter.md) | The Credentials Setter for Custom Query Parameter |

The API client can be initialized as follows:

```java
import com.coingecko.api.CoinGeckoDemoApiClient;
import com.coingecko.api.authentication.HeaderAuthModel;
import com.coingecko.api.authentication.QueryAuthModel;
import com.coingecko.api.exceptions.ApiException;
import com.coingecko.api.http.response.ApiResponse;
import org.slf4j.event.Level;

public class Program {
    public static void main(String[] args) {
        CoinGeckoDemoApiClient client = new CoinGeckoDemoApiClient.Builder()
            .loggingConfig(builder -> builder
                    .level(Level.DEBUG)
                    .requestConfig(logConfigBuilder -> logConfigBuilder.body(true))
                    .responseConfig(logConfigBuilder -> logConfigBuilder.headers(true)))
            .httpClientConfig(configBuilder -> configBuilder
                    .timeout(0))
            .headerAuthCredentials(new HeaderAuthModel.Builder(
                    "x-cg-demo-api-key"
                )
                .build())
            .queryAuthCredentials(new QueryAuthModel.Builder(
                    "x_cg_demo_api_key"
                )
                .build())
            .build();

    }
}
```

## Authorization

This API uses the following authentication schemes.

* [`headerAuth (Custom Header Signature)`](doc/auth/custom-header-signature.md)
* [`queryAuth (Custom Query Parameter)`](doc/auth/custom-query-parameter.md)

## List of APIs

* [API](doc/controllers/api.md)

## SDK Infrastructure

### Configuration

* [ApiLoggingConfiguration](doc/api-logging-configuration.md)
* [ApiLoggingConfiguration.Builder](doc/api-logging-configuration-builder.md)
* [ApiRequestLoggingConfiguration.Builder](doc/api-request-logging-configuration-builder.md)
* [ApiResponseLoggingConfiguration.Builder](doc/api-response-logging-configuration-builder.md)
* [Configuration Interface](doc/configuration-interface.md)
* [HttpClientConfiguration](doc/http-client-configuration.md)
* [HttpClientConfiguration.Builder](doc/http-client-configuration-builder.md)
* [HttpProxyConfiguration](doc/http-proxy-configuration.md)
* [HttpProxyConfiguration.Builder](doc/http-proxy-configuration-builder.md)

### HTTP

* [Headers](doc/headers.md)
* [HttpCallback Interface](doc/http-callback-interface.md)
* [HttpContext](doc/http-context.md)
* [HttpBodyRequest](doc/http-body-request.md)
* [HttpRequest](doc/http-request.md)
* [HttpResponse](doc/http-response.md)
* [HttpStringResponse](doc/http-string-response.md)

### Utilities

* [ApiException](doc/api-exception.md)
* [ApiResponse](doc/api-response.md)
* [ApiHelper](doc/api-helper.md)
* [FileWrapper](doc/file-wrapper.md)
* [DateTimeHelper](doc/date-time-helper.md)

