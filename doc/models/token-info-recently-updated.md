
# Token Info Recently Updated

*This model accepts additional fields of type Object.*

## Structure

`TokenInfoRecentlyUpdated`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Data10>`](../../doc/models/data-10.md) | Required | - | List<Data10> getData() | setData(List<Data10> data) |
| `Included` | [`List<Included2>`](../../doc/models/included-2.md) | Optional | Included network data, present when include=network is specified | List<Included2> getIncluded() | setIncluded(List<Included2> included) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes5;
import com.coingecko.api.models.Attributes6;
import com.coingecko.api.models.Data10;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Included2;
import com.coingecko.api.models.Network;
import com.coingecko.api.models.Relationships1;
import com.coingecko.api.models.TokenInfoRecentlyUpdated;
import java.io.IOException;
import java.util.Arrays;

TokenInfoRecentlyUpdated tokenInfoRecentlyUpdated = new TokenInfoRecentlyUpdated.Builder(
    Arrays.asList(
        new Data10.Builder(
            "id0",
            "type0",
            new Attributes5.Builder(
                "address0",
                "name4",
                "symbol6",
                220,
                "image_url0",
                "coingecko_coin_id4",
                Arrays.asList(
                    "websites5",
                    "websites6"
                ),
                "discord_url8",
                "farcaster_url6",
                "zora_url4",
                "telegram_handle2",
                "twitter_handle8",
                "description4",
                173.1D,
                "metadata_updated_at8"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Relationships1.Builder()
                .network(new Network.Builder()
                    .data(new Data5.Builder()
                        .id("id0")
                        .type("type0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.included(Arrays.asList(
        new Included2.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes6.Builder()
                .name("name4")
                .coingeckoAssetPlatformId("coingecko_asset_platform_id2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Included2.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes6.Builder()
                .name("name4")
                .coingeckoAssetPlatformId("coingecko_asset_platform_id2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Included2.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes6.Builder()
                .name("name4")
                .coingeckoAssetPlatformId("coingecko_asset_platform_id2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

