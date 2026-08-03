
# Custom Query Parameter



Documentation for accessing and setting credentials for queryAuth.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| x_cg_demo_api_key | `String` | Learn how to [set up your API key](https://docs.coingecko.com/docs/setting-up-your-api-key) | `xCgDemoApiKey` | `getXCgDemoApiKey()` |



**Note:** Auth credentials can be set using `queryAuthCredentials` in the client builder and accessed through `getQueryAuthCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```java
import com.coingecko.api.CoinGeckoDemoApiClient;
import com.coingecko.api.authentication.QueryAuthModel;

public class Program {
    public static void main(String[] args) {
        CoinGeckoDemoApiClient client = new CoinGeckoDemoApiClient.Builder()
            .queryAuthCredentials(new QueryAuthModel.Builder(
                    "x_cg_demo_api_key"
                )
                .build())
            .build();
    }
}
```


