
# Attributes 18

*This model accepts additional fields of type Object.*

## Structure

`Attributes18`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Network name | String getName() | setName(String name) |
| `CoingeckoAssetPlatformId` | `String` | Required | Corresponding CoinGecko asset platform ID | String getCoingeckoAssetPlatformId() | setCoingeckoAssetPlatformId(String coingeckoAssetPlatformId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes18;
import java.io.IOException;

Attributes18 attributes18 = new Attributes18.Builder(
    "name2",
    "coingecko_asset_platform_id0"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

