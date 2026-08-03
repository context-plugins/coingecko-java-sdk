
# Derivatives Exchanges Id

*This model accepts additional fields of type Object.*

## Structure

`DerivativesExchangesId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Derivatives exchange name | String getName() | setName(String name) |
| `OpenInterestBtc` | [`Double`](../../doc/models/precision.md) | Required | Derivatives exchange open interest in BTC | Double getOpenInterestBtc() | setOpenInterestBtc(Double openInterestBtc) |
| `TradeVolume24HBtc` | `String` | Required | Derivatives exchange trade volume in BTC in 24 hours | String getTradeVolume24HBtc() | setTradeVolume24HBtc(String tradeVolume24HBtc) |
| `NumberOfPerpetualPairs` | `int` | Required | Number of perpetual pairs in the derivatives exchange | int getNumberOfPerpetualPairs() | setNumberOfPerpetualPairs(int numberOfPerpetualPairs) |
| `NumberOfFuturesPairs` | `int` | Required | Number of futures pairs in the derivatives exchange | int getNumberOfFuturesPairs() | setNumberOfFuturesPairs(int numberOfFuturesPairs) |
| `Image` | `String` | Required | Derivatives exchange image URL | String getImage() | setImage(String image) |
| `YearEstablished` | `Integer` | Required | Derivatives exchange established year | Integer getYearEstablished() | setYearEstablished(Integer yearEstablished) |
| `Country` | `String` | Required | Derivatives exchange incorporated country | String getCountry() | setCountry(String country) |
| `Description` | `String` | Required | Derivatives exchange description | String getDescription() | setDescription(String description) |
| `Url` | `String` | Required | Derivatives exchange website URL | String getUrl() | setUrl(String url) |
| `Tickers` | [`List<Ticker4>`](../../doc/models/ticker-4.md) | Optional | Derivative tickers data, available when include_tickers is specified | List<Ticker4> getTickers() | setTickers(List<Ticker4> tickers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ConvertedLast4;
import com.coingecko.api.models.ConvertedVolume4;
import com.coingecko.api.models.DerivativesExchangesId;
import com.coingecko.api.models.Ticker4;
import java.io.IOException;
import java.util.Arrays;

DerivativesExchangesId derivativesExchangesId = new DerivativesExchangesId.Builder(
    "name8",
    150.58D,
    "trade_volume_24h_btc8",
    136,
    100,
    "image8",
    8,
    "country2",
    "description2",
    "url2"
)
.tickers(Arrays.asList(
        new Ticker4.Builder(
            "symbol8",
            "base6",
            "target2",
            "coin_id6",
            "target_coin_id2",
            "trade_url6",
            "contract_type8",
            99.8D,
            205.66D,
            29.04D,
            99.64D,
            242.16D,
            72.18D,
            192.82D,
            111.68D,
            new ConvertedVolume4.Builder()
                .btc("btc0")
                .eth("eth8")
                .usd("usd8")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new ConvertedLast4.Builder()
                .btc("btc6")
                .eth("eth4")
                .usd("usd4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            151.68D,
            1.6D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Ticker4.Builder(
            "symbol8",
            "base6",
            "target2",
            "coin_id6",
            "target_coin_id2",
            "trade_url6",
            "contract_type8",
            99.8D,
            205.66D,
            29.04D,
            99.64D,
            242.16D,
            72.18D,
            192.82D,
            111.68D,
            new ConvertedVolume4.Builder()
                .btc("btc0")
                .eth("eth8")
                .usd("usd8")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new ConvertedLast4.Builder()
                .btc("btc6")
                .eth("eth4")
                .usd("usd4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            151.68D,
            1.6D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

