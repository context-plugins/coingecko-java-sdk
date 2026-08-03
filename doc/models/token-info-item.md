
# Token Info Item

*This model accepts additional fields of type Object.*

## Structure

`TokenInfoItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Token identifier | String getId() | setId(String id) |
| `Type` | `String` | Required | Resource type | String getType() | setType(String type) |
| `Attributes` | [`Attributes7`](../../doc/models/attributes-7.md) | Required | - | Attributes7 getAttributes() | setAttributes(Attributes7 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes7;
import com.coingecko.api.models.GtScoreDetails;
import com.coingecko.api.models.Holders;
import com.coingecko.api.models.Image6;
import com.coingecko.api.models.TokenInfoItem;
import com.coingecko.api.models.containers.Attributes7IsHoneypot;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

TokenInfoItem tokenInfoItem = new TokenInfoItem.Builder(
    "id0",
    "type0",
    new Attributes7.Builder(
        "address0",
        "name4",
        "symbol6",
        220,
        "image_url0",
        new Image6.Builder()
            .thumb("thumb4")
            .small("small0")
            .large("large8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        "banner_image_url6",
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
        new GtScoreDetails.Builder()
            .pool(155.82D)
            .transaction(141.8D)
            .creation(88.54D)
            .info(69.28D)
            .holders(31.82D)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        false,
        Arrays.asList(
            "categories8",
            "categories7"
        ),
        Arrays.asList(
            "gt_category_ids6",
            "gt_category_ids7"
        ),
        new Holders.Builder()
            .count(46)
            .distributionPercentage(new LinkedHashMap<String, String>() {{
                put("key0", "distribution_percentage0");
                put("key1", "distribution_percentage1");
            }})
            .lastUpdated("last_updated8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        "mint_authority6",
        "freeze_authority2",
        Attributes7IsHoneypot.fromBoolean(
            true
        ),
        "developer_address0",
        "developer_holding_percentage2"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

