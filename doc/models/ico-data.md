
# Ico Data

ICO data

*This model accepts additional fields of type Object.*

## Structure

`IcoData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IcoStartDate` | `String` | Optional | ICO start date | String getIcoStartDate() | setIcoStartDate(String icoStartDate) |
| `IcoEndDate` | `String` | Optional | ICO end date | String getIcoEndDate() | setIcoEndDate(String icoEndDate) |
| `ShortDesc` | `String` | Optional | Short description | String getShortDesc() | setShortDesc(String shortDesc) |
| `Description` | `String` | Optional | Detailed description | String getDescription() | setDescription(String description) |
| `Links` | `Map<String, String>` | Optional | ICO related links | Map<String, String> getLinks() | setLinks(Map<String, String> links) |
| `SoftcapCurrency` | `String` | Optional | Softcap currency | String getSoftcapCurrency() | setSoftcapCurrency(String softcapCurrency) |
| `HardcapCurrency` | `String` | Optional | Hardcap currency | String getHardcapCurrency() | setHardcapCurrency(String hardcapCurrency) |
| `TotalRaisedCurrency` | `String` | Optional | Total raised currency | String getTotalRaisedCurrency() | setTotalRaisedCurrency(String totalRaisedCurrency) |
| `SoftcapAmount` | [`Double`](../../doc/models/precision.md) | Optional | Softcap amount | Double getSoftcapAmount() | setSoftcapAmount(Double softcapAmount) |
| `HardcapAmount` | [`Double`](../../doc/models/precision.md) | Optional | Hardcap amount | Double getHardcapAmount() | setHardcapAmount(Double hardcapAmount) |
| `TotalRaised` | [`Double`](../../doc/models/precision.md) | Optional | Total raised amount | Double getTotalRaised() | setTotalRaised(Double totalRaised) |
| `QuotePreSaleCurrency` | `String` | Optional | Quote pre-sale currency | String getQuotePreSaleCurrency() | setQuotePreSaleCurrency(String quotePreSaleCurrency) |
| `BasePreSaleAmount` | [`Double`](../../doc/models/precision.md) | Optional | Base pre-sale amount | Double getBasePreSaleAmount() | setBasePreSaleAmount(Double basePreSaleAmount) |
| `QuotePreSaleAmount` | [`Double`](../../doc/models/precision.md) | Optional | Quote pre-sale amount | Double getQuotePreSaleAmount() | setQuotePreSaleAmount(Double quotePreSaleAmount) |
| `QuotePublicSaleCurrency` | `String` | Optional | Quote public sale currency | String getQuotePublicSaleCurrency() | setQuotePublicSaleCurrency(String quotePublicSaleCurrency) |
| `BasePublicSaleAmount` | [`Double`](../../doc/models/precision.md) | Optional | Base public sale amount | Double getBasePublicSaleAmount() | setBasePublicSaleAmount(Double basePublicSaleAmount) |
| `QuotePublicSaleAmount` | [`Double`](../../doc/models/precision.md) | Optional | Quote public sale amount | Double getQuotePublicSaleAmount() | setQuotePublicSaleAmount(Double quotePublicSaleAmount) |
| `AcceptingCurrencies` | `String` | Optional | Accepting currencies | String getAcceptingCurrencies() | setAcceptingCurrencies(String acceptingCurrencies) |
| `CountryOrigin` | `String` | Optional | Country of origin | String getCountryOrigin() | setCountryOrigin(String countryOrigin) |
| `PreSaleStartDate` | `String` | Optional | Pre-sale start date | String getPreSaleStartDate() | setPreSaleStartDate(String preSaleStartDate) |
| `PreSaleEndDate` | `String` | Optional | Pre-sale end date | String getPreSaleEndDate() | setPreSaleEndDate(String preSaleEndDate) |
| `WhitelistUrl` | `String` | Optional | Whitelist URL | String getWhitelistUrl() | setWhitelistUrl(String whitelistUrl) |
| `WhitelistStartDate` | `String` | Optional | Whitelist start date | String getWhitelistStartDate() | setWhitelistStartDate(String whitelistStartDate) |
| `WhitelistEndDate` | `String` | Optional | Whitelist end date | String getWhitelistEndDate() | setWhitelistEndDate(String whitelistEndDate) |
| `BountyDetailUrl` | `String` | Optional | Bounty detail URL | String getBountyDetailUrl() | setBountyDetailUrl(String bountyDetailUrl) |
| `AmountForSale` | [`Double`](../../doc/models/precision.md) | Optional | Amount for sale | Double getAmountForSale() | setAmountForSale(Double amountForSale) |
| `KycRequired` | `Boolean` | Optional | KYC required | Boolean getKycRequired() | setKycRequired(Boolean kycRequired) |
| `WhitelistAvailable` | `Boolean` | Optional | Whitelist available | Boolean getWhitelistAvailable() | setWhitelistAvailable(Boolean whitelistAvailable) |
| `PreSaleAvailable` | `Boolean` | Optional | Pre-sale available | Boolean getPreSaleAvailable() | setPreSaleAvailable(Boolean preSaleAvailable) |
| `PreSaleEnded` | `Boolean` | Optional | Pre-sale ended | Boolean getPreSaleEnded() | setPreSaleEnded(Boolean preSaleEnded) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.IcoData;
import java.io.IOException;
import java.util.LinkedHashMap;

IcoData icoData = new IcoData.Builder()
    .icoStartDate("ico_start_date8")
    .icoEndDate("ico_end_date4")
    .shortDesc("short_desc2")
    .description("description0")
    .links(new LinkedHashMap<String, String>() {{
        put("key0", "links6");
    }})
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

