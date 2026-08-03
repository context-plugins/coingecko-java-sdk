
# Derivatives Ticker

*This model accepts additional fields of type Object.*

## Structure

`DerivativesTicker`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Market` | `String` | Required | Derivative market name | String getMarket() | setMarket(String market) |
| `Symbol` | `String` | Required | Derivative ticker symbol | String getSymbol() | setSymbol(String symbol) |
| `IndexId` | `String` | Required | Derivative underlying asset | String getIndexId() | setIndexId(String indexId) |
| `Price` | `String` | Required | Derivative ticker price | String getPrice() | setPrice(String price) |
| `PricePercentageChange24H` | [`double`](../../doc/models/precision.md) | Required | Derivative ticker price percentage change in 24 hours | double getPricePercentageChange24H() | setPricePercentageChange24H(double pricePercentageChange24H) |
| `ContractType` | `String` | Required | Derivative contract type | String getContractType() | setContractType(String contractType) |
| `Index` | [`double`](../../doc/models/precision.md) | Required | Derivative underlying asset price | double getIndex() | setIndex(double index) |
| `Basis` | [`double`](../../doc/models/precision.md) | Required | Difference of derivative price and index price | double getBasis() | setBasis(double basis) |
| `Spread` | [`double`](../../doc/models/precision.md) | Required | Derivative bid-ask spread | double getSpread() | setSpread(double spread) |
| `FundingRate` | [`double`](../../doc/models/precision.md) | Required | Derivative funding rate | double getFundingRate() | setFundingRate(double fundingRate) |
| `OpenInterest` | [`double`](../../doc/models/precision.md) | Required | Derivative open interest | double getOpenInterest() | setOpenInterest(double openInterest) |
| `Volume24H` | [`double`](../../doc/models/precision.md) | Required | Derivative trading volume in 24 hours | double getVolume24H() | setVolume24H(double volume24H) |
| `LastTradedAt` | [`double`](../../doc/models/precision.md) | Required | Derivative last traded time in UNIX timestamp | double getLastTradedAt() | setLastTradedAt(double lastTradedAt) |
| `ExpiredAt` | [`Double`](../../doc/models/precision.md) | Required | Derivative expiry time in UNIX timestamp | Double getExpiredAt() | setExpiredAt(Double expiredAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.DerivativesTicker;
import java.io.IOException;

DerivativesTicker derivativesTicker = new DerivativesTicker.Builder(
    "market6",
    "symbol8",
    "index_id8",
    "price4",
    93.9D,
    "contract_type4",
    59.38D,
    188.56D,
    29.56D,
    102.52D,
    99.34D,
    122.52D,
    149.68D,
    227.26D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

