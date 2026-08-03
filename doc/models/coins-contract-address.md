
# Coins Contract Address

*This model accepts additional fields of type Object.*

## Structure

`CoinsContractAddress`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Coin ID | String getId() | setId(String id) |
| `Symbol` | `String` | Required | Coin symbol | String getSymbol() | setSymbol(String symbol) |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `WebSlug` | `String` | Required | Coin web slug | String getWebSlug() | setWebSlug(String webSlug) |
| `AssetPlatformId` | `String` | Required | Coin asset platform ID | String getAssetPlatformId() | setAssetPlatformId(String assetPlatformId) |
| `Platforms` | `Map<String, String>` | Required | Coin asset platform and contract address | Map<String, String> getPlatforms() | setPlatforms(Map<String, String> platforms) |
| `DetailPlatforms` | [`Map<String, DetailPlatforms>`](../../doc/models/detail-platforms.md) | Required | Detailed coin asset platform and contract address | Map<String, DetailPlatforms> getDetailPlatforms() | setDetailPlatforms(Map<String, DetailPlatforms> detailPlatforms) |
| `BlockTimeInMinutes` | [`double`](../../doc/models/precision.md) | Required | Blockchain block time in minutes | double getBlockTimeInMinutes() | setBlockTimeInMinutes(double blockTimeInMinutes) |
| `HashingAlgorithm` | `String` | Required | Blockchain hashing algorithm | String getHashingAlgorithm() | setHashingAlgorithm(String hashingAlgorithm) |
| `Categories` | `List<String>` | Required | Coin categories | List<String> getCategories() | setCategories(List<String> categories) |
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
| `ContractAddress` | `String` | Required | Coin contract address | String getContractAddress() | setContractAddress(String contractAddress) |
| `SentimentVotesUpPercentage` | [`Double`](../../doc/models/precision.md) | Required | Sentiment votes up percentage | Double getSentimentVotesUpPercentage() | setSentimentVotesUpPercentage(Double sentimentVotesUpPercentage) |
| `SentimentVotesDownPercentage` | [`Double`](../../doc/models/precision.md) | Required | Sentiment votes down percentage | Double getSentimentVotesDownPercentage() | setSentimentVotesDownPercentage(Double sentimentVotesDownPercentage) |
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
import com.coingecko.api.models.CoinsContractAddress;
import com.coingecko.api.models.CommunityData1;
import com.coingecko.api.models.DetailPlatforms;
import com.coingecko.api.models.DeveloperData1;
import com.coingecko.api.models.Image1;
import com.coingecko.api.models.Links;
import com.coingecko.api.models.Market1;
import com.coingecko.api.models.MarketData1;
import com.coingecko.api.models.Roi;
import com.coingecko.api.models.StatusUpdate;
import com.coingecko.api.models.Ticker1;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

CoinsContractAddress coinsContractAddress = new CoinsContractAddress.Builder(
    "id6",
    "symbol2",
    "name6",
    "web_slug6",
    "asset_platform_id8",
    new LinkedHashMap<String, String>() {{
        put("key0", "platforms1");
    }},
    new LinkedHashMap<String, DetailPlatforms>() {{
        put("key0", new DetailPlatforms.Builder()
            .decimalPlace(250)
            .contractAddress("contract_address4")
            .geckoterminalUrl("geckoterminal_url0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build());
        put("key1", new DetailPlatforms.Builder()
            .decimalPlace(250)
            .contractAddress("contract_address4")
            .geckoterminalUrl("geckoterminal_url0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build());
    }},
    93.18D,
    "hashing_algorithm4",
    Arrays.asList(
        "categories2",
        "categories1",
        "categories0"
    ),
    false,
    "public_notice4",
    Arrays.asList(
        "additional_notices1",
        "additional_notices0"
    ),
    false,
    new LinkedHashMap<String, String>() {{
        put("key0", "description1");
        put("key1", "description2");
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
    "country_origin6",
    "genesis_date0",
    "contract_address0",
    36.82D,
    37.6D,
    195.84D,
    16,
    252,
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
    "last_updated8"
)
.localization(new LinkedHashMap<String, String>() {{
        put("key0", "localization8");
        put("key1", "localization9");
    }})
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
.developerData(new DeveloperData1.Builder()
        .forks(63.8D)
        .stars(132.7D)
        .subscribers(173.76D)
        .totalIssues(68.92D)
        .closedIssues(119.96D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.tickers(Arrays.asList(
        new Ticker1.Builder()
            .base("base6")
            .target("target2")
            .market(new Market1.Builder()
                .name("name0")
                .identifier("identifier2")
                .hasTradingIncentive(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .last(99.8D)
            .volume(36.06D)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Ticker1.Builder()
            .base("base6")
            .target("target2")
            .market(new Market1.Builder()
                .name("name0")
                .identifier("identifier2")
                .hasTradingIncentive(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .last(99.8D)
            .volume(36.06D)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

