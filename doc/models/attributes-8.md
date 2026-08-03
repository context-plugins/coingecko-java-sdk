
# Attributes 8

*This model accepts additional fields of type Object.*

## Structure

`Attributes8`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BaseTokenAddress` | `String` | Optional | Base token contract address | String getBaseTokenAddress() | setBaseTokenAddress(String baseTokenAddress) |
| `QuoteTokenAddress` | `String` | Optional | Quote token contract address | String getQuoteTokenAddress() | setQuoteTokenAddress(String quoteTokenAddress) |
| `QuoteTokenAddresses` | `List<String>` | Optional | Quote token contract addresses, present for pools with more than 2 tokens | List<String> getQuoteTokenAddresses() | setQuoteTokenAddresses(List<String> quoteTokenAddresses) |
| `SentimentVotePositivePercentage` | [`Double`](../../doc/models/precision.md) | Optional | GeckoTerminal community positive sentiment vote percentage | Double getSentimentVotePositivePercentage() | setSentimentVotePositivePercentage(Double sentimentVotePositivePercentage) |
| `SentimentVoteNegativePercentage` | [`Double`](../../doc/models/precision.md) | Optional | GeckoTerminal community negative sentiment vote percentage | Double getSentimentVoteNegativePercentage() | setSentimentVoteNegativePercentage(Double sentimentVoteNegativePercentage) |
| `CommunitySusReport` | `Integer` | Optional | GeckoTerminal community suspicious reports count | Integer getCommunitySusReport() | setCommunitySusReport(Integer communitySusReport) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes8;
import java.io.IOException;
import java.util.Arrays;

Attributes8 attributes8 = new Attributes8.Builder()
    .baseTokenAddress("base_token_address8")
    .quoteTokenAddress("quote_token_address2")
    .quoteTokenAddresses(Arrays.asList(
        "quote_token_addresses9",
        "quote_token_addresses0"
    ))
    .sentimentVotePositivePercentage(162.76D)
    .sentimentVoteNegativePercentage(222.78D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

