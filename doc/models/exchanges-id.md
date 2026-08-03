
# Exchanges Id

*This model accepts additional fields of type Object.*

## Structure

`ExchangesId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Exchange name | String getName() | setName(String name) |
| `YearEstablished` | [`Double`](../../doc/models/precision.md) | Required | Year the exchange was established | Double getYearEstablished() | setYearEstablished(Double yearEstablished) |
| `Country` | `String` | Required | Country where the exchange is based | String getCountry() | setCountry(String country) |
| `Description` | `String` | Required | Exchange description | String getDescription() | setDescription(String description) |
| `Url` | `String` | Required | Exchange website URL | String getUrl() | setUrl(String url) |
| `Image` | `String` | Required | Exchange logo URL | String getImage() | setImage(String image) |
| `FacebookUrl` | `String` | Required | Facebook URL | String getFacebookUrl() | setFacebookUrl(String facebookUrl) |
| `RedditUrl` | `String` | Required | Reddit URL | String getRedditUrl() | setRedditUrl(String redditUrl) |
| `TelegramUrl` | `String` | Required | Telegram URL | String getTelegramUrl() | setTelegramUrl(String telegramUrl) |
| `SlackUrl` | `String` | Required | Slack URL | String getSlackUrl() | setSlackUrl(String slackUrl) |
| `OtherUrl1` | `String` | Required | Other URL 1 | String getOtherUrl1() | setOtherUrl1(String otherUrl1) |
| `OtherUrl2` | `String` | Required | Other URL 2 | String getOtherUrl2() | setOtherUrl2(String otherUrl2) |
| `TwitterHandle` | `String` | Required | Twitter handle | String getTwitterHandle() | setTwitterHandle(String twitterHandle) |
| `HasTradingIncentive` | `boolean` | Required | Whether the exchange has trading incentive | boolean getHasTradingIncentive() | setHasTradingIncentive(boolean hasTradingIncentive) |
| `Centralized` | `boolean` | Required | Whether the exchange is centralized | boolean getCentralized() | setCentralized(boolean centralized) |
| `PublicNotice` | `String` | Required | Public notice | String getPublicNotice() | setPublicNotice(String publicNotice) |
| `AlertNotice` | `String` | Required | Alert notice | String getAlertNotice() | setAlertNotice(String alertNotice) |
| `TrustScore` | [`Double`](../../doc/models/precision.md) | Required | Exchange trust score | Double getTrustScore() | setTrustScore(Double trustScore) |
| `TrustScoreRank` | [`Double`](../../doc/models/precision.md) | Required | Exchange trust score rank | Double getTrustScoreRank() | setTrustScoreRank(Double trustScoreRank) |
| `Coins` | [`double`](../../doc/models/precision.md) | Required | Number of coins listed | double getCoins() | setCoins(double coins) |
| `Pairs` | [`double`](../../doc/models/precision.md) | Required | Number of trading pairs | double getPairs() | setPairs(double pairs) |
| `TradeVolume24HBtc` | [`double`](../../doc/models/precision.md) | Required | Exchange 24h trading volume in BTC | double getTradeVolume24HBtc() | setTradeVolume24HBtc(double tradeVolume24HBtc) |
| `Tickers` | [`List<Ticker3>`](../../doc/models/ticker-3.md) | Required | Exchange tickers | List<Ticker3> getTickers() | setTickers(List<Ticker3> tickers) |
| `StatusUpdates` | [`List<StatusUpdate2>`](../../doc/models/status-update-2.md) | Required | Status updates | List<StatusUpdate2> getStatusUpdates() | setStatusUpdates(List<StatusUpdate2> statusUpdates) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ExchangesId;
import com.coingecko.api.models.Market3;
import com.coingecko.api.models.StatusUpdate2;
import com.coingecko.api.models.Ticker3;
import java.io.IOException;
import java.util.Arrays;

ExchangesId exchangesId = new ExchangesId.Builder(
    "name8",
    3.64D,
    "country2",
    "description8",
    "url2",
    "image8",
    "facebook_url0",
    "reddit_url6",
    "telegram_url8",
    "slack_url4",
    "other_url_10",
    "other_url_24",
    "twitter_handle2",
    false,
    false,
    "public_notice2",
    "alert_notice6",
    30.78D,
    127.6D,
    44.82D,
    39.5D,
    120.72D,
    Arrays.asList(
        new Ticker3.Builder()
            .base("base6")
            .target("target2")
            .market(new Market3.Builder()
                .name("name0")
                .identifier("identifier2")
                .hasTradingIncentive(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .last(99.8D)
            .volume(36.06D)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ),
    Arrays.asList(
        new StatusUpdate2.Builder()
            .description("description4")
            .category("category2")
            .createdAt("created_at2")
            .user("user4")
            .userTitle("user_title8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

