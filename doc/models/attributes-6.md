
# Attributes 6

*This model accepts additional fields of type Object.*

## Structure

`Attributes6`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `CoingeckoAssetPlatformId` | `String` | Optional | - | String getCoingeckoAssetPlatformId() | setCoingeckoAssetPlatformId(String coingeckoAssetPlatformId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes6;
import java.io.IOException;

Attributes6 attributes6 = new Attributes6.Builder()
    .name("name2")
    .coingeckoAssetPlatformId("coingecko_asset_platform_id0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

