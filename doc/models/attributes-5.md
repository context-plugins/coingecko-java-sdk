
# Attributes 5

*This model accepts additional fields of type Object.*

## Structure

`Attributes5`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | `String` | Required | Token contract address | String getAddress() | setAddress(String address) |
| `Name` | `String` | Required | Token name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | Token symbol | String getSymbol() | setSymbol(String symbol) |
| `Decimals` | `int` | Required | Token decimals | int getDecimals() | setDecimals(int decimals) |
| `ImageUrl` | `String` | Required | Token image URL | String getImageUrl() | setImageUrl(String imageUrl) |
| `CoingeckoCoinId` | `String` | Required | CoinGecko coin ID | String getCoingeckoCoinId() | setCoingeckoCoinId(String coingeckoCoinId) |
| `Websites` | `List<String>` | Required | Token websites | List<String> getWebsites() | setWebsites(List<String> websites) |
| `DiscordUrl` | `String` | Required | Discord URL | String getDiscordUrl() | setDiscordUrl(String discordUrl) |
| `FarcasterUrl` | `String` | Required | Farcaster URL | String getFarcasterUrl() | setFarcasterUrl(String farcasterUrl) |
| `ZoraUrl` | `String` | Required | Zora URL | String getZoraUrl() | setZoraUrl(String zoraUrl) |
| `TelegramHandle` | `String` | Required | Telegram handle | String getTelegramHandle() | setTelegramHandle(String telegramHandle) |
| `TwitterHandle` | `String` | Required | Twitter handle | String getTwitterHandle() | setTwitterHandle(String twitterHandle) |
| `Description` | `String` | Required | Token description | String getDescription() | setDescription(String description) |
| `GtScore` | [`Double`](../../doc/models/precision.md) | Required | GeckoTerminal trust score | Double getGtScore() | setGtScore(Double gtScore) |
| `MetadataUpdatedAt` | `String` | Required | Metadata last updated timestamp | String getMetadataUpdatedAt() | setMetadataUpdatedAt(String metadataUpdatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes5;
import java.io.IOException;
import java.util.Arrays;

Attributes5 attributes5 = new Attributes5.Builder(
    "address6",
    "name0",
    "symbol8",
    248,
    "image_url6",
    "coingecko_coin_id8",
    Arrays.asList(
        "websites9"
    ),
    "discord_url4",
    "farcaster_url2",
    "zora_url0",
    "telegram_handle2",
    "twitter_handle4",
    "description0",
    117.06D,
    "metadata_updated_at4"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

