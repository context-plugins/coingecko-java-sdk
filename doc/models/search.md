
# Search

*This model accepts additional fields of type Object.*

## Structure

`Search`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Coins` | [`List<Coin>`](../../doc/models/coin.md) | Required | - | List<Coin> getCoins() | setCoins(List<Coin> coins) |
| `Exchanges` | [`List<Exchange>`](../../doc/models/exchange.md) | Required | - | List<Exchange> getExchanges() | setExchanges(List<Exchange> exchanges) |
| `Icos` | `List<Object>` | Required | - | List<Object> getIcos() | setIcos(List<Object> icos) |
| `Categories` | [`List<Category>`](../../doc/models/category.md) | Required | - | List<Category> getCategories() | setCategories(List<Category> categories) |
| `Nfts` | [`List<Nft>`](../../doc/models/nft.md) | Required | - | List<Nft> getNfts() | setNfts(List<Nft> nfts) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Category;
import com.coingecko.api.models.Coin;
import com.coingecko.api.models.Exchange;
import com.coingecko.api.models.Nft;
import com.coingecko.api.models.Search;
import java.io.IOException;
import java.util.Arrays;

Search search = new Search.Builder(
    Arrays.asList(
        new Coin.Builder(
            "id0",
            "name0",
            "api_symbol8",
            "symbol2",
            74,
            "thumb8",
            "large2"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Arrays.asList(
        new Exchange.Builder(
            "id2",
            "name2",
            "market_type8",
            "thumb0",
            "large4"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Arrays.asList(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    ),
    Arrays.asList(
        new Category.Builder(
            "id8",
            "name8"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Arrays.asList(
        new Nft.Builder(
            "id2",
            "name2",
            "symbol6",
            "thumb0"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

