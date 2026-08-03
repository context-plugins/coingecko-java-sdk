
# Coins Id

*This model accepts additional fields of type Object.*

## Structure

`CoinsId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Coin ID | String getId() | setId(String id) |
| `Symbol` | `String` | Required | Coin symbol | String getSymbol() | setSymbol(String symbol) |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `WebSlug` | `String` | Required | Coin web slug | String getWebSlug() | setWebSlug(String webSlug) |
| `AssetPlatformId` | `String` | Required | Coin asset platform ID | String getAssetPlatformId() | setAssetPlatformId(String assetPlatformId) |
| `Platforms` | `Map<String, String>` | Required | Coin asset platform and contract address | Map<String, String> getPlatforms() | setPlatforms(Map<String, String> platforms) |
| `DetailPlatforms` | [`Map<String, DetailPlatforms1>`](../../doc/models/detail-platforms-1.md) | Required | Detailed coin asset platform and contract address | Map<String, DetailPlatforms1> getDetailPlatforms() | setDetailPlatforms(Map<String, DetailPlatforms1> detailPlatforms) |
| `BlockTimeInMinutes` | [`double`](../../doc/models/precision.md) | Required | Blockchain block time in minutes | double getBlockTimeInMinutes() | setBlockTimeInMinutes(double blockTimeInMinutes) |
| `HashingAlgorithm` | `String` | Required | Blockchain hashing algorithm | String getHashingAlgorithm() | setHashingAlgorithm(String hashingAlgorithm) |
| `Categories` | `List<String>` | Required | Coin categories | List<String> getCategories() | setCategories(List<String> categories) |
| `CategoriesDetails` | [`List<CategoriesDetail>`](../../doc/models/categories-detail.md) | Optional | Detailed coin categories | List<CategoriesDetail> getCategoriesDetails() | setCategoriesDetails(List<CategoriesDetail> categoriesDetails) |
| `PreviewListing` | `boolean` | Required | Preview listing coin | boolean getPreviewListing() | setPreviewListing(boolean previewListing) |
| `PublicNotice` | `String` | Required | Public notice | String getPublicNotice() | setPublicNotice(String publicNotice) |
| `AdditionalNotices` | `List<String>` | Required | Additional notices | List<String> getAdditionalNotices() | setAdditionalNotices(List<String> additionalNotices) |
| `HasSupplyBreakdown` | `boolean` | Required | Whether detailed supply breakdown data is available via /coins/supply_breakdown | boolean getHasSupplyBreakdown() | setHasSupplyBreakdown(boolean hasSupplyBreakdown) |
| `Localization` | `Map<String, String>` | Optional | Coin name localization | Map<String, String> getLocalization() | setLocalization(Map<String, String> localization) |
| `Description` | `Map<String, String>` | Required | Coin description | Map<String, String> getDescription() | setDescription(Map<String, String> description) |
| `Links` | [`Links`](../../doc/models/links.md) | Required | Links | Links getLinks() | setLinks(Links links) |
| `Image` | [`Image1`](../../doc/models/image-1.md) | Required | Coin image URL | Image1 getImage() | setImage(Image1 image) |
| `CountryOrigin` | `String` | Required | Country of origin | String getCountryOrigin() | setCountryOrigin(String countryOrigin) |
| `GenesisDate` | `String` | Required | Genesis date | String getGenesisDate() | setGenesisDate(String genesisDate) |
| `SentimentVotesUpPercentage` | [`Double`](../../doc/models/precision.md) | Required | Sentiment votes up percentage | Double getSentimentVotesUpPercentage() | setSentimentVotesUpPercentage(Double sentimentVotesUpPercentage) |
| `SentimentVotesDownPercentage` | [`Double`](../../doc/models/precision.md) | Required | Sentiment votes down percentage | Double getSentimentVotesDownPercentage() | setSentimentVotesDownPercentage(Double sentimentVotesDownPercentage) |
| `IcoData` | [`IcoData`](../../doc/models/ico-data.md) | Optional | ICO data | IcoData getIcoData() | setIcoData(IcoData icoData) |
| `WatchlistPortfolioUsers` | [`double`](../../doc/models/precision.md) | Required | Number of users watching this coin in portfolio | double getWatchlistPortfolioUsers() | setWatchlistPortfolioUsers(double watchlistPortfolioUsers) |
| `MarketCapRank` | `Integer` | Required | Market cap rank | Integer getMarketCapRank() | setMarketCapRank(Integer marketCapRank) |
| `MarketCapRankWithRehypothecated` | `Integer` | Required | Market cap rank including rehypothecated tokens | Integer getMarketCapRankWithRehypothecated() | setMarketCapRankWithRehypothecated(Integer marketCapRankWithRehypothecated) |
| `MarketData` | [`MarketData1`](../../doc/models/market-data-1.md) | Optional | Market data | MarketData1 getMarketData() | setMarketData(MarketData1 marketData) |
| `CommunityData` | [`CommunityData1`](../../doc/models/community-data-1.md) | Optional | Community data | CommunityData1 getCommunityData() | setCommunityData(CommunityData1 communityData) |
| `DeveloperData` | [`DeveloperData1`](../../doc/models/developer-data-1.md) | Optional | Developer data | DeveloperData1 getDeveloperData() | setDeveloperData(DeveloperData1 developerData) |
| `StatusUpdates` | [`List<StatusUpdate>`](../../doc/models/status-update.md) | Required | Status updates | List<StatusUpdate> getStatusUpdates() | setStatusUpdates(List<StatusUpdate> statusUpdates) |
| `LastUpdated` | `String` | Required | Last updated timestamp | String getLastUpdated() | setLastUpdated(String lastUpdated) |
| `Tickers` | [`List<Ticker1>`](../../doc/models/ticker-1.md) | Optional | Tickers | List<Ticker1> getTickers() | setTickers(List<Ticker1> tickers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CategoriesDetail;
import com.coingecko.api.models.CoinsId;
import com.coingecko.api.models.CommunityData1;
import com.coingecko.api.models.DetailPlatforms1;
import com.coingecko.api.models.IcoData;
import com.coingecko.api.models.Image1;
import com.coingecko.api.models.Links;
import com.coingecko.api.models.MarketData1;
import com.coingecko.api.models.Roi;
import com.coingecko.api.models.StatusUpdate;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

CoinsId coinsId = new CoinsId.Builder(
    "id0",
    "symbol2",
    "name0",
    "web_slug2",
    "asset_platform_id2",
    new LinkedHashMap<String, String>() {{
        put("key0", "platforms5");
        put("key1", "platforms4");
    }},
    new LinkedHashMap<String, DetailPlatforms1>() {{
        put("key0", new DetailPlatforms1.Builder()
            .decimalPlace(250)
            .contractAddress("contract_address4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build());
    }},
    151.42D,
    "hashing_algorithm8",
    Arrays.asList(
        "categories6",
        "categories5"
    ),
    false,
    "public_notice0",
    Arrays.asList(
        "additional_notices5"
    ),
    false,
    new LinkedHashMap<String, String>() {{
        put("key0", "description5");
        put("key1", "description6");
        put("key2", "description7");
    }},
    new Links.Builder()
        .homepage(Arrays.asList(
            "homepage8",
            "homepage9",
            "homepage0"
        ))
        .whitepaper("whitepaper2")
        .blockchainSite(Arrays.asList(
            "blockchain_site1",
            "blockchain_site2",
            "blockchain_site3"
        ))
        .officialForumUrl(Arrays.asList(
            "official_forum_url8",
            "official_forum_url9"
        ))
        .chatUrl(Arrays.asList(
            "chat_url2"
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new Image1.Builder()
        .thumb("thumb4")
        .small("small0")
        .large("large8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "country_origin0",
    "genesis_date4",
    21.42D,
    95.84D,
    254.08D,
    208,
    196,
    Arrays.asList(
        new StatusUpdate.Builder()
            .description("description4")
            .category("category2")
            .createdAt("created_at2")
            .user("user4")
            .userTitle("user_title8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ),
    "last_updated2"
)
.categoriesDetails(Arrays.asList(
        new CategoriesDetail.Builder()
            .id("id4")
            .name("name4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new CategoriesDetail.Builder()
            .id("id4")
            .name("name4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new CategoriesDetail.Builder()
            .id("id4")
            .name("name4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.localization(new LinkedHashMap<String, String>() {{
        put("key0", "localization2");
        put("key1", "localization3");
        put("key2", "localization4");
    }})
.icoData(new IcoData.Builder()
        .icoStartDate("ico_start_date8")
        .icoEndDate("ico_end_date0")
        .shortDesc("short_desc8")
        .description("description6")
        .links(new LinkedHashMap<String, String>() {{
            put("key0", "links2");
            put("key1", "links3");
        }})
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.marketData(new MarketData1.Builder()
        .currentPrice(new LinkedHashMap<String, Double>() {{
            put("key0", 235.13D);
            put("key1", 235.14D);
        }})
        .totalValueLocked(41.16D)
        .mcapToTvlRatio(245.44D)
        .fdvToTvlRatio(212.54D)
        .roi(new Roi.Builder()
            .times(28.88D)
            .currency("currency0")
            .percentage(145.98D)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.communityData(new CommunityData1.Builder()
        .facebookLikes(230.38D)
        .redditAveragePosts48H(178.44D)
        .redditAverageComments48H(47.96D)
        .redditSubscribers(50.74D)
        .redditAccountsActive48H(153.56D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

