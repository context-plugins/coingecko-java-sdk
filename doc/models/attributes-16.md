
# Attributes 16

*This model accepts additional fields of type Object.*

## Structure

`Attributes16`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TokenPrices` | `Map<String, String>` | Required | Token prices keyed by contract address | Map<String, String> getTokenPrices() | setTokenPrices(Map<String, String> tokenPrices) |
| `MarketCapUsd` | `Map<String, String>` | Optional | Market cap in USD keyed by contract address | Map<String, String> getMarketCapUsd() | setMarketCapUsd(Map<String, String> marketCapUsd) |
| `H24VolumeUsd` | `Map<String, String>` | Optional | 24hr volume in USD keyed by contract address | Map<String, String> getH24VolumeUsd() | setH24VolumeUsd(Map<String, String> h24VolumeUsd) |
| `H24PriceChangePercentage` | `Map<String, String>` | Optional | 24hr price change percentage keyed by contract address | Map<String, String> getH24PriceChangePercentage() | setH24PriceChangePercentage(Map<String, String> h24PriceChangePercentage) |
| `TotalReserveInUsd` | `Map<String, String>` | Optional | Total reserve in USD keyed by contract address | Map<String, String> getTotalReserveInUsd() | setTotalReserveInUsd(Map<String, String> totalReserveInUsd) |
| `LastTradeTimestamp` | `Map<String, String>` | Optional | Last trade timestamp keyed by contract address | Map<String, String> getLastTradeTimestamp() | setLastTradeTimestamp(Map<String, String> lastTradeTimestamp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes16;
import java.io.IOException;
import java.util.LinkedHashMap;

Attributes16 attributes16 = new Attributes16.Builder(
    new LinkedHashMap<String, String>() {{
        put("key0", "token_prices1");
    }}
)
.marketCapUsd(new LinkedHashMap<String, String>() {{
        put("key0", "market_cap_usd2");
        put("key1", "market_cap_usd3");
        put("key2", "market_cap_usd4");
    }})
.h24VolumeUsd(new LinkedHashMap<String, String>() {{
        put("key0", "h24_volume_usd7");
        put("key1", "h24_volume_usd8");
    }})
.h24PriceChangePercentage(new LinkedHashMap<String, String>() {{
        put("key0", "h24_price_change_percentage8");
    }})
.totalReserveInUsd(new LinkedHashMap<String, String>() {{
        put("key0", "total_reserve_in_usd8");
        put("key1", "total_reserve_in_usd9");
    }})
.lastTradeTimestamp(new LinkedHashMap<String, String>() {{
        put("key0", "last_trade_timestamp8");
        put("key1", "last_trade_timestamp9");
        put("key2", "last_trade_timestamp0");
    }})
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

