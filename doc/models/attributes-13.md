
# Attributes 13

*This model accepts additional fields of type Object.*

## Structure

`Attributes13`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | `String` | Optional | - | String getAddress() | setAddress(String address) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Symbol` | `String` | Optional | - | String getSymbol() | setSymbol(String symbol) |
| `Decimals` | `Integer` | Optional | - | Integer getDecimals() | setDecimals(Integer decimals) |
| `ImageUrl` | `String` | Optional | - | String getImageUrl() | setImageUrl(String imageUrl) |
| `CoingeckoCoinId` | `String` | Optional | - | String getCoingeckoCoinId() | setCoingeckoCoinId(String coingeckoCoinId) |
| `CoingeckoAssetPlatformId` | `String` | Optional | - | String getCoingeckoAssetPlatformId() | setCoingeckoAssetPlatformId(String coingeckoAssetPlatformId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes13;
import java.io.IOException;

Attributes13 attributes13 = new Attributes13.Builder()
    .address("address2")
    .name("name6")
    .symbol("symbol8")
    .decimals(94)
    .imageUrl("image_url2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

