
# Attributes 3

*This model accepts additional fields of type Object.*

## Structure

`Attributes3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BlockNumber` | `int` | Required | Block number of the trade | int getBlockNumber() | setBlockNumber(int blockNumber) |
| `TxHash` | `String` | Required | Transaction hash | String getTxHash() | setTxHash(String txHash) |
| `TxFromAddress` | `String` | Required | Transaction sender address | String getTxFromAddress() | setTxFromAddress(String txFromAddress) |
| `FromTokenAmount` | `String` | Required | Amount of token sent | String getFromTokenAmount() | setFromTokenAmount(String fromTokenAmount) |
| `ToTokenAmount` | `String` | Required | Amount of token received | String getToTokenAmount() | setToTokenAmount(String toTokenAmount) |
| `PriceFromInCurrencyToken` | `String` | Required | Price of from-token in currency token | String getPriceFromInCurrencyToken() | setPriceFromInCurrencyToken(String priceFromInCurrencyToken) |
| `PriceToInCurrencyToken` | `String` | Required | Price of to-token in currency token | String getPriceToInCurrencyToken() | setPriceToInCurrencyToken(String priceToInCurrencyToken) |
| `PriceFromInUsd` | `String` | Required | Price of from-token in USD | String getPriceFromInUsd() | setPriceFromInUsd(String priceFromInUsd) |
| `PriceToInUsd` | `String` | Required | Price of to-token in USD | String getPriceToInUsd() | setPriceToInUsd(String priceToInUsd) |
| `BlockTimestamp` | `String` | Required | Block timestamp | String getBlockTimestamp() | setBlockTimestamp(String blockTimestamp) |
| `Kind` | `String` | Required | Trade kind (buy or sell) | String getKind() | setKind(String kind) |
| `VolumeInUsd` | `String` | Required | Trade volume in USD | String getVolumeInUsd() | setVolumeInUsd(String volumeInUsd) |
| `FromTokenAddress` | `String` | Required | From-token contract address | String getFromTokenAddress() | setFromTokenAddress(String fromTokenAddress) |
| `ToTokenAddress` | `String` | Required | To-token contract address | String getToTokenAddress() | setToTokenAddress(String toTokenAddress) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes3;
import java.io.IOException;

Attributes3 attributes3 = new Attributes3.Builder(
    172,
    "tx_hash4",
    "tx_from_address8",
    "from_token_amount0",
    "to_token_amount6",
    "price_from_in_currency_token4",
    "price_to_in_currency_token2",
    "price_from_in_usd8",
    "price_to_in_usd2",
    "block_timestamp8",
    "kind6",
    "volume_in_usd4",
    "from_token_address2",
    "to_token_address2"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

