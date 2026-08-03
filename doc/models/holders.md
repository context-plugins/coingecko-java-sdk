
# Holders

Token holder information

*This model accepts additional fields of type Object.*

## Structure

`Holders`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Count` | `Integer` | Optional | Number of holders | Integer getCount() | setCount(Integer count) |
| `DistributionPercentage` | `Map<String, String>` | Optional | Holder distribution percentage (keys vary by chain, e.g. top_10, 11_30, 31_50, rest) | Map<String, String> getDistributionPercentage() | setDistributionPercentage(Map<String, String> distributionPercentage) |
| `LastUpdated` | `String` | Optional | Last updated timestamp | String getLastUpdated() | setLastUpdated(String lastUpdated) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Holders;
import java.io.IOException;
import java.util.LinkedHashMap;

Holders holders = new Holders.Builder()
    .count(46)
    .distributionPercentage(new LinkedHashMap<String, String>() {{
        put("key0", "distribution_percentage0");
        put("key1", "distribution_percentage1");
    }})
    .lastUpdated("last_updated8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

