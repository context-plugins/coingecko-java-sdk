
# Trending Search

*This model accepts additional fields of type Object.*

## Structure

`TrendingSearch`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Coins` | [`List<Coin1>`](../../doc/models/coin-1.md) | Required | - | List<Coin1> getCoins() | setCoins(List<Coin1> coins) |
| `Nfts` | [`List<Nft1>`](../../doc/models/nft-1.md) | Required | - | List<Nft1> getNfts() | setNfts(List<Nft1> nfts) |
| `Categories` | [`List<Category2>`](../../doc/models/category-2.md) | Required | - | List<Category2> getCategories() | setCategories(List<Category2> categories) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Category2;
import com.coingecko.api.models.Coin1;
import com.coingecko.api.models.Content;
import com.coingecko.api.models.Data2;
import com.coingecko.api.models.Data3;
import com.coingecko.api.models.Data4;
import com.coingecko.api.models.Item;
import com.coingecko.api.models.Nft1;
import com.coingecko.api.models.TrendingSearch;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

TrendingSearch trendingSearch = new TrendingSearch.Builder(
    Arrays.asList(
        new Coin1.Builder(
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
        .build()
    ),
    Arrays.asList(
        new Nft1.Builder(
            "id2",
            "name2",
            "symbol6",
            "thumb0",
            84,
            "native_currency_symbol4",
            61.32D,
            88.84D,
            new Data3.Builder(
                "floor_price8",
                "floor_price_in_usd_24h_percentage_change0",
                "h24_volume8",
                "h24_average_sale_price8",
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
    ),
    Arrays.asList(
        new Category2.Builder(
            16,
            "name8",
            Arrays.asList(
                "top_3_coins_images0",
                "top_3_coins_images1"
            ),
            72.34D,
            "slug2",
            "coins_count0",
            new Data4.Builder(
                184.2D,
                21.84D,
                14.42D,
                197.04D,
                new LinkedHashMap<String, Double>() {{
                    put("key0", 226.93D);
                    put("key1", 226.94D);
                    put("key2", 226.95D);
                }},
                "sparkline8"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

