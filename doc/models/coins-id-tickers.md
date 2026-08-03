
# Coins Id Tickers

*This model accepts additional fields of type Object.*

## Structure

`CoinsIdTickers`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `Tickers` | [`List<Ticker>`](../../doc/models/ticker.md) | Required | List of tickers | List<Ticker> getTickers() | setTickers(List<Ticker> tickers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CoinsIdTickers;
import com.coingecko.api.models.ConvertedLast;
import com.coingecko.api.models.ConvertedVolume;
import com.coingecko.api.models.Market;
import com.coingecko.api.models.Ticker;
import java.io.IOException;
import java.util.Arrays;

CoinsIdTickers coinsIdTickers = new CoinsIdTickers.Builder(
    "name6",
    Arrays.asList(
        new Ticker.Builder(
            "base6",
            "target2",
            new Market.Builder()
                .name("name0")
                .identifier("identifier2")
                .hasTradingIncentive(false)
                .logo("logo6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            99.8D,
            36.06D,
            new ConvertedLast.Builder()
                .btc(30.96D)
                .eth(71.74D)
                .usd(5.04D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new ConvertedVolume.Builder()
                .btc(54.2D)
                .eth(94.98D)
                .usd(28.28D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            "trust_score0",
            137.08D,
            "timestamp8",
            "last_traded_at8",
            "last_fetch_at0",
            false,
            false,
            "trade_url6",
            "token_info_url2",
            "coin_id6",
            "target_coin_id2",
            3.12D
        )
        .costToMoveUpUsd(135D)
        .costToMoveDownUsd(186.48D)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

