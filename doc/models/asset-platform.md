
# Asset Platform

*This model accepts additional fields of type Object.*

## Structure

`AssetPlatform`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Asset platform ID | String getId() | setId(String id) |
| `ChainIdentifier` | [`Double`](../../doc/models/precision.md) | Required | Chainlist's chain ID | Double getChainIdentifier() | setChainIdentifier(Double chainIdentifier) |
| `Name` | `String` | Required | Chain name | String getName() | setName(String name) |
| `Shortname` | `String` | Required | Chain shortname | String getShortname() | setShortname(String shortname) |
| `NativeCoinId` | `String` | Required | Chain native coin ID | String getNativeCoinId() | setNativeCoinId(String nativeCoinId) |
| `Image` | [`Image3`](../../doc/models/image-3.md) | Required | Asset platform image URLs | Image3 getImage() | setImage(Image3 image) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.AssetPlatform;
import com.coingecko.api.models.Image3;
import java.io.IOException;

AssetPlatform assetPlatform = new AssetPlatform.Builder(
    "id8",
    188D,
    "name8",
    "shortname8",
    "native_coin_id6",
    new Image3.Builder()
        .thumb("thumb4")
        .small("small0")
        .large("large8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

