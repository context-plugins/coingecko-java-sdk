
# Coin 1

*This model accepts additional fields of type Object.*

## Structure

`Coin1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Item` | [`Item`](../../doc/models/item.md) | Required | - | Item getItem() | setItem(Item item) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Coin1;
import com.coingecko.api.models.Content;
import com.coingecko.api.models.Data2;
import com.coingecko.api.models.Item;
import java.io.IOException;
import java.util.LinkedHashMap;

Coin1 coin1 = new Coin1.Builder(
    new Item.Builder(
        "id2",
        118,
        "name2",
        "symbol4",
        162,
        "thumb0",
        "small6",
        "large4",
        "slug6",
        212.04D,
        28,
        new Data2.Builder(
            148.58D,
            "price_btc2",
            new LinkedHashMap<String, Double>() {{
                put("key0", 92.11D);
                put("key1", 92.12D);
                put("key2", 92.13D);
            }},
            "market_cap0",
            "market_cap_btc4",
            "total_volume2",
            "total_volume_btc4",
            "sparkline8",
            new Content.Builder()
                .title("title0")
                .description("description6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

