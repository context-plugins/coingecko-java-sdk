
# Government

*This model accepts additional fields of type Object.*

## Structure

`Government`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Government name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | Government ticker symbol | String getSymbol() | setSymbol(String symbol) |
| `Country` | `String` | Required | Country code | String getCountry() | setCountry(String country) |
| `TotalHoldings` | [`double`](../../doc/models/precision.md) | Required | Total crypto holdings | double getTotalHoldings() | setTotalHoldings(double totalHoldings) |
| `TotalEntryValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total entry value in USD | double getTotalEntryValueUsd() | setTotalEntryValueUsd(double totalEntryValueUsd) |
| `TotalCurrentValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total current value of crypto holdings in USD | double getTotalCurrentValueUsd() | setTotalCurrentValueUsd(double totalCurrentValueUsd) |
| `PercentageOfTotalSupply` | [`double`](../../doc/models/precision.md) | Required | Percentage of total crypto supply | double getPercentageOfTotalSupply() | setPercentageOfTotalSupply(double percentageOfTotalSupply) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Government;
import java.io.IOException;

Government government = new Government.Builder(
    "name0",
    "symbol2",
    "country4",
    72.4D,
    112.26D,
    10.76D,
    4D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

