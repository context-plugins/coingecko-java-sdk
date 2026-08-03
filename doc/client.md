
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](../doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| loggingConfig | [`Consumer<ApiLoggingConfiguration.Builder>`](../doc/api-logging-configuration-builder.md) | Set up Logging Configuration instance. |
| headerAuthCredentials | [`HeaderAuthCredentials`](auth/custom-header-signature.md) | The Credentials Setter for Custom Header Signature |
| queryAuthCredentials | [`QueryAuthCredentials`](auth/custom-query-parameter.md) | The Credentials Setter for Custom Query Parameter |

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

## CoinGecko Demo APIClient Class

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

### Apis

| Name | Description | Return Type |
|  --- | --- | --- |
| `getApi()` | Provides access to Client controller. | `Api` |

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `shutdown()` | Shutdown the underlying HttpClient instance. | `void` |
| `getEnvironment()` | Current API environment. | `Environment` |
| `getHttpClient()` | The HTTP Client instance to use for making HTTP requests. | `HttpClient` |
| `getHttpClientConfig()` | Http Client Configuration instance. | [`ReadonlyHttpClientConfiguration`](../doc/http-client-configuration.md) |
| `getLoggingConfig()` | Logging Configuration instance. | [`ReadonlyLoggingConfiguration`](../doc/api-logging-configuration.md) |
| `getHeaderAuthCredentials()` | The credentials to use with HeaderAuth. | [`HeaderAuthCredentials`](auth/custom-header-signature.md) |
| `getQueryAuthCredentials()` | The credentials to use with QueryAuth. | [`QueryAuthCredentials`](auth/custom-query-parameter.md) |
| `getBaseUri(Server server)` | Get base URI by current environment | `String` |
| `getBaseUri()` | Get base URI by current environment | `String` |

