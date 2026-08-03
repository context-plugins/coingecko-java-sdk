
# Nft

*This model accepts additional fields of type Object.*

## Structure

`Nft`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | NFT collection ID | String getId() | setId(String id) |
| `Name` | `String` | Required | NFT collection name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | NFT collection symbol | String getSymbol() | setSymbol(String symbol) |
| `Thumb` | `String` | Required | NFT collection thumb image URL | String getThumb() | setThumb(String thumb) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Nft;
import java.io.IOException;

Nft nft = new Nft.Builder(
    "id4",
    "name4",
    "symbol4",
    "thumb2"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

