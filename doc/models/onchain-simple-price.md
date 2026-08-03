
# Onchain Simple Price

*This model accepts additional fields of type Object.*

## Structure

`OnchainSimplePrice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Data31`](../../doc/models/data-31.md) | Required | - | Data31 getData() | setData(Data31 data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes16;
import com.coingecko.api.models.Data31;
import com.coingecko.api.models.OnchainSimplePrice;
import java.io.IOException;
import java.util.LinkedHashMap;

OnchainSimplePrice onchainSimplePrice = new OnchainSimplePrice.Builder(
    new Data31.Builder(
        "id0",
        "type0",
        new Attributes16.Builder(
            new LinkedHashMap<String, String>() {{
                put("key0", "token_prices3");
                put("key1", "token_prices4");
                put("key2", "token_prices5");
            }}
        )
        .marketCapUsd(new LinkedHashMap<String, String>() {{
                put("key0", "market_cap_usd8");
                put("key1", "market_cap_usd9");
            }})
        .h24VolumeUsd(new LinkedHashMap<String, String>() {{
                put("key0", "h24_volume_usd3");
            }})
        .h24PriceChangePercentage(new LinkedHashMap<String, String>() {{
                put("key0", "h24_price_change_percentage4");
                put("key1", "h24_price_change_percentage3");
                put("key2", "h24_price_change_percentage2");
            }})
        .totalReserveInUsd(new LinkedHashMap<String, String>() {{
                put("key0", "total_reserve_in_usd4");
            }})
        .lastTradeTimestamp(new LinkedHashMap<String, String>() {{
                put("key0", "last_trade_timestamp4");
                put("key1", "last_trade_timestamp5");
            }})
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

