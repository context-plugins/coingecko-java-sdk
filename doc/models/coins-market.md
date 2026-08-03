
# Coins Market

*This model accepts additional fields of type Object.*

## Structure

`CoinsMarket`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Coin ID | String getId() | setId(String id) |
| `Symbol` | `String` | Required | Coin symbol | String getSymbol() | setSymbol(String symbol) |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `Image` | `String` | Required | Coin image URL | String getImage() | setImage(String image) |
| `CurrentPrice` | [`Double`](../../doc/models/precision.md) | Required | Current price in target currency | Double getCurrentPrice() | setCurrentPrice(Double currentPrice) |
| `MarketCap` | [`Double`](../../doc/models/precision.md) | Required | Market cap in target currency | Double getMarketCap() | setMarketCap(Double marketCap) |
| `MarketCapRank` | `Integer` | Required | Market cap rank | Integer getMarketCapRank() | setMarketCapRank(Integer marketCapRank) |
| `FullyDilutedValuation` | [`Double`](../../doc/models/precision.md) | Required | Fully diluted valuation in target currency | Double getFullyDilutedValuation() | setFullyDilutedValuation(Double fullyDilutedValuation) |
| `TotalVolume` | [`Double`](../../doc/models/precision.md) | Required | Total trading volume in target currency | Double getTotalVolume() | setTotalVolume(Double totalVolume) |
| `High24H` | [`Double`](../../doc/models/precision.md) | Required | 24-hour price high in target currency | Double getHigh24H() | setHigh24H(Double high24H) |
| `Low24H` | [`Double`](../../doc/models/precision.md) | Required | 24-hour price low in target currency | Double getLow24H() | setLow24H(Double low24H) |
| `PriceChange24H` | [`Double`](../../doc/models/precision.md) | Required | 24-hour price change in target currency | Double getPriceChange24H() | setPriceChange24H(Double priceChange24H) |
| `PriceChangePercentage24H` | [`Double`](../../doc/models/precision.md) | Required | 24-hour price change percentage | Double getPriceChangePercentage24H() | setPriceChangePercentage24H(Double priceChangePercentage24H) |
| `MarketCapChange24H` | [`Double`](../../doc/models/precision.md) | Required | 24-hour market cap change in target currency | Double getMarketCapChange24H() | setMarketCapChange24H(Double marketCapChange24H) |
| `MarketCapChangePercentage24H` | [`Double`](../../doc/models/precision.md) | Required | 24-hour market cap change percentage | Double getMarketCapChangePercentage24H() | setMarketCapChangePercentage24H(Double marketCapChangePercentage24H) |
| `CirculatingSupply` | [`Double`](../../doc/models/precision.md) | Required | Circulating supply | Double getCirculatingSupply() | setCirculatingSupply(Double circulatingSupply) |
| `TotalSupply` | [`Double`](../../doc/models/precision.md) | Required | Total supply | Double getTotalSupply() | setTotalSupply(Double totalSupply) |
| `MaxSupply` | [`Double`](../../doc/models/precision.md) | Required | Max supply | Double getMaxSupply() | setMaxSupply(Double maxSupply) |
| `Ath` | [`Double`](../../doc/models/precision.md) | Required | All-time high price in target currency | Double getAth() | setAth(Double ath) |
| `AthChangePercentage` | [`Double`](../../doc/models/precision.md) | Required | All-time high change percentage | Double getAthChangePercentage() | setAthChangePercentage(Double athChangePercentage) |
| `AthDate` | `LocalDateTime` | Required | All-time high date | LocalDateTime getAthDate() | setAthDate(LocalDateTime athDate) |
| `Atl` | [`Double`](../../doc/models/precision.md) | Required | All-time low price in target currency | Double getAtl() | setAtl(Double atl) |
| `AtlChangePercentage` | [`Double`](../../doc/models/precision.md) | Required | All-time low change percentage | Double getAtlChangePercentage() | setAtlChangePercentage(Double atlChangePercentage) |
| `AtlDate` | `LocalDateTime` | Required | All-time low date | LocalDateTime getAtlDate() | setAtlDate(LocalDateTime atlDate) |
| `Roi` | [`Roi2`](../../doc/models/roi-2.md) | Required | Return on investment data | Roi2 getRoi() | setRoi(Roi2 roi) |
| `LastUpdated` | `LocalDateTime` | Required | Last updated timestamp | LocalDateTime getLastUpdated() | setLastUpdated(LocalDateTime lastUpdated) |
| `MarketCapRankWithRehypothecated` | `Integer` | Optional | Market cap rank including rehypothecated tokens | Integer getMarketCapRankWithRehypothecated() | setMarketCapRankWithRehypothecated(Integer marketCapRankWithRehypothecated) |
| `SparklineIn7D` | [`SparklineIn7D`](../../doc/models/sparkline-in-7-d.md) | Optional | Sparkline price data for the last 7 days | SparklineIn7D getSparklineIn7D() | setSparklineIn7D(SparklineIn7D sparklineIn7D) |
| `PriceChangePercentage1HInCurrency` | [`Double`](../../doc/models/precision.md) | Optional | 1-hour price change percentage in target currency | Double getPriceChangePercentage1HInCurrency() | setPriceChangePercentage1HInCurrency(Double priceChangePercentage1HInCurrency) |
| `PriceChangePercentage24HInCurrency` | [`Double`](../../doc/models/precision.md) | Optional | 24-hour price change percentage in target currency | Double getPriceChangePercentage24HInCurrency() | setPriceChangePercentage24HInCurrency(Double priceChangePercentage24HInCurrency) |
| `PriceChangePercentage7DInCurrency` | [`Double`](../../doc/models/precision.md) | Optional | 7-day price change percentage in target currency | Double getPriceChangePercentage7DInCurrency() | setPriceChangePercentage7DInCurrency(Double priceChangePercentage7DInCurrency) |
| `PriceChangePercentage14DInCurrency` | [`Double`](../../doc/models/precision.md) | Optional | 14-day price change percentage in target currency | Double getPriceChangePercentage14DInCurrency() | setPriceChangePercentage14DInCurrency(Double priceChangePercentage14DInCurrency) |
| `PriceChangePercentage30DInCurrency` | [`Double`](../../doc/models/precision.md) | Optional | 30-day price change percentage in target currency | Double getPriceChangePercentage30DInCurrency() | setPriceChangePercentage30DInCurrency(Double priceChangePercentage30DInCurrency) |
| `PriceChangePercentage200DInCurrency` | [`Double`](../../doc/models/precision.md) | Optional | 200-day price change percentage in target currency | Double getPriceChangePercentage200DInCurrency() | setPriceChangePercentage200DInCurrency(Double priceChangePercentage200DInCurrency) |
| `PriceChangePercentage1YInCurrency` | [`Double`](../../doc/models/precision.md) | Optional | 1-year price change percentage in target currency | Double getPriceChangePercentage1YInCurrency() | setPriceChangePercentage1YInCurrency(Double priceChangePercentage1YInCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.DateTimeHelper;
import com.coingecko.api.models.CoinsMarket;
import com.coingecko.api.models.Roi2;
import com.coingecko.api.models.SparklineIn7D;
import java.io.IOException;
import java.util.Arrays;

CoinsMarket coinsMarket = new CoinsMarket.Builder(
    "id6",
    "symbol2",
    "name6",
    "image0",
    207.02D,
    220.54D,
    26,
    171.88D,
    121.68D,
    129.94D,
    141.82D,
    45.94D,
    116.7D,
    224.9D,
    206.58D,
    137.36D,
    115.24D,
    71.88D,
    111.52D,
    158.58D,
    DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
    244.4D,
    47.94D,
    DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
    new Roi2.Builder()
        .times(28.88D)
        .currency("currency0")
        .percentage(145.98D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z")
)
.marketCapRankWithRehypothecated(242)
.sparklineIn7D(new SparklineIn7D.Builder()
        .price(Arrays.asList(
            192D,
            191.99D
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.priceChangePercentage1HInCurrency(58.48D)
.priceChangePercentage24HInCurrency(141.28D)
.priceChangePercentage7DInCurrency(92.46D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

