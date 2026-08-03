
# Company Treasury

*This model accepts additional fields of type Object.*

## Structure

`CompanyTreasury`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TotalHoldings` | [`double`](../../doc/models/precision.md) | Required | Total crypto holdings | double getTotalHoldings() | setTotalHoldings(double totalHoldings) |
| `TotalValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total crypto holdings value in USD | double getTotalValueUsd() | setTotalValueUsd(double totalValueUsd) |
| `MarketCapDominance` | [`double`](../../doc/models/precision.md) | Required | Market cap dominance percentage | double getMarketCapDominance() | setMarketCapDominance(double marketCapDominance) |
| `Companies` | [`List<Company>`](../../doc/models/company.md) | Required | List of companies holding crypto | List<Company> getCompanies() | setCompanies(List<Company> companies) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Company;
import com.coingecko.api.models.CompanyTreasury;
import java.io.IOException;
import java.util.Arrays;

CompanyTreasury companyTreasury = new CompanyTreasury.Builder(
    40.56D,
    139.92D,
    37.76D,
    Arrays.asList(
        new Company.Builder(
            "name2",
            "symbol4",
            "country6",
            92.32D,
            132.18D,
            9.16D,
            23.92D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

