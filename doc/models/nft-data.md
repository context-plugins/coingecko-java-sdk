
# Nft Data

*This model accepts additional fields of type Object.*

## Structure

`NftData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | NFT collection ID | String getId() | setId(String id) |
| `WebSlug` | `String` | Required | NFT collection web slug | String getWebSlug() | setWebSlug(String webSlug) |
| `ContractAddress` | `String` | Required | NFT collection contract address | String getContractAddress() | setContractAddress(String contractAddress) |
| `AssetPlatformId` | `String` | Required | NFT collection asset platform ID | String getAssetPlatformId() | setAssetPlatformId(String assetPlatformId) |
| `Name` | `String` | Required | NFT collection name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | NFT collection symbol | String getSymbol() | setSymbol(String symbol) |
| `Image` | [`Image5`](../../doc/models/image-5.md) | Required | NFT collection image URLs | Image5 getImage() | setImage(Image5 image) |
| `BannerImage` | `String` | Required | NFT collection banner image URL | String getBannerImage() | setBannerImage(String bannerImage) |
| `Description` | `String` | Required | NFT collection description | String getDescription() | setDescription(String description) |
| `NativeCurrency` | `String` | Required | NFT collection native currency | String getNativeCurrency() | setNativeCurrency(String nativeCurrency) |
| `NativeCurrencySymbol` | `String` | Required | NFT collection native currency symbol | String getNativeCurrencySymbol() | setNativeCurrencySymbol(String nativeCurrencySymbol) |
| `MarketCapRank` | `Integer` | Required | NFT collection market cap rank | Integer getMarketCapRank() | setMarketCapRank(Integer marketCapRank) |
| `FloorPrice` | [`FloorPrice`](../../doc/models/floor-price.md) | Required | NFT collection floor price | FloorPrice getFloorPrice() | setFloorPrice(FloorPrice floorPrice) |
| `MarketCap` | [`MarketCap`](../../doc/models/market-cap.md) | Required | NFT collection market cap | MarketCap getMarketCap() | setMarketCap(MarketCap marketCap) |
| `Volume24H` | [`Volume24H`](../../doc/models/volume-24-h.md) | Required | NFT collection volume in 24 hours | Volume24H getVolume24H() | setVolume24H(Volume24H volume24H) |
| `FloorPriceInUsd24HPercentageChange` | [`double`](../../doc/models/precision.md) | Required | NFT collection floor price in USD 24 hours percentage change | double getFloorPriceInUsd24HPercentageChange() | setFloorPriceInUsd24HPercentageChange(double floorPriceInUsd24HPercentageChange) |
| `FloorPrice24HPercentageChange` | [`FloorPrice24HPercentageChange`](../../doc/models/floor-price-24-h-percentage-change.md) | Required | NFT collection floor price 24 hours percentage change | FloorPrice24HPercentageChange getFloorPrice24HPercentageChange() | setFloorPrice24HPercentageChange(FloorPrice24HPercentageChange floorPrice24HPercentageChange) |
| `MarketCap24HPercentageChange` | [`MarketCap24HPercentageChange`](../../doc/models/market-cap-24-h-percentage-change.md) | Required | NFT collection market cap 24 hours percentage change | MarketCap24HPercentageChange getMarketCap24HPercentageChange() | setMarketCap24HPercentageChange(MarketCap24HPercentageChange marketCap24HPercentageChange) |
| `Volume24HPercentageChange` | [`Volume24HPercentageChange`](../../doc/models/volume-24-h-percentage-change.md) | Required | NFT collection volume in 24 hours percentage change | Volume24HPercentageChange getVolume24HPercentageChange() | setVolume24HPercentageChange(Volume24HPercentageChange volume24HPercentageChange) |
| `NumberOfUniqueAddresses` | [`double`](../../doc/models/precision.md) | Required | Number of unique addresses owning the NFTs | double getNumberOfUniqueAddresses() | setNumberOfUniqueAddresses(double numberOfUniqueAddresses) |
| `NumberOfUniqueAddresses24HPercentageChange` | [`double`](../../doc/models/precision.md) | Required | Number of unique addresses 24 hours percentage change | double getNumberOfUniqueAddresses24HPercentageChange() | setNumberOfUniqueAddresses24HPercentageChange(double numberOfUniqueAddresses24HPercentageChange) |
| `VolumeInUsd24HPercentageChange` | [`double`](../../doc/models/precision.md) | Required | NFT collection volume in USD 24 hours percentage change | double getVolumeInUsd24HPercentageChange() | setVolumeInUsd24HPercentageChange(double volumeInUsd24HPercentageChange) |
| `TotalSupply` | [`double`](../../doc/models/precision.md) | Required | NFT collection total supply | double getTotalSupply() | setTotalSupply(double totalSupply) |
| `OneDaySales` | [`Double`](../../doc/models/precision.md) | Required | NFT collection one day sales | Double getOneDaySales() | setOneDaySales(Double oneDaySales) |
| `OneDaySales24HPercentageChange` | [`double`](../../doc/models/precision.md) | Required | NFT collection one day sales 24 hours percentage change | double getOneDaySales24HPercentageChange() | setOneDaySales24HPercentageChange(double oneDaySales24HPercentageChange) |
| `OneDayAverageSalePrice` | [`Double`](../../doc/models/precision.md) | Required | NFT collection one day average sale price | Double getOneDayAverageSalePrice() | setOneDayAverageSalePrice(Double oneDayAverageSalePrice) |
| `OneDayAverageSalePrice24HPercentageChange` | [`double`](../../doc/models/precision.md) | Required | NFT collection one day average sale price 24 hours percentage change | double getOneDayAverageSalePrice24HPercentageChange() | setOneDayAverageSalePrice24HPercentageChange(double oneDayAverageSalePrice24HPercentageChange) |
| `Links` | [`Links2`](../../doc/models/links-2.md) | Required | NFT collection links | Links2 getLinks() | setLinks(Links2 links) |
| `FloorPrice7DPercentageChange` | [`FloorPrice7DPercentageChange`](../../doc/models/floor-price-7-d-percentage-change.md) | Required | NFT collection floor price 7 days percentage change | FloorPrice7DPercentageChange getFloorPrice7DPercentageChange() | setFloorPrice7DPercentageChange(FloorPrice7DPercentageChange floorPrice7DPercentageChange) |
| `FloorPrice14DPercentageChange` | [`FloorPrice14DPercentageChange`](../../doc/models/floor-price-14-d-percentage-change.md) | Required | NFT collection floor price 14 days percentage change | FloorPrice14DPercentageChange getFloorPrice14DPercentageChange() | setFloorPrice14DPercentageChange(FloorPrice14DPercentageChange floorPrice14DPercentageChange) |
| `FloorPrice30DPercentageChange` | [`FloorPrice30DPercentageChange`](../../doc/models/floor-price-30-d-percentage-change.md) | Required | NFT collection floor price 30 days percentage change | FloorPrice30DPercentageChange getFloorPrice30DPercentageChange() | setFloorPrice30DPercentageChange(FloorPrice30DPercentageChange floorPrice30DPercentageChange) |
| `FloorPrice60DPercentageChange` | [`FloorPrice60DPercentageChange`](../../doc/models/floor-price-60-d-percentage-change.md) | Required | NFT collection floor price 60 days percentage change | FloorPrice60DPercentageChange getFloorPrice60DPercentageChange() | setFloorPrice60DPercentageChange(FloorPrice60DPercentageChange floorPrice60DPercentageChange) |
| `FloorPrice1YPercentageChange` | [`FloorPrice1YPercentageChange`](../../doc/models/floor-price-1-y-percentage-change.md) | Required | NFT collection floor price 1 year percentage change | FloorPrice1YPercentageChange getFloorPrice1YPercentageChange() | setFloorPrice1YPercentageChange(FloorPrice1YPercentageChange floorPrice1YPercentageChange) |
| `Explorers` | [`List<Explorer>`](../../doc/models/explorer.md) | Required | NFT collection block explorer links | List<Explorer> getExplorers() | setExplorers(List<Explorer> explorers) |
| `UserFavoritesCount` | `int` | Required | NFT collection user favorites count | int getUserFavoritesCount() | setUserFavoritesCount(int userFavoritesCount) |
| `Ath` | [`Ath`](../../doc/models/ath.md) | Required | NFT collection all time highs | Ath getAth() | setAth(Ath ath) |
| `AthChangePercentage` | [`AthChangePercentage`](../../doc/models/ath-change-percentage.md) | Required | NFT collection all time highs change percentage | AthChangePercentage getAthChangePercentage() | setAthChangePercentage(AthChangePercentage athChangePercentage) |
| `AthDate` | [`AthDate`](../../doc/models/ath-date.md) | Required | NFT collection all time highs date | AthDate getAthDate() | setAthDate(AthDate athDate) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.DateTimeHelper;
import com.coingecko.api.models.Ath;
import com.coingecko.api.models.AthChangePercentage;
import com.coingecko.api.models.AthDate;
import com.coingecko.api.models.Explorer;
import com.coingecko.api.models.FloorPrice;
import com.coingecko.api.models.FloorPrice14DPercentageChange;
import com.coingecko.api.models.FloorPrice1YPercentageChange;
import com.coingecko.api.models.FloorPrice24HPercentageChange;
import com.coingecko.api.models.FloorPrice30DPercentageChange;
import com.coingecko.api.models.FloorPrice60DPercentageChange;
import com.coingecko.api.models.FloorPrice7DPercentageChange;
import com.coingecko.api.models.Image5;
import com.coingecko.api.models.Links2;
import com.coingecko.api.models.MarketCap;
import com.coingecko.api.models.MarketCap24HPercentageChange;
import com.coingecko.api.models.NftData;
import com.coingecko.api.models.Volume24H;
import com.coingecko.api.models.Volume24HPercentageChange;
import java.io.IOException;
import java.util.Arrays;

NftData nftData = new NftData.Builder(
    "id8",
    "web_slug6",
    "contract_address2",
    "asset_platform_id0",
    "name8",
    "symbol0",
    new Image5.Builder()
        .small("small0")
        .small2X("small_2x8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "banner_image4",
    "description8",
    "native_currency8",
    "native_currency_symbol2",
    98,
    new FloorPrice.Builder()
        .nativeCurrency(137.38D)
        .usd(36.82D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new MarketCap.Builder()
        .nativeCurrency(156.9D)
        .usd(238.7D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new Volume24H.Builder()
        .nativeCurrency(61.38D)
        .usd(143.18D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    65.18D,
    new FloorPrice24HPercentageChange.Builder()
        .usd(127.92D)
        .nativeCurrency(46.12D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new MarketCap24HPercentageChange.Builder()
        .usd(49.82D)
        .nativeCurrency(224.02D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new Volume24HPercentageChange.Builder()
        .usd(88.54D)
        .nativeCurrency(6.74D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    211.12D,
    116.8D,
    28.06D,
    0.76D,
    140.74D,
    136.9D,
    110.06D,
    168.96D,
    new Links2.Builder()
        .homepage("homepage0")
        .twitter("twitter0")
        .discord("discord4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new FloorPrice7DPercentageChange.Builder()
        .usd(18.72D)
        .nativeCurrency(192.92D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new FloorPrice14DPercentageChange.Builder()
        .usd(39.12D)
        .nativeCurrency(213.32D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new FloorPrice30DPercentageChange.Builder()
        .usd(32.38D)
        .nativeCurrency(206.58D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new FloorPrice60DPercentageChange.Builder()
        .usd(61.98D)
        .nativeCurrency(236.18D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new FloorPrice1YPercentageChange.Builder()
        .usd(92.94D)
        .nativeCurrency(11.14D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    Arrays.asList(
        new Explorer.Builder()
            .name("name0")
            .link("link0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ),
    110,
    new Ath.Builder()
        .nativeCurrency(47.88D)
        .usd(129.68D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new AthChangePercentage.Builder()
        .nativeCurrency(192.22D)
        .usd(18.02D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new AthDate.Builder()
        .nativeCurrency(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .usd(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

