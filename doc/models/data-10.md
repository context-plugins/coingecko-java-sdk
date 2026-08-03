
# Data 10

*This model accepts additional fields of type Object.*

## Structure

`Data10`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Token identifier | String getId() | setId(String id) |
| `Type` | `String` | Required | Resource type | String getType() | setType(String type) |
| `Attributes` | [`Attributes5`](../../doc/models/attributes-5.md) | Required | - | Attributes5 getAttributes() | setAttributes(Attributes5 attributes) |
| `Relationships` | [`Relationships1`](../../doc/models/relationships-1.md) | Required | - | Relationships1 getRelationships() | setRelationships(Relationships1 relationships) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes5;
import com.coingecko.api.models.Data10;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Network;
import com.coingecko.api.models.Relationships1;
import java.io.IOException;
import java.util.Arrays;

Data10 data10 = new Data10.Builder(
    "id6",
    "type6",
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
.build();
```

