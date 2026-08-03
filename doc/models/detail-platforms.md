
# Detail Platforms

*This model accepts additional fields of type Object.*

## Structure

`DetailPlatforms`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DecimalPlace` | `Integer` | Optional | Token decimal place | Integer getDecimalPlace() | setDecimalPlace(Integer decimalPlace) |
| `ContractAddress` | `String` | Optional | Token contract address | String getContractAddress() | setContractAddress(String contractAddress) |
| `GeckoterminalUrl` | `String` | Optional | GeckoTerminal URL | String getGeckoterminalUrl() | setGeckoterminalUrl(String geckoterminalUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.DetailPlatforms;
import java.io.IOException;

DetailPlatforms detailPlatforms = new DetailPlatforms.Builder()
    .decimalPlace(40)
    .contractAddress("contract_address8")
    .geckoterminalUrl("geckoterminal_url6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

