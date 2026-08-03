
# Company

*This model accepts additional fields of type Object.*

## Structure

`Company`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Company name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | Company ticker symbol | String getSymbol() | setSymbol(String symbol) |
| `Country` | `String` | Required | Country code | String getCountry() | setCountry(String country) |
| `TotalHoldings` | [`double`](../../doc/models/precision.md) | Required | Total crypto holdings | double getTotalHoldings() | setTotalHoldings(double totalHoldings) |
| `TotalEntryValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total entry value in USD | double getTotalEntryValueUsd() | setTotalEntryValueUsd(double totalEntryValueUsd) |
| `TotalCurrentValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total current value of crypto holdings in USD | double getTotalCurrentValueUsd() | setTotalCurrentValueUsd(double totalCurrentValueUsd) |
| `PercentageOfTotalSupply` | [`double`](../../doc/models/precision.md) | Required | Percentage of total crypto supply | double getPercentageOfTotalSupply() | setPercentageOfTotalSupply(double percentageOfTotalSupply) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Company;
import java.io.IOException;

Company company = new Company.Builder(
    "name0",
    "symbol8",
    "country4",
    136.3D,
    159.56D,
    219.46D,
    51.3D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

