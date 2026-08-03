
# Custom Header Signature



Documentation for accessing and setting credentials for headerAuth.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| x-cg-demo-api-key | `String` | Learn how to [set up your API key](https://docs.coingecko.com/docs/setting-up-your-api-key) | `xCgDemoApiKey` | `getXCgDemoApiKey()` |



**Note:** Auth credentials can be set using `headerAuthCredentials` in the client builder and accessed through `getHeaderAuthCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```java
import com.coingecko.api.CoinGeckoDemoApiClient;
import com.coingecko.api.authentication.HeaderAuthModel;

public class Program {
    public static void main(String[] args) {
        CoinGeckoDemoApiClient client = new CoinGeckoDemoApiClient.Builder()
            .headerAuthCredentials(new HeaderAuthModel.Builder(
                    "x-cg-demo-api-key"
                )
                .build())
            .build();
    }
}
```


