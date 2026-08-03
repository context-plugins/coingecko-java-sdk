
# Token Item

*This model accepts additional fields of type Object.*

## Structure

`TokenItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Token identifier | String getId() | setId(String id) |
| `Type` | `String` | Required | Resource type | String getType() | setType(String type) |
| `Attributes` | [`Attributes9`](../../doc/models/attributes-9.md) | Required | - | Attributes9 getAttributes() | setAttributes(Attributes9 attributes) |
| `Relationships` | [`Relationships3`](../../doc/models/relationships-3.md) | Required | - | Relationships3 getRelationships() | setRelationships(Relationships3 relationships) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes9;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.LaunchpadDetails;
import com.coingecko.api.models.Relationships3;
import com.coingecko.api.models.TokenItem;
import com.coingecko.api.models.TopPools;
import com.coingecko.api.models.VolumeUsd1;
import java.io.IOException;
import java.util.Arrays;

TokenItem tokenItem = new TokenItem.Builder(
    "id8",
    "type2",
    new Attributes9.Builder(
        "address0",
        "name4",
        "symbol6",
        220,
        "image_url0",
        "coingecko_coin_id4",
        "total_supply2",
        "normalized_total_supply4",
        "price_usd8",
        "fdv_usd8",
        "total_reserve_in_usd4",
        new VolumeUsd1.Builder()
            .h24("h242")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        "market_cap_usd0"
    )
    .lastTradeTimestamp("last_trade_timestamp4")
    .launchpadDetails(new LaunchpadDetails.Builder()
            .graduationPercentage(93.02D)
            .completed(false)
            .completedAt("completed_at4")
            .migratedDestinationPoolAddress("migrated_destination_pool_address8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new Relationships3.Builder()
        .topPools(new TopPools.Builder()
            .data(Arrays.asList(
                new Data5.Builder()
                    .id("id0")
                    .type("type0")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new Data5.Builder()
                    .id("id0")
                    .type("type0")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

