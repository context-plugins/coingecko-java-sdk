
# Token

*This model accepts additional fields of type Object.*

## Structure

`Token`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ChainId` | [`double`](../../doc/models/precision.md) | Required | Chainlist's chain ID | double getChainId() | setChainId(double chainId) |
| `Address` | `String` | Required | Token contract address | String getAddress() | setAddress(String address) |
| `Name` | `String` | Required | Token name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | Token symbol | String getSymbol() | setSymbol(String symbol) |
| `Decimals` | [`double`](../../doc/models/precision.md) | Required | Token decimals | double getDecimals() | setDecimals(double decimals) |
| `LogoUri` | `String` | Required | Token image URL | String getLogoUri() | setLogoUri(String logoUri) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Token;
import java.io.IOException;

Token token = new Token.Builder(
    158.7D,
    "address2",
    "name6",
    "symbol8",
    50.7D,
    "logoURI4"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

