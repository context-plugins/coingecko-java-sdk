
# Token Lists

*This model accepts additional fields of type Object.*

## Structure

`TokenLists`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Token list name | String getName() | setName(String name) |
| `LogoUri` | `String` | Required | Token list logo URL | String getLogoUri() | setLogoUri(String logoUri) |
| `Keywords` | `List<String>` | Required | Token list keywords | List<String> getKeywords() | setKeywords(List<String> keywords) |
| `Timestamp` | `LocalDateTime` | Required | Token list generation timestamp | LocalDateTime getTimestamp() | setTimestamp(LocalDateTime timestamp) |
| `Tokens` | [`List<Token>`](../../doc/models/token.md) | Required | List of tokens | List<Token> getTokens() | setTokens(List<Token> tokens) |
| `Version` | [`Version`](../../doc/models/version.md) | Required | Token list version | Version getVersion() | setVersion(Version version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.DateTimeHelper;
import com.coingecko.api.models.Token;
import com.coingecko.api.models.TokenLists;
import com.coingecko.api.models.Version;
import java.io.IOException;
import java.util.Arrays;

TokenLists tokenLists = new TokenLists.Builder(
    "name2",
    "logoURI0",
    Arrays.asList(
        "keywords9",
        "keywords8"
    ),
    DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
    Arrays.asList(
        new Token.Builder(
            120.68D,
            "address4",
            "name8",
            "symbol0",
            27.32D,
            "logoURI6"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    new Version.Builder()
        .major(131.98D)
        .minor(74.22D)
        .patch(252.26D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

