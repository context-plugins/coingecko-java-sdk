
# Government Treasury

*This model accepts additional fields of type Object.*

## Structure

`GovernmentTreasury`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TotalHoldings` | [`double`](../../doc/models/precision.md) | Required | Total crypto holdings | double getTotalHoldings() | setTotalHoldings(double totalHoldings) |
| `TotalValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total crypto holdings value in USD | double getTotalValueUsd() | setTotalValueUsd(double totalValueUsd) |
| `MarketCapDominance` | [`double`](../../doc/models/precision.md) | Required | Market cap dominance percentage | double getMarketCapDominance() | setMarketCapDominance(double marketCapDominance) |
| `Governments` | [`List<Government>`](../../doc/models/government.md) | Required | List of governments holding crypto | List<Government> getGovernments() | setGovernments(List<Government> governments) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Government;
import com.coingecko.api.models.GovernmentTreasury;
import java.io.IOException;
import java.util.Arrays;

GovernmentTreasury governmentTreasury = new GovernmentTreasury.Builder(
    25.46D,
    182.1D,
    103.78D,
    Arrays.asList(
        new Government.Builder(
            "name4",
            "symbol4",
            "country8",
            170.96D,
            124.9D,
            254.12D,
            16.64D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

