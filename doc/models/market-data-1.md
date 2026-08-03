
# Market Data 1

Market data

*This model accepts additional fields of type Object.*

## Structure

`MarketData1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CurrentPrice` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | Current price in target currency | Map<String, Double> getCurrentPrice() | setCurrentPrice(Map<String, Double> currentPrice) |
| `TotalValueLocked` | [`Double`](../../doc/models/precision.md) | Optional | Total value locked | Double getTotalValueLocked() | setTotalValueLocked(Double totalValueLocked) |
| `McapToTvlRatio` | [`Double`](../../doc/models/precision.md) | Optional | Market cap to TVL ratio | Double getMcapToTvlRatio() | setMcapToTvlRatio(Double mcapToTvlRatio) |
| `FdvToTvlRatio` | [`Double`](../../doc/models/precision.md) | Optional | FDV to TVL ratio | Double getFdvToTvlRatio() | setFdvToTvlRatio(Double fdvToTvlRatio) |
| `Roi` | [`Roi`](../../doc/models/roi.md) | Optional | Return on investment | Roi getRoi() | setRoi(Roi roi) |
| `Ath` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | All-time high in target currency | Map<String, Double> getAth() | setAth(Map<String, Double> ath) |
| `AthChangePercentage` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | All-time high change percentage | Map<String, Double> getAthChangePercentage() | setAthChangePercentage(Map<String, Double> athChangePercentage) |
| `AthDate` | `Map<String, String>` | Optional | All-time high date | Map<String, String> getAthDate() | setAthDate(Map<String, String> athDate) |
| `Atl` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | All-time low in target currency | Map<String, Double> getAtl() | setAtl(Map<String, Double> atl) |
| `AtlChangePercentage` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | All-time low change percentage | Map<String, Double> getAtlChangePercentage() | setAtlChangePercentage(Map<String, Double> atlChangePercentage) |
| `AtlDate` | `Map<String, String>` | Optional | All-time low date | Map<String, String> getAtlDate() | setAtlDate(Map<String, String> atlDate) |
| `MarketCap` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | Market cap in target currency | Map<String, Double> getMarketCap() | setMarketCap(Map<String, Double> marketCap) |
| `FullyDilutedValuation` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | Fully diluted valuation in target currency | Map<String, Double> getFullyDilutedValuation() | setFullyDilutedValuation(Map<String, Double> fullyDilutedValuation) |
| `MarketCapFdvRatio` | [`Double`](../../doc/models/precision.md) | Optional | Market cap to FDV ratio | Double getMarketCapFdvRatio() | setMarketCapFdvRatio(Double marketCapFdvRatio) |
| `MarketCapRank` | `Integer` | Optional | Market cap rank | Integer getMarketCapRank() | setMarketCapRank(Integer marketCapRank) |
| `OutstandingTokenValueUsd` | [`Double`](../../doc/models/precision.md) | Optional | Outstanding token value in USD | Double getOutstandingTokenValueUsd() | setOutstandingTokenValueUsd(Double outstandingTokenValueUsd) |
| `MarketCapRankWithRehypothecated` | `Integer` | Optional | Market cap rank including rehypothecated tokens | Integer getMarketCapRankWithRehypothecated() | setMarketCapRankWithRehypothecated(Integer marketCapRankWithRehypothecated) |
| `TotalVolume` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | Total trading volume in target currency | Map<String, Double> getTotalVolume() | setTotalVolume(Map<String, Double> totalVolume) |
| `High24H` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 24h price high in target currency | Map<String, Double> getHigh24H() | setHigh24H(Map<String, Double> high24H) |
| `Low24H` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 24h price low in target currency | Map<String, Double> getLow24H() | setLow24H(Map<String, Double> low24H) |
| `PriceChange24H` | [`Double`](../../doc/models/precision.md) | Optional | 24h price change in target currency | Double getPriceChange24H() | setPriceChange24H(Double priceChange24H) |
| `PriceChangePercentage24H` | [`Double`](../../doc/models/precision.md) | Optional | 24h price change percentage | Double getPriceChangePercentage24H() | setPriceChangePercentage24H(Double priceChangePercentage24H) |
| `PriceChangePercentage7D` | [`Double`](../../doc/models/precision.md) | Optional | 7d price change percentage | Double getPriceChangePercentage7D() | setPriceChangePercentage7D(Double priceChangePercentage7D) |
| `PriceChangePercentage14D` | [`Double`](../../doc/models/precision.md) | Optional | 14d price change percentage | Double getPriceChangePercentage14D() | setPriceChangePercentage14D(Double priceChangePercentage14D) |
| `PriceChangePercentage30D` | [`Double`](../../doc/models/precision.md) | Optional | 30d price change percentage | Double getPriceChangePercentage30D() | setPriceChangePercentage30D(Double priceChangePercentage30D) |
| `PriceChangePercentage60D` | [`Double`](../../doc/models/precision.md) | Optional | 60d price change percentage | Double getPriceChangePercentage60D() | setPriceChangePercentage60D(Double priceChangePercentage60D) |
| `PriceChangePercentage200D` | [`Double`](../../doc/models/precision.md) | Optional | 200d price change percentage | Double getPriceChangePercentage200D() | setPriceChangePercentage200D(Double priceChangePercentage200D) |
| `PriceChangePercentage1Y` | [`Double`](../../doc/models/precision.md) | Optional | 1y price change percentage | Double getPriceChangePercentage1Y() | setPriceChangePercentage1Y(Double priceChangePercentage1Y) |
| `MarketCapChange24H` | [`Double`](../../doc/models/precision.md) | Optional | 24h market cap change in target currency | Double getMarketCapChange24H() | setMarketCapChange24H(Double marketCapChange24H) |
| `MarketCapChangePercentage24H` | [`Double`](../../doc/models/precision.md) | Optional | 24h market cap change percentage | Double getMarketCapChangePercentage24H() | setMarketCapChangePercentage24H(Double marketCapChangePercentage24H) |
| `PriceChange24HInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 24h price change in target currency | Map<String, Double> getPriceChange24HInCurrency() | setPriceChange24HInCurrency(Map<String, Double> priceChange24HInCurrency) |
| `PriceChangePercentage1HInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 1h price change percentage per currency | Map<String, Double> getPriceChangePercentage1HInCurrency() | setPriceChangePercentage1HInCurrency(Map<String, Double> priceChangePercentage1HInCurrency) |
| `PriceChangePercentage24HInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 24h price change percentage per currency | Map<String, Double> getPriceChangePercentage24HInCurrency() | setPriceChangePercentage24HInCurrency(Map<String, Double> priceChangePercentage24HInCurrency) |
| `PriceChangePercentage7DInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 7d price change percentage per currency | Map<String, Double> getPriceChangePercentage7DInCurrency() | setPriceChangePercentage7DInCurrency(Map<String, Double> priceChangePercentage7DInCurrency) |
| `PriceChangePercentage14DInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 14d price change percentage per currency | Map<String, Double> getPriceChangePercentage14DInCurrency() | setPriceChangePercentage14DInCurrency(Map<String, Double> priceChangePercentage14DInCurrency) |
| `PriceChangePercentage30DInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 30d price change percentage per currency | Map<String, Double> getPriceChangePercentage30DInCurrency() | setPriceChangePercentage30DInCurrency(Map<String, Double> priceChangePercentage30DInCurrency) |
| `PriceChangePercentage60DInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 60d price change percentage per currency | Map<String, Double> getPriceChangePercentage60DInCurrency() | setPriceChangePercentage60DInCurrency(Map<String, Double> priceChangePercentage60DInCurrency) |
| `PriceChangePercentage200DInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 200d price change percentage per currency | Map<String, Double> getPriceChangePercentage200DInCurrency() | setPriceChangePercentage200DInCurrency(Map<String, Double> priceChangePercentage200DInCurrency) |
| `PriceChangePercentage1YInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 1y price change percentage per currency | Map<String, Double> getPriceChangePercentage1YInCurrency() | setPriceChangePercentage1YInCurrency(Map<String, Double> priceChangePercentage1YInCurrency) |
| `MarketCapChange24HInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 24h market cap change in target currency | Map<String, Double> getMarketCapChange24HInCurrency() | setMarketCapChange24HInCurrency(Map<String, Double> marketCapChange24HInCurrency) |
| `MarketCapChangePercentage24HInCurrency` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | 24h market cap change percentage per currency | Map<String, Double> getMarketCapChangePercentage24HInCurrency() | setMarketCapChangePercentage24HInCurrency(Map<String, Double> marketCapChangePercentage24HInCurrency) |
| `TotalSupply` | [`Double`](../../doc/models/precision.md) | Optional | Total supply | Double getTotalSupply() | setTotalSupply(Double totalSupply) |
| `MaxSupply` | [`Double`](../../doc/models/precision.md) | Optional | Max supply | Double getMaxSupply() | setMaxSupply(Double maxSupply) |
| `MaxSupplyInfinite` | `Boolean` | Optional | Max supply infinite | Boolean getMaxSupplyInfinite() | setMaxSupplyInfinite(Boolean maxSupplyInfinite) |
| `CirculatingSupply` | [`Double`](../../doc/models/precision.md) | Optional | Circulating supply | Double getCirculatingSupply() | setCirculatingSupply(Double circulatingSupply) |
| `OutstandingSupply` | [`Double`](../../doc/models/precision.md) | Optional | Tokens outstanding in the market | Double getOutstandingSupply() | setOutstandingSupply(Double outstandingSupply) |
| `LastUpdated` | `String` | Optional | Market data last updated timestamp | String getLastUpdated() | setLastUpdated(String lastUpdated) |
| `Sparkline7D` | [`List<Double>`](../../doc/models/precision.md) | Optional | Sparkline 7-day price data | List<Double> getSparkline7D() | setSparkline7D(List<Double> sparkline7D) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.MarketData1;
import com.coingecko.api.models.Roi;
import java.io.IOException;
import java.util.LinkedHashMap;

MarketData1 marketData1 = new MarketData1.Builder()
    .currentPrice(new LinkedHashMap<String, Double>() {{
        put("key0", 159.25D);
        put("key1", 159.26D);
        put("key2", 159.27D);
    }})
    .totalValueLocked(117.04D)
    .mcapToTvlRatio(169.56D)
    .fdvToTvlRatio(136.66D)
    .roi(new Roi.Builder()
        .times(28.88D)
        .currency("currency0")
        .percentage(145.98D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

