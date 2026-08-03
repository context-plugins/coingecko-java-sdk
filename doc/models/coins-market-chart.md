
# Coins Market Chart

*This model accepts additional fields of type Object.*

## Structure

`CoinsMarketChart`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Prices` | [`List<List<Double>>`](../../doc/models/precision.md) | Required | Price data points as [timestamp, price] pairs | List<List<Double>> getPrices() | setPrices(List<List<Double>> prices) |
| `MarketCaps` | [`List<List<Double>>`](../../doc/models/precision.md) | Required | Market cap data points as [timestamp, market_cap] pairs | List<List<Double>> getMarketCaps() | setMarketCaps(List<List<Double>> marketCaps) |
| `TotalVolumes` | [`List<List<Double>>`](../../doc/models/precision.md) | Required | Total volume data points as [timestamp, volume] pairs | List<List<Double>> getTotalVolumes() | setTotalVolumes(List<List<Double>> totalVolumes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CoinsMarketChart;
import java.io.IOException;
import java.util.Arrays;

CoinsMarketChart coinsMarketChart = new CoinsMarketChart.Builder(
    Arrays.asList(
        Arrays.asList(
            158.33D,
            158.34D,
            158.35D
        ),
        Arrays.asList(
            158.33D,
            158.34D,
            158.35D
        ),
        Arrays.asList(
            158.33D,
            158.34D,
            158.35D
        )
    ),
    Arrays.asList(
        Arrays.asList(
            178.35D
        )
    ),
    Arrays.asList(
        Arrays.asList(
            113.24D,
            113.25D,
            113.26D
        ),
        Arrays.asList(
            113.24D,
            113.25D,
            113.26D
        ),
        Arrays.asList(
            113.24D,
            113.25D,
            113.26D
        )
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

