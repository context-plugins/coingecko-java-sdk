
# Attributes 7

*This model accepts additional fields of type Object.*

## Structure

`Attributes7`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | `String` | Required | Token contract address | String getAddress() | setAddress(String address) |
| `Name` | `String` | Required | Token name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | Token symbol | String getSymbol() | setSymbol(String symbol) |
| `Decimals` | `int` | Required | Token decimals | int getDecimals() | setDecimals(int decimals) |
| `ImageUrl` | `String` | Required | Token image URL | String getImageUrl() | setImageUrl(String imageUrl) |
| `Image` | [`Image6`](../../doc/models/image-6.md) | Required | Token image URLs in different sizes | Image6 getImage() | setImage(Image6 image) |
| `BannerImageUrl` | `String` | Required | Token banner image URL | String getBannerImageUrl() | setBannerImageUrl(String bannerImageUrl) |
| `CoingeckoCoinId` | `String` | Required | CoinGecko coin ID | String getCoingeckoCoinId() | setCoingeckoCoinId(String coingeckoCoinId) |
| `Websites` | `List<String>` | Required | Token websites | List<String> getWebsites() | setWebsites(List<String> websites) |
| `DiscordUrl` | `String` | Required | Discord URL | String getDiscordUrl() | setDiscordUrl(String discordUrl) |
| `FarcasterUrl` | `String` | Required | Farcaster URL | String getFarcasterUrl() | setFarcasterUrl(String farcasterUrl) |
| `ZoraUrl` | `String` | Required | Zora URL | String getZoraUrl() | setZoraUrl(String zoraUrl) |
| `TelegramHandle` | `String` | Required | Telegram handle | String getTelegramHandle() | setTelegramHandle(String telegramHandle) |
| `TwitterHandle` | `String` | Required | Twitter handle | String getTwitterHandle() | setTwitterHandle(String twitterHandle) |
| `Description` | `String` | Required | Token description | String getDescription() | setDescription(String description) |
| `GtScore` | [`double`](../../doc/models/precision.md) | Required | GeckoTerminal trust score | double getGtScore() | setGtScore(double gtScore) |
| `GtScoreDetails` | [`GtScoreDetails`](../../doc/models/gt-score-details.md) | Required | GeckoTerminal trust score breakdown | GtScoreDetails getGtScoreDetails() | setGtScoreDetails(GtScoreDetails gtScoreDetails) |
| `GtVerified` | `boolean` | Required | Whether the token is verified on GeckoTerminal | boolean getGtVerified() | setGtVerified(boolean gtVerified) |
| `Categories` | `List<String>` | Required | Token categories | List<String> getCategories() | setCategories(List<String> categories) |
| `GtCategoryIds` | `List<String>` | Required | GeckoTerminal category IDs | List<String> getGtCategoryIds() | setGtCategoryIds(List<String> gtCategoryIds) |
| `Holders` | [`Holders`](../../doc/models/holders.md) | Required | Token holder information | Holders getHolders() | setHolders(Holders holders) |
| `MintAuthority` | `String` | Required | Mint authority status | String getMintAuthority() | setMintAuthority(String mintAuthority) |
| `FreezeAuthority` | `String` | Required | Freeze authority status | String getFreezeAuthority() | setFreezeAuthority(String freezeAuthority) |
| `IsHoneypot` | [`Attributes7IsHoneypot`](../../doc/models/containers/attributes-7-is-honeypot.md) | Required | This is a container for one-of cases. | Attributes7IsHoneypot getIsHoneypot() | setIsHoneypot(Attributes7IsHoneypot isHoneypot) |
| `DeveloperAddress` | `String` | Required | Developer wallet address | String getDeveloperAddress() | setDeveloperAddress(String developerAddress) |
| `DeveloperHoldingPercentage` | `String` | Required | Developer holding as a percentage of total supply | String getDeveloperHoldingPercentage() | setDeveloperHoldingPercentage(String developerHoldingPercentage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes7;
import com.coingecko.api.models.GtScoreDetails;
import com.coingecko.api.models.Holders;
import com.coingecko.api.models.Image6;
import com.coingecko.api.models.containers.Attributes7IsHoneypot;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

Attributes7 attributes7 = new Attributes7.Builder(
    "address6",
    "name0",
    "symbol8",
    50,
    "image_url6",
    new Image6.Builder()
        .thumb("thumb4")
        .small("small0")
        .large("large8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "banner_image_url8",
    "coingecko_coin_id8",
    Arrays.asList(
        "websites7",
        "websites6"
    ),
    "discord_url4",
    "farcaster_url2",
    "zora_url0",
    "telegram_handle2",
    "twitter_handle6",
    "description0",
    58.76D,
    new GtScoreDetails.Builder()
        .pool(155.82D)
        .transaction(141.8D)
        .creation(88.54D)
        .info(69.28D)
        .holders(31.82D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    false,
    Arrays.asList(
        "categories4",
        "categories5"
    ),
    Arrays.asList(
        "gt_category_ids8",
        "gt_category_ids7",
        "gt_category_ids6"
    ),
    new Holders.Builder()
        .count(46)
        .distributionPercentage(new LinkedHashMap<String, String>() {{
            put("key0", "distribution_percentage0");
            put("key1", "distribution_percentage1");
        }})
        .lastUpdated("last_updated8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "mint_authority2",
    "freeze_authority8",
    Attributes7IsHoneypot.fromBoolean(
        true
    ),
    "developer_address4",
    "developer_holding_percentage8"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

