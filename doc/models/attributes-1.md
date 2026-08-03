
# Attributes 1

*This model accepts additional fields of type Object.*

## Structure

`Attributes1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | `String` | Optional | - | String getAddress() | setAddress(String address) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Symbol` | `String` | Optional | - | String getSymbol() | setSymbol(String symbol) |
| `Decimals` | `Integer` | Optional | - | Integer getDecimals() | setDecimals(Integer decimals) |
| `ImageUrl` | `String` | Optional | - | String getImageUrl() | setImageUrl(String imageUrl) |
| `CoingeckoCoinId` | `String` | Optional | - | String getCoingeckoCoinId() | setCoingeckoCoinId(String coingeckoCoinId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes1;
import java.io.IOException;

Attributes1 attributes1 = new Attributes1.Builder()
    .address("address4")
    .name("name8")
    .symbol("symbol0")
    .decimals(124)
    .imageUrl("image_url4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

