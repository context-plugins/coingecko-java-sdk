
# Global De Fi

*This model accepts additional fields of type Object.*

## Structure

`GlobalDeFi`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Data1`](../../doc/models/data-1.md) | Required | - | Data1 getData() | setData(Data1 data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data1;
import com.coingecko.api.models.GlobalDeFi;
import java.io.IOException;

GlobalDeFi globalDeFi = new GlobalDeFi.Builder(
    new Data1.Builder(
        "defi_market_cap0",
        "eth_market_cap4",
        "defi_to_eth_ratio4",
        "trading_volume_24h4",
        "defi_dominance2",
        "top_coin_name6",
        222.16D
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

