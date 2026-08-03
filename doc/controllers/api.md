# API

```java
Api api = client.getApi();
```

## Class Name

`Api`

## Methods

* [Ping-Server](../../doc/controllers/api.md#ping-server)
* [Simple-Price](../../doc/controllers/api.md#simple-price)
* [Search-Data](../../doc/controllers/api.md#search-data)
* [Simple-Supported-Currencies](../../doc/controllers/api.md#simple-supported-currencies)
* [Simple-Token-Price](../../doc/controllers/api.md#simple-token-price)
* [Coins-List](../../doc/controllers/api.md#coins-list)
* [Coins-Id](../../doc/controllers/api.md#coins-id)
* [Coins-Markets](../../doc/controllers/api.md#coins-markets)
* [Coins-Id-Tickers](../../doc/controllers/api.md#coins-id-tickers)
* [Coins-Id-History](../../doc/controllers/api.md#coins-id-history)
* [Coins-Id-Market-Chart](../../doc/controllers/api.md#coins-id-market-chart)
* [Coins-Id-Market-Chart-Range](../../doc/controllers/api.md#coins-id-market-chart-range)
* [Coins-Id-Ohlc](../../doc/controllers/api.md#coins-id-ohlc)
* [Coins-Contract-Address](../../doc/controllers/api.md#coins-contract-address)
* [Contract-Address-Market-Chart](../../doc/controllers/api.md#contract-address-market-chart)
* [Contract-Address-Market-Chart-Range](../../doc/controllers/api.md#contract-address-market-chart-range)
* [Asset-Platforms-List](../../doc/controllers/api.md#asset-platforms-list)
* [Token-Lists](../../doc/controllers/api.md#token-lists)
* [Coins-Categories-List](../../doc/controllers/api.md#coins-categories-list)
* [Coins-Categories](../../doc/controllers/api.md#coins-categories)
* [Exchanges](../../doc/controllers/api.md#exchanges)
* [Exchanges-List](../../doc/controllers/api.md#exchanges-list)
* [Exchanges-Id](../../doc/controllers/api.md#exchanges-id)
* [Exchanges-Id-Tickers](../../doc/controllers/api.md#exchanges-id-tickers)
* [Exchanges-Id-Volume-Chart](../../doc/controllers/api.md#exchanges-id-volume-chart)
* [Derivatives-Tickers](../../doc/controllers/api.md#derivatives-tickers)
* [Derivatives-Exchanges](../../doc/controllers/api.md#derivatives-exchanges)
* [Derivatives-Exchanges-Id](../../doc/controllers/api.md#derivatives-exchanges-id)
* [Derivatives-Exchanges-List](../../doc/controllers/api.md#derivatives-exchanges-list)
* [Entities-List](../../doc/controllers/api.md#entities-list)
* [Companies-Public-Treasury](../../doc/controllers/api.md#companies-public-treasury)
* [Public-Treasury-Entity](../../doc/controllers/api.md#public-treasury-entity)
* [Public-Treasury-Entity-Chart](../../doc/controllers/api.md#public-treasury-entity-chart)
* [Public-Treasury-Transaction-History](../../doc/controllers/api.md#public-treasury-transaction-history)
* [Nfts-List](../../doc/controllers/api.md#nfts-list)
* [Nfts-Id](../../doc/controllers/api.md#nfts-id)
* [Nfts-Contract-Address](../../doc/controllers/api.md#nfts-contract-address)
* [Exchange-Rates](../../doc/controllers/api.md#exchange-rates)
* [Trending-Search](../../doc/controllers/api.md#trending-search)
* [Crypto-Global](../../doc/controllers/api.md#crypto-global)
* [Global-Defi](../../doc/controllers/api.md#global-defi)
* [Pool-Address](../../doc/controllers/api.md#pool-address)
* [Trending-Pools-List](../../doc/controllers/api.md#trending-pools-list)
* [Trending-Pools-Network](../../doc/controllers/api.md#trending-pools-network)
* [Top-Pools-Network](../../doc/controllers/api.md#top-pools-network)
* [Top-Pools-Dex](../../doc/controllers/api.md#top-pools-dex)
* [Top-Pools-Contract-Address](../../doc/controllers/api.md#top-pools-contract-address)
* [Token-Data-Contract-Address](../../doc/controllers/api.md#token-data-contract-address)
* [Tokens-Data-Contract-Addresses](../../doc/controllers/api.md#tokens-data-contract-addresses)
* [Token-Info-Contract-Address](../../doc/controllers/api.md#token-info-contract-address)
* [Pool-Token-Info-Contract-Address](../../doc/controllers/api.md#pool-token-info-contract-address)
* [Tokens-Info-Recent-Updated](../../doc/controllers/api.md#tokens-info-recent-updated)
* [Pool-Ohlcv-Contract-Address](../../doc/controllers/api.md#pool-ohlcv-contract-address)
* [Pool-Trades-Contract-Address](../../doc/controllers/api.md#pool-trades-contract-address)
* [Latest-Pools-List](../../doc/controllers/api.md#latest-pools-list)
* [Latest-Pools-Network](../../doc/controllers/api.md#latest-pools-network)
* [Pools-Addresses](../../doc/controllers/api.md#pools-addresses)
* [Search-Pools](../../doc/controllers/api.md#search-pools)
* [Onchain-Simple-Price](../../doc/controllers/api.md#onchain-simple-price)
* [Networks-List](../../doc/controllers/api.md#networks-list)
* [Dexes-List](../../doc/controllers/api.md#dexes-list)


# Ping-Server

To check the API server status

```java
CompletableFuture<ApiResponse<PingServer>> pingServerAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: Server status

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PingServer`](../../doc/models/ping-server.md).

## Example Usage

```java
api.pingServerAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "gecko_says": "(V3) To the Moon!"
}
```


# Simple-Price

To query the prices of one or more coins by using their unique Coin API IDs, symbols, or names

```java
CompletableFuture<ApiResponse<Map<String, SimplePrice>>> simplePriceAsync(
    final String vsCurrencies,
    final String ids,
    final String names,
    final String symbols,
    final IncludeTokens includeTokens,
    final Boolean includeMarketCap,
    final Boolean include24HrVol,
    final Boolean include24HrChange,
    final Boolean includeLastUpdatedAt,
    final Precision precision)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vsCurrencies` | `String` | Query, Required | Target currency of coins, comma-separated if querying more than 1 currency.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies) |
| `ids` | `String` | Query, Optional | Coins' IDs, comma-separated if querying more than 1 coin.<br>*refers to [`/coins/list`](/reference/coins-list)<br><br>**Default**: `"bitcoin"` |
| `names` | `String` | Query, Optional | Coins' names, comma-separated if querying more than 1 coin.<br><br>**Default**: `"Bitcoin"` |
| `symbols` | `String` | Query, Optional | Coins' symbols, comma-separated if querying more than 1 coin.<br><br>**Default**: `"btc"` |
| `includeTokens` | [`IncludeTokens`](../../doc/models/include-tokens.md) | Query, Optional | For `symbols` lookups, specify `all` to include all matching tokens.<br>Default `top` returns top-ranked tokens by market cap or volume. |
| `includeMarketCap` | `Boolean` | Query, Optional | Include market capitalization.<br>Default: false |
| `include24HrVol` | `Boolean` | Query, Optional | Include 24-hour trading volume.<br>Default: false |
| `include24HrChange` | `Boolean` | Query, Optional | Include 24-hour change percentage.<br>Default: false |
| `includeLastUpdatedAt` | `Boolean` | Query, Optional | Include last updated price time as a UNIX timestamp.<br>Default: false |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal places for currency price value |

## Response Type

**200**: Coin prices

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Map<String, SimplePrice>`](../../doc/models/simple-price.md).

## Example Usage

```java
String vsCurrencies = "usd";
String ids = "bitcoin";
String names = "Bitcoin";
String symbols = "btc";

api.simplePriceAsync(vsCurrencies, ids, names, symbols, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "bitcoin": {
    "usd": 76975,
    "usd_market_cap": 1542226908349.8406,
    "usd_24h_vol": 29096603418.89408,
    "usd_24h_change": -1.4093297098441402,
    "last_updated_at": 1779092258
  }
}
```


# Search-Data

To search for coins, categories and markets listed on CoinGecko

```java
CompletableFuture<ApiResponse<Search>> searchDataAsync(
    final String query)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query` | `String` | Query, Required | Search query |

## Response Type

**200**: Search results

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Search`](../../doc/models/search.md).

## Example Usage

```java
String query = "query0";

api.searchDataAsync(query).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "coins": [
    {
      "id": "ethereum",
      "name": "Ethereum",
      "api_symbol": "ethereum",
      "symbol": "ETH",
      "market_cap_rank": 2,
      "thumb": "https://coin-images.coingecko.com/coins/images/279/thumb/ethereum.png",
      "large": "https://coin-images.coingecko.com/coins/images/279/large/ethereum.png"
    }
  ],
  "exchanges": [
    {
      "id": "uniswap_v3",
      "name": "Uniswap V3 (Ethereum)",
      "market_type": "spot",
      "thumb": "https://coin-images.coingecko.com/markets/images/665/thumb/uniswap-v3.png",
      "large": "https://coin-images.coingecko.com/markets/images/665/large/uniswap-v3.png"
    }
  ],
  "icos": [],
  "categories": [
    {
      "id": "ethereum-pos-iou",
      "name": "Ethereum PoS IOU"
    }
  ],
  "nfts": [
    {
      "id": "ens-ethereum-name-service",
      "name": "ENS: Ethereum Name Service",
      "symbol": "ENS",
      "thumb": "https://coin-images.coingecko.com/nft_contracts/images/373/thumb/ens-ethereum-name-service.png"
    }
  ]
}
```


# Simple-Supported-Currencies

To query all the supported currencies on CoinGecko

```java
CompletableFuture<ApiResponse<List<String>>> simpleSupportedCurrenciesAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: List of supported currencies

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `List<String>`.

## Example Usage

```java
api.simpleSupportedCurrenciesAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response

```
[
  "btc",
  "eth",
  "ltc",
  "bch",
  "bnb",
  "eos",
  "xrp",
  "xlm",
  "link",
  "dot",
  "yfi",
  "sol",
  "usd",
  "aed",
  "ars",
  "aud",
  "bdt",
  "bhd",
  "bmd",
  "brl",
  "cad",
  "chf",
  "clp",
  "cny",
  "czk",
  "dkk",
  "eur",
  "gbp",
  "gel",
  "hkd",
  "huf",
  "idr",
  "ils",
  "inr",
  "jpy",
  "krw",
  "kwd",
  "lkr",
  "mmk",
  "mxn",
  "myr",
  "ngn",
  "nok",
  "nzd",
  "php",
  "pkr",
  "pln",
  "rub",
  "sar",
  "sek",
  "sgd",
  "thb",
  "try",
  "twd",
  "uah",
  "vef",
  "vnd",
  "zar",
  "xdr",
  "xag",
  "xau",
  "bits",
  "sats"
]
```


# Simple-Token-Price

To query one or more token prices by using their token contract addresses

```java
CompletableFuture<ApiResponse<Map<String, SimplePrice>>> simpleTokenPriceAsync(
    final String id,
    final String contractAddresses,
    final String vsCurrencies,
    final Boolean includeMarketCap,
    final Boolean include24HrVol,
    final Boolean include24HrChange,
    final Boolean includeLastUpdatedAt,
    final Precision precision)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Asset platform's ID.<br>*refers to [`/asset_platforms`](/reference/asset-platforms-list) |
| `contractAddresses` | `String` | Query, Required | Token contract addresses, comma-separated if querying more than 1 token |
| `vsCurrencies` | `String` | Query, Required | Target currency of coins, comma-separated if querying more than 1 currency.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies) |
| `includeMarketCap` | `Boolean` | Query, Optional | Include market capitalization.<br>Default: false |
| `include24HrVol` | `Boolean` | Query, Optional | Include 24-hour trading volume.<br>Default: false |
| `include24HrChange` | `Boolean` | Query, Optional | Include 24-hour change percentage.<br>Default: false |
| `includeLastUpdatedAt` | `Boolean` | Query, Optional | Include last updated price time as a UNIX timestamp.<br>Default: false |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal places for currency price value |

## Response Type

**200**: Token prices

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Map<String, SimplePrice>`](../../doc/models/simple-price.md).

## Example Usage

```java
String id = "ethereum";
String contractAddresses = "0x2260fac5e5542a773aa44fbcfedf7c193bc2c599";
String vsCurrencies = "usd";

api.simpleTokenPriceAsync(id, contractAddresses, vsCurrencies, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "0x2260fac5e5542a773aa44fbcfedf7c193bc2c599": {
    "usd": 76721,
    "usd_market_cap": 9008047197.715635,
    "usd_24h_vol": 181232010.10689816,
    "usd_24h_change": -1.6069562341774564,
    "last_updated_at": 1779094527
  }
}
```


# Coins-List

To query all the supported coins on CoinGecko with coin ID, name and symbol

```java
CompletableFuture<ApiResponse<List<CoinsList>>> coinsListAsync(
    final Boolean includePlatform,
    final Status status)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `includePlatform` | `Boolean` | Query, Optional | Include platform and token's contract addresses.<br>Default: false |
| `status` | [`Status`](../../doc/models/status.md) | Query, Optional | Filter by status of coins.<br>Default: active |

## Response Type

**200**: List of coins

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<CoinsList>`](../../doc/models/coins-list.md).

## Example Usage

```java
api.coinsListAsync(null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "official-trump",
    "symbol": "trump",
    "name": "Official Trump",
    "platforms": {
      "solana": "6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN"
    }
  },
  {
    "id": "ondo-finance",
    "symbol": "ondo",
    "name": "Ondo",
    "platforms": {
      "ethereum": "0xfaba6f8e4a5e8ab82f62fe7c39859fa577269be3"
    }
  }
]
```


# Coins-Id

To query all the metadata (image, websites, socials, description, contract address, etc.) and market data (price, ATH, exchange tickers, etc.) of a coin based on a particular coin ID

```java
CompletableFuture<ApiResponse<CoinsId>> coinsIdAsync(
    final String id,
    final Boolean localization,
    final Boolean tickers,
    final Boolean marketData,
    final Boolean communityData,
    final Boolean developerData,
    final Boolean sparkline,
    final Boolean includeCategoriesDetails,
    final DexPairFormat dexPairFormat)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Coin ID.<br>*refers to [`/coins/list`](/reference/coins-list) |
| `localization` | `Boolean` | Query, Optional | Include all localized languages in the response.<br>Default: true |
| `tickers` | `Boolean` | Query, Optional | Include tickers data.<br>Default: true |
| `marketData` | `Boolean` | Query, Optional | Include market data.<br>Default: true |
| `communityData` | `Boolean` | Query, Optional | Include community data.<br>Default: true |
| `developerData` | `Boolean` | Query, Optional | Include developer data.<br>Default: true |
| `sparkline` | `Boolean` | Query, Optional | Include sparkline 7-day data.<br>Default: false |
| `includeCategoriesDetails` | `Boolean` | Query, Optional | Include categories details.<br>Default: false |
| `dexPairFormat` | [`DexPairFormat`](../../doc/models/dex-pair-format.md) | Query, Optional | Set to `symbol` to display DEX pair base and target as symbols.<br>Default: `contract_address` |

## Response Type

**200**: Coin data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsId`](../../doc/models/coins-id.md).

## Example Usage

```java
String id = "bitcoin";

api.coinsIdAsync(id, null, null, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "id": "bitcoin",
  "symbol": "btc",
  "name": "Bitcoin",
  "web_slug": "bitcoin",
  "asset_platform_id": null,
  "platforms": {
    "": ""
  },
  "detail_platforms": {
    "": {
      "decimal_place": null,
      "contract_address": ""
    }
  },
  "block_time_in_minutes": 10,
  "hashing_algorithm": "SHA-256",
  "categories": [
    "Cryptocurrency",
    "Layer 1 (L1)"
  ],
  "preview_listing": false,
  "public_notice": null,
  "additional_notices": [],
  "has_supply_breakdown": false,
  "description": {
    "en": "Bitcoin is the first successful internet money based on peer-to-peer technology..."
  },
  "links": {
    "homepage": [
      "http://www.bitcoin.org",
      "",
      ""
    ],
    "whitepaper": "https://bitcoin.org/bitcoin.pdf",
    "blockchain_site": [
      "https://mempool.space/",
      "https://blockchair.com/bitcoin/"
    ],
    "official_forum_url": [
      "https://bitcointalk.org/"
    ],
    "chat_url": [
      ""
    ],
    "announcement_url": [
      "",
      ""
    ],
    "snapshot_url": null,
    "twitter_screen_name": "bitcoin",
    "facebook_username": "bitcoins",
    "bitcointalk_thread_identifier": null,
    "telegram_channel_identifier": "",
    "subreddit_url": "https://www.reddit.com/r/Bitcoin/",
    "repos_url": {
      "github": [
        "https://github.com/bitcoin/bitcoin",
        "https://github.com/bitcoin/bips"
      ],
      "bitbucket": []
    }
  },
  "image": {
    "thumb": "https://assets.coingecko.com/coins/images/1/thumb/bitcoin.png?1696501400",
    "small": "https://assets.coingecko.com/coins/images/1/small/bitcoin.png?1696501400",
    "large": "https://assets.coingecko.com/coins/images/1/large/bitcoin.png?1696501400"
  },
  "country_origin": "",
  "genesis_date": "2009-01-03",
  "sentiment_votes_up_percentage": 84.07,
  "sentiment_votes_down_percentage": 15.93,
  "watchlist_portfolio_users": 1541900,
  "market_cap_rank": 1,
  "market_cap_rank_with_rehypothecated": 1,
  "status_updates": [],
  "last_updated": "2024-04-07T15:24:51.021Z",
  "market_data": {
    "current_price": {
      "btc": 1,
      "eur": 64375,
      "usd": 69840
    },
    "total_value_locked": null,
    "mcap_to_tvl_ratio": null,
    "fdv_to_tvl_ratio": null,
    "roi": null,
    "ath": {
      "btc": 1.003301,
      "eur": 67405,
      "usd": 73738
    },
    "ath_change_percentage": {
      "btc": -0.32896,
      "eur": -4.54383,
      "usd": -5.33399
    },
    "ath_date": {
      "btc": "2024-03-02T16:05:19.446Z",
      "eur": "2024-03-14T07:10:36.635Z",
      "usd": "2024-03-14T07:10:36.635Z"
    },
    "atl": {
      "btc": 0.99895134,
      "eur": 51.3,
      "usd": 67.81
    },
    "atl_change_percentage": {
      "btc": 0.10408,
      "eur": 125385.41242,
      "usd": 102882.36498
    },
    "atl_date": {
      "btc": "2019-10-21T00:00:00.000Z",
      "eur": "2013-07-05T00:00:00.000Z",
      "usd": "2013-07-06T00:00:00.000Z"
    },
    "market_cap": {
      "btc": 19675377,
      "eur": 1265825267281,
      "usd": 1373296629498
    },
    "fully_diluted_valuation": {
      "btc": 21000000,
      "eur": 1351831155,
      "usd": 1466577759
    },
    "market_cap_fdv_ratio": 1,
    "market_cap_rank": 1,
    "outstanding_token_value_usd": null,
    "market_cap_rank_with_rehypothecated": 1,
    "total_volume": {
      "btc": 270165,
      "eur": 17368113665,
      "usd": 18867210007
    },
    "high_24h": {
      "btc": 1,
      "eur": 64343,
      "usd": 69805
    },
    "low_24h": {
      "btc": 1,
      "eur": 62695,
      "usd": 67985
    },
    "price_change_24h": 1619,
    "price_change_percentage_24h": 2.37311,
    "price_change_percentage_7d": -0.89706,
    "price_change_percentage_14d": 6.36178,
    "price_change_percentage_30d": 1.81171,
    "price_change_percentage_60d": 62.54292,
    "price_change_percentage_200d": 157.51875,
    "price_change_percentage_1y": 149.76989,
    "market_cap_change_24h": 31172487848,
    "market_cap_change_percentage_24h": 2.32219,
    "price_change_24h_in_currency": {
      "btc": 0,
      "eur": 1461.64,
      "usd": 1618.95
    },
    "price_change_percentage_1h_in_currency": {
      "btc": 0,
      "eur": 0.79523,
      "usd": 0.79523
    },
    "price_change_percentage_24h_in_currency": {
      "btc": 0,
      "eur": 2.32219,
      "usd": 2.37311
    },
    "price_change_percentage_7d_in_currency": {
      "btc": 0,
      "eur": -1.01955,
      "usd": -0.89706
    },
    "price_change_percentage_14d_in_currency": {
      "btc": 0,
      "eur": 5.84662,
      "usd": 6.36178
    },
    "price_change_percentage_30d_in_currency": {
      "btc": 0,
      "eur": 2.28048,
      "usd": 1.81171
    },
    "price_change_percentage_60d_in_currency": {
      "btc": 0,
      "eur": 60.98834,
      "usd": 62.54292
    },
    "price_change_percentage_200d_in_currency": {
      "btc": 0,
      "eur": 148.68948,
      "usd": 157.51875
    },
    "price_change_percentage_1y_in_currency": {
      "btc": 0,
      "eur": 138.20277,
      "usd": 149.76989
    },
    "market_cap_change_24h_in_currency": {
      "btc": -49432,
      "eur": 28668703539,
      "usd": 31172487848
    },
    "market_cap_change_percentage_24h_in_currency": {
      "btc": -0.25084,
      "eur": 2.31801,
      "usd": 2.32219
    },
    "total_supply": 21000000,
    "max_supply": 21000000,
    "max_supply_infinite": false,
    "circulating_supply": 19675377,
    "outstanding_supply": null,
    "last_updated": "2024-04-07T15:24:51.021Z"
  },
  "community_data": {
    "facebook_likes": null,
    "reddit_average_posts_48h": 7.333,
    "reddit_average_comments_48h": 384.667,
    "reddit_subscribers": 6127543,
    "reddit_accounts_active_48h": 3498,
    "telegram_channel_user_count": null
  },
  "developer_data": {
    "forks": 36433,
    "stars": 76697,
    "subscribers": 3967,
    "total_issues": 7743,
    "closed_issues": 7379,
    "pull_requests_merged": 11204,
    "pull_request_contributors": 829,
    "code_additions_deletions_4_weeks": {
      "additions": 1264,
      "deletions": -1314
    },
    "commit_count_4_weeks": 108,
    "last_4_weeks_commit_activity_series": [
      0,
      3,
      2,
      0,
      1,
      0,
      0
    ]
  },
  "tickers": [
    {
      "base": "BTC",
      "target": "USDT",
      "market": {
        "name": "Binance",
        "identifier": "binance",
        "has_trading_incentive": false
      },
      "last": 69816,
      "volume": 19988.82111,
      "converted_last": {
        "btc": 0.99999255,
        "eth": 20.441016,
        "usd": 69835
      },
      "converted_volume": {
        "btc": 19783,
        "eth": 404380,
        "usd": 1381537193
      },
      "trust_score": null,
      "bid_ask_spread_percentage": 0.010014,
      "timestamp": "2024-04-07T15:23:02+00:00",
      "last_traded_at": "2024-04-07T15:23:02+00:00",
      "last_fetch_at": "2024-04-07T15:24:00+00:00",
      "is_anomaly": false,
      "is_stale": false,
      "trade_url": "https://www.binance.com/en/trade/BTC_USDT?ref=37754157",
      "token_info_url": null,
      "coin_id": "bitcoin",
      "target_coin_id": "tether",
      "coin_mcap_usd": 230926944910.5146
    }
  ]
}
```


# Coins-Markets

To query all the supported coins with price, market cap, volume and market related data

```java
CompletableFuture<ApiResponse<List<CoinsMarket>>> coinsMarketsAsync(
    final String vsCurrency,
    final String ids,
    final String names,
    final String symbols,
    final IncludeTokens includeTokens,
    final String category,
    final Order order,
    final Integer perPage,
    final Integer page,
    final Boolean sparkline,
    final String priceChangePercentage,
    final Locale locale,
    final Precision precision,
    final Boolean includeRehypothecated)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vsCurrency` | `String` | Query, Required | Target currency of coins and market data.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies) |
| `ids` | `String` | Query, Optional | Coins' IDs, comma-separated if querying more than 1 coin.<br>*refers to [`/coins/list`](/reference/coins-list)<br><br>**Default**: `"bitcoin"` |
| `names` | `String` | Query, Optional | Coins' names, comma-separated if querying more than 1 coin.<br><br>**Default**: `"Bitcoin"` |
| `symbols` | `String` | Query, Optional | Coins' symbols, comma-separated if querying more than 1 coin.<br><br>**Default**: `"btc"` |
| `includeTokens` | [`IncludeTokens`](../../doc/models/include-tokens.md) | Query, Optional | For `symbols` lookups, specify `all` to include all matching tokens.<br>Default `top` returns top-ranked tokens by market cap or volume. |
| `category` | `String` | Query, Optional | Filter based on coins' category.<br>*refers to [`/coins/categories/list`](/reference/coins-categories-list) |
| `order` | [`Order`](../../doc/models/order.md) | Query, Optional | Sort result by field.<br>Default: market_cap_desc |
| `perPage` | `Integer` | Query, Optional | Total results per page.<br>Default: 100<br>Valid values: 1...250 |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default: 1 |
| `sparkline` | `Boolean` | Query, Optional | Include sparkline 7-day data.<br>Default: false |
| `priceChangePercentage` | `String` | Query, Optional | Include price change percentage timeframe, comma-separated if querying more than 1 timeframe.<br>Valid values: `1h`, `24h`, `7d`, `14d`, `30d`, `200d`, `1y` |
| `locale` | [`Locale`](../../doc/models/locale.md) | Query, Optional | Language background.<br>Default: en |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal places for currency price value |
| `includeRehypothecated` | `Boolean` | Query, Optional | Include rehypothecated tokens in results. When true, returns `market_cap_rank_with_rehypothecated` field.<br>Default: false |

## Response Type

**200**: List of coins with market data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<CoinsMarket>`](../../doc/models/coins-market.md).

## Example Usage

```java
String vsCurrency = "usd";
String ids = "bitcoin";
String names = "Bitcoin";
String symbols = "btc";

api.coinsMarketsAsync(vsCurrency, ids, names, symbols, null, null, null, null, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "bitcoin",
    "symbol": "btc",
    "name": "Bitcoin",
    "image": "https://coin-images.coingecko.com/coins/images/1/large/bitcoin.png?1696501400",
    "current_price": 77671,
    "market_cap": 1555886872303,
    "market_cap_rank": 1,
    "fully_diluted_valuation": 1555914058873,
    "total_volume": 33235034316,
    "high_24h": 78419,
    "low_24h": 76696,
    "price_change_24h": -747.3360347281705,
    "price_change_percentage_24h": -0.95302,
    "market_cap_change_24h": -15184401491.513184,
    "market_cap_change_percentage_24h": -0.9665,
    "circulating_supply": 20030493.0,
    "total_supply": 20030843.0,
    "max_supply": 21000000.0,
    "ath": 126080,
    "ath_change_percentage": -38.39571,
    "ath_date": "2025-10-06T18:57:42.558Z",
    "atl": 67.81,
    "atl_change_percentage": 114443.23093,
    "atl_date": "2013-07-06T00:00:00.000Z",
    "roi": null,
    "last_updated": "2026-05-18T12:49:21.599Z",
    "market_cap_rank_with_rehypothecated": 1,
    "sparkline_in_7d": {
      "price": [
        81045.84776489827,
        81001.73089268175,
        80898.20817826076
      ]
    },
    "price_change_percentage_1h_in_currency": 0.5823392426906319,
    "price_change_percentage_24h_in_currency": -0.9530164743774191,
    "price_change_percentage_7d_in_currency": -4.042267423689584,
    "price_change_percentage_14d_in_currency": -1.5720857443461431,
    "price_change_percentage_30d_in_currency": 1.9453890367549207,
    "price_change_percentage_200d_in_currency": -29.452371850925864,
    "price_change_percentage_1y_in_currency": -25.214612207475373
  }
]
```


# Coins-Id-Tickers

To query the coin tickers on both centralized exchange (CEX) and decentralized exchange (DEX) based on a particular coin ID

```java
CompletableFuture<ApiResponse<CoinsIdTickers>> coinsIdTickersAsync(
    final String id,
    final String exchangeIds,
    final Boolean includeExchangeLogo,
    final Integer page,
    final Order1 order,
    final Boolean depth,
    final DexPairFormat dexPairFormat)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Coin ID.<br>*refers to [`/coins/list`](/reference/coins-list) |
| `exchangeIds` | `String` | Query, Optional | Exchange ID.<br>*refers to [`/exchanges/list`](/reference/exchanges-list) |
| `includeExchangeLogo` | `Boolean` | Query, Optional | Include exchange logo.<br>Default: false |
| `page` | `Integer` | Query, Optional | Page through results |
| `order` | [`Order1`](../../doc/models/order-1.md) | Query, Optional | Sort the order of responses.<br>Default: trust_score_desc |
| `depth` | `Boolean` | Query, Optional | Include 2% orderbook depth, i.e. `cost_to_move_up_usd` and `cost_to_move_down_usd`.<br>Default: false |
| `dexPairFormat` | [`DexPairFormat`](../../doc/models/dex-pair-format.md) | Query, Optional | Set to `symbol` to display DEX pair base and target as symbols.<br>Default: `contract_address` |

## Response Type

**200**: Coin tickers

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsIdTickers`](../../doc/models/coins-id-tickers.md).

## Example Usage

```java
String id = "bitcoin";

api.coinsIdTickersAsync(id, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "name": "Bitcoin",
  "tickers": [
    {
      "base": "BTC",
      "target": "USDT",
      "market": {
        "name": "Binance",
        "identifier": "binance",
        "has_trading_incentive": false,
        "logo": "https://coin-images.coingecko.com/markets/images/52/small/binance.jpg?1706864274"
      },
      "last": 76894.07,
      "volume": 13786.06991,
      "cost_to_move_up_usd": 19320706.3958517,
      "cost_to_move_down_usd": 16360235.3694131,
      "converted_last": {
        "btc": 0.99664066,
        "eth": 36.004874,
        "usd": 76856
      },
      "converted_volume": {
        "btc": 13740,
        "eth": 496366,
        "usd": 1059536991
      },
      "trust_score": null,
      "bid_ask_spread_percentage": 0.010013,
      "timestamp": "2026-05-18T13:37:29+00:00",
      "last_traded_at": "2026-05-18T13:37:29+00:00",
      "last_fetch_at": "2026-05-18T13:37:29+00:00",
      "is_anomaly": false,
      "is_stale": false,
      "trade_url": "https://www.binance.com/en/trade/BTC_USDT?ref=37754157",
      "token_info_url": null,
      "coin_id": "bitcoin",
      "target_coin_id": "tether",
      "coin_mcap_usd": 1544810408447.1313
    }
  ]
}
```


# Coins-Id-History

To query the historical data (price, market cap, 24hrs volume, etc.) at a given date for a coin based on a particular coin ID

```java
CompletableFuture<ApiResponse<CoinsIdHistory>> coinsIdHistoryAsync(
    final String id,
    final String date,
    final Boolean localization)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Coin ID.<br>*refers to [`/coins/list`](/reference/coins-list). |
| `date` | `String` | Query, Required | The date of data snapshot.<br>Format: `dd-mm-yyyy` |
| `localization` | `Boolean` | Query, Optional | Include all the localized languages in response.<br>Default: true |

## Response Type

**200**: Coin historical data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsIdHistory`](../../doc/models/coins-id-history.md).

## Example Usage

```java
String id = "bitcoin";
String date = "30-12-2025";

api.coinsIdHistoryAsync(id, date, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "id": "bitcoin",
  "symbol": "btc",
  "name": "Bitcoin",
  "localization": {
    "en": "Bitcoin",
    "zh": "比特币",
    "zh-tw": "比特幣",
    "de": "Bitcoin",
    "fr": "Bitcoin",
    "es": "Bitcoin",
    "ja": "ビットコイン",
    "id": "Bitcoin",
    "ru": "Биткоин",
    "ko": "비트코인",
    "ar": "بيتكوين",
    "th": "บิตคอยน์",
    "vi": "Bitcoin",
    "it": "Bitcoin",
    "pl": "Bitcoin",
    "tr": "Bitcoin",
    "hu": "Bitcoin",
    "nl": "Bitcoin",
    "ro": "Bitcoin",
    "sv": "Bitcoin",
    "cs": "Bitcoin",
    "da": "Bitcoin",
    "el": "Bitcoin",
    "hi": "Bitcoin",
    "no": "Bitcoin",
    "sk": "Bitcoin",
    "uk": "Bitcoin",
    "he": "Bitcoin",
    "fi": "Bitcoin",
    "bg": "Bitcoin",
    "hr": "Bitcoin",
    "lt": "Bitcoin",
    "sl": "Bitcoin",
    "pt": "Bitcoin"
  },
  "image": {
    "thumb": "https://coin-images.coingecko.com/coins/images/1/thumb/bitcoin.png?1696501400",
    "small": "https://coin-images.coingecko.com/coins/images/1/small/bitcoin.png?1696501400"
  },
  "market_data": {
    "current_price": {
      "aed": 155021.01870663263,
      "ars": 34223222.03038811,
      "aud": 61961.64079464181,
      "bch": 162.9444394169128,
      "bdt": 4640974.295329716,
      "bhd": 15935.706731619232,
      "bmd": 42208.202176186474,
      "bnb": 135.24654224991627,
      "brl": 204813.86598107114,
      "btc": 1.0,
      "cad": 55925.65684243621,
      "chf": 35496.88698916195,
      "clp": 37196103.56833302,
      "cny": 298785.10989287664,
      "czk": 944615.3438828368,
      "dkk": 285068.92147269147,
      "dot": 5160.299955562896,
      "eos": 50098.037591566885,
      "eth": 18.514283305187227,
      "eur": 38240.20908960317,
      "gbp": 33156.484386694596,
      "gel": 113329.02284306048,
      "hkd": 329606.38328597124,
      "huf": 14657368.01641012,
      "idr": 649885162.0865278,
      "ils": 152105.57155771676,
      "inr": 3513053.119048727,
      "jpy": 5952559.440604322,
      "krw": 54661344.54593342,
      "kwd": 12984.298194449415,
      "lkr": 13696906.151726862,
      "ltc": 579.0962960970021,
      "mmk": 88806742.41781776,
      "mxn": 716452.3647481233,
      "myr": 194052.20950501712,
      "ngn": 37886364.22413555,
      "nok": 429442.7101393702,
      "nzd": 66802.583918633,
      "php": 2338503.1911612307,
      "pkr": 11792242.372501094,
      "pln": 165880.09171330827,
      "rub": 3767047.138041446,
      "sar": 158357.45046405343,
      "sek": 425811.11642413173,
      "sgd": 55694.77797653248,
      "sol": 416.5289478886034,
      "thb": 1453127.860988517,
      "try": 1243001.417432343,
      "twd": 1295461.9075007213,
      "uah": 1607901.3285893872,
      "usd": 42208.202176186474,
      "vef": 4226.30728390156,
      "vnd": 1024346748.4635574,
      "xag": 1773.9385614394023,
      "xau": 20.435523165622502,
      "xdr": 31508.676173736272,
      "xlm": 327801.5907899002,
      "xrp": 68792.39040895543,
      "yfi": 5.23330767599715,
      "zar": 772207.5004537676,
      "bits": 999797.6500840397,
      "link": 2828.6459350540995,
      "sats": 99979765.00840396
    },
    "market_cap": {
      "aed": 3039570628249.035,
      "ars": 671030943774608.1,
      "aud": 1214911274669.9553,
      "bch": 3192400331.4673758,
      "bdt": 90997783863352.8,
      "bhd": 312458958958.8847,
      "bmd": 827596236151.1959,
      "bnb": 2647323702.8955383,
      "brl": 4015882597651.6562,
      "btc": 19586150.0,
      "cad": 1096560874919.1543,
      "chf": 696004296621.9747,
      "clp": 729321641896660.1,
      "cny": 5858421340316.535,
      "czk": 18521521005440.16,
      "dkk": 5589481529435.656,
      "dot": 101067225072.82333,
      "eos": 981764701266.0074,
      "eth": 362734483.2978319,
      "eur": 749793913990.623,
      "gbp": 650114912923.6271,
      "gel": 2222095894065.9663,
      "hkd": 6462748663878.865,
      "huf": 287393965552690.7,
      "idr": 12742606563251504,
      "ils": 2982406073429.352,
      "inr": 68882098474316.74,
      "jpy": 116714655790049.02,
      "krw": 1071770904156178.4,
      "kwd": 254589292146.01266,
      "lkr": 268561734299139.16,
      "ltc": 11369266145.87004,
      "mmk": 1741275912749029.8,
      "mxn": 14047821273508.254,
      "myr": 3804873695705.123,
      "ngn": 742855909912170.9,
      "nok": 8420286869134.373,
      "nzd": 1309829942186.6091,
      "php": 45852141040124.65,
      "pkr": 231216088345279.94,
      "pln": 3252489622308.595,
      "rub": 73862279654407.0,
      "sar": 3104989627928.0786,
      "sek": 8349080488975.917,
      "sgd": 1092033923507.4076,
      "sol": 8167080608.685882,
      "thb": 28493545024184.4,
      "try": 24372118250940.145,
      "twd": 25400735957660.043,
      "uah": 31526883852775.1,
      "usd": 827596236151.1959,
      "vef": 82867211125.81927,
      "vnd": 20084852465487144,
      "xag": 34782454615.8709,
      "xau": 400688993.6949639,
      "xdr": 617805555864.2843,
      "xlm": 6420377180809.443,
      "xrp": 1347730925908.2449,
      "yfi": 102656498.40039586,
      "zar": 15141038659633.365,
      "bits": 19587615789973.43,
      "link": 55342736984.57576,
      "sats": 1958761578997342.8
    },
    "total_volume": {
      "aed": 52093574029.40443,
      "ars": 11500440167656.37,
      "aud": 20821714040.129295,
      "bch": 54756176.21574547,
      "bdt": 1559562309933.2505,
      "bhd": 5355066850.034618,
      "bmd": 14183728910.169804,
      "bnb": 45448519.30208316,
      "brl": 68826062289.8161,
      "btc": 335974.0074837291,
      "cad": 18793369887.330444,
      "chf": 11928445094.808254,
      "clp": 12499453241945.738,
      "cny": 100404347558.46667,
      "czk": 317430434636.70953,
      "dkk": 95795132093.1731,
      "dot": 1734077546.3343449,
      "eos": 16835045026.655567,
      "eth": 6221576.893294353,
      "eur": 12850316555.324738,
      "gbp": 11141971510.468252,
      "gel": 38083312123.805855,
      "hkd": 110761590083.25078,
      "huf": 4925491344396.748,
      "idr": 218388713248196.1,
      "ils": 51113861322.39222,
      "inr": 1180533415747.48,
      "jpy": 2000310012607.8845,
      "krw": 18368507847565.402,
      "kwd": 4363269605.991003,
      "lkr": 4602735813129.19,
      "ltc": 194600680.75008962,
      "mmk": 29842795828917.508,
      "mxn": 240758089534.80554,
      "myr": 65209693664.5056,
      "ngn": 12731409817077.545,
      "nok": 144310789586.34262,
      "nzd": 22448474276.294495,
      "php": 785835302355.318,
      "pkr": 3962688776849.6025,
      "pln": 55742678701.03927,
      "rub": 1265886075288.8472,
      "sar": 53214755248.56654,
      "sek": 143090421550.91183,
      "sgd": 18715784890.19182,
      "sol": 139971223.0203305,
      "thb": 488312000734.88245,
      "try": 417700689222.06055,
      "twd": 435329617517.0529,
      "uah": 540322387194.22906,
      "usd": 14183728910.169804,
      "vef": 1420216775.7753053,
      "vnd": 344223535737756.94,
      "xag": 596117871.9180025,
      "xau": 6867194.189147832,
      "xdr": 10588238733.815224,
      "xlm": 110155103993.25989,
      "xrp": 23117132839.969418,
      "yfi": 1758611.2071300931,
      "zar": 259494157157.33887,
      "bits": 335974007483.7291,
      "link": 950543853.0214615,
      "sats": 33597400748372.91
    }
  },
  "community_data": {
    "facebook_likes": null,
    "reddit_average_posts_48h": 0.0,
    "reddit_average_comments_48h": 0.0,
    "reddit_subscribers": null,
    "reddit_accounts_active_48h": 0.0
  },
  "developer_data": {
    "forks": null,
    "stars": null,
    "subscribers": null,
    "total_issues": null,
    "closed_issues": null,
    "pull_requests_merged": null,
    "pull_request_contributors": null,
    "code_additions_deletions_4_weeks": {
      "additions": null,
      "deletions": null
    },
    "commit_count_4_weeks": null
  },
  "public_interest_stats": {
    "alexa_rank": null,
    "bing_matches": null
  }
}
```


# Coins-Id-Market-Chart

To get the historical chart data of a coin including time in UNIX, price, market cap and 24hrs volume based on particular coin ID

```java
CompletableFuture<ApiResponse<CoinsMarketChart>> coinsIdMarketChartAsync(
    final String id,
    final String vsCurrency,
    final String days,
    final Interval interval,
    final Precision precision)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Coin ID.<br>*refers to [`/coins/list`](/reference/coins-list). |
| `vsCurrency` | `String` | Query, Required | Target currency of market data.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies). |
| `days` | `String` | Query, Required | Data up to number of days ago.<br>You may use any integer or `max` for number of days. |
| `interval` | [`Interval`](../../doc/models/interval.md) | Query, Optional | Data interval, leave empty for auto granularity. |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal place for currency price value. |

## Response Type

**200**: Coin historical chart data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsMarketChart`](../../doc/models/coins-market-chart.md).

## Example Usage

```java
String id = "bitcoin";
String vsCurrency = "usd";
String days = "1";

api.coinsIdMarketChartAsync(id, vsCurrency, days, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "prices": [
    [
      1779027899041,
      77953.82550382407
    ],
    [
      1779028199661,
      78052.87543398788
    ]
  ],
  "market_caps": [
    [
      1779027899041,
      1560631481361.8042
    ],
    [
      1779028199661,
      1562027330524.267
    ]
  ],
  "total_volumes": [
    [
      1779027899041,
      18688431751.857048
    ],
    [
      1779028199661,
      18974828816.446976
    ]
  ]
}
```


# Coins-Id-Market-Chart-Range

To get the historical chart data of a coin within certain time range in UNIX along with price, market cap and 24hrs volume based on particular coin ID

```java
CompletableFuture<ApiResponse<CoinsMarketChart>> coinsIdMarketChartRangeAsync(
    final String id,
    final String vsCurrency,
    final int from,
    final int to,
    final Precision precision)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Coin ID.<br>*refers to [`/coins/list`](/reference/coins-list). |
| `vsCurrency` | `String` | Query, Required | Target currency of market data.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies). |
| `from` | `int` | Query, Required | Starting date in UNIX timestamp. |
| `to` | `int` | Query, Required | Ending date in UNIX timestamp. |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal place for currency price value. |

## Response Type

**200**: Coin historical chart data within time range

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsMarketChart`](../../doc/models/coins-market-chart.md).

## Example Usage

```java
String id = "bitcoin";
String vsCurrency = "usd";
int from = 1767024000;
int to = 1777564800;

api.coinsIdMarketChartRangeAsync(id, vsCurrency, from, to, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "prices": [
    [
      1779027899041,
      77953.82550382407
    ],
    [
      1779028199661,
      78052.87543398788
    ]
  ],
  "market_caps": [
    [
      1779027899041,
      1560631481361.8042
    ],
    [
      1779028199661,
      1562027330524.267
    ]
  ],
  "total_volumes": [
    [
      1779027899041,
      18688431751.857048
    ],
    [
      1779028199661,
      18974828816.446976
    ]
  ]
}
```


# Coins-Id-Ohlc

To get the OHLC chart (Open, High, Low, Close) of a coin based on particular coin ID

```java
CompletableFuture<ApiResponse<List<List<Double>>>> coinsIdOhlcAsync(
    final String id,
    final String vsCurrency,
    final Days days,
    final Precision precision)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Coin ID.<br>*refers to [`/coins/list`](/reference/coins-list). |
| `vsCurrency` | `String` | Query, Required | Target currency of price data.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies). |
| `days` | [`Days`](../../doc/models/days.md) | Query, Required | Data up to number of days ago. |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal place for currency price value. |

## Response Type

**200**: Coin OHLC chart data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `List<List<Double>>`.

## Example Usage

```java
String id = "bitcoin";
String vsCurrency = "usd";
Days days = Days.ENUM_1;

api.coinsIdOhlcAsync(id, vsCurrency, days, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response

```
[
  [
    1779199200000,
    76769.0,
    76889.0,
    76744.0,
    76818.0
  ],
  [
    1779201000000,
    76712.0,
    76712.0,
    76321.0,
    76422.0
  ]
]
```


# Coins-Contract-Address

To query all the metadata (image, websites, socials, description, contract address, etc.) and market data (price, ATH, exchange tickers, etc.) of a coin based on an asset platform and a particular token contract address

```java
CompletableFuture<ApiResponse<CoinsContractAddress>> coinsContractAddressAsync(
    final String id,
    final String contractAddress)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Asset platform ID.<br>*refers to [`/asset_platforms`](/reference/asset-platforms-list). |
| `contractAddress` | `String` | Template, Required | The contract address of token. |

## Response Type

**200**: Coin data by token contract address

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsContractAddress`](../../doc/models/coins-contract-address.md).

## Example Usage

```java
String id = "ethereum";
String contractAddress = "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2";

api.coinsContractAddressAsync(id, contractAddress).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Contract-Address-Market-Chart

To get the historical chart data including time in UNIX, price, market cap and 24hrs volume based on asset platform and particular token contract address

```java
CompletableFuture<ApiResponse<CoinsMarketChart>> contractAddressMarketChartAsync(
    final String id,
    final String contractAddress,
    final String vsCurrency,
    final String days,
    final Interval interval,
    final Precision precision)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Asset platform ID.<br>*refers to [`/asset_platforms`](/reference/asset-platforms-list). |
| `contractAddress` | `String` | Template, Required | The contract address of token. |
| `vsCurrency` | `String` | Query, Required | Target currency of market data.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies). |
| `days` | `String` | Query, Required | Data up to number of days ago.<br>You may use any integer or `max` for number of days. |
| `interval` | [`Interval`](../../doc/models/interval.md) | Query, Optional | Data interval, leave empty for auto granularity. |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal place for currency price value. |

## Response Type

**200**: Coin historical chart data by token address

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsMarketChart`](../../doc/models/coins-market-chart.md).

## Example Usage

```java
String id = "ethereum";
String contractAddress = "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48";
String vsCurrency = "usd";
String days = "1";

api.contractAddressMarketChartAsync(id, contractAddress, vsCurrency, days, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "prices": [
    [
      1779619498604,
      0.9997624087636037
    ],
    [
      1779619877081,
      0.9997817655336941
    ]
  ],
  "market_caps": [
    [
      1779619498604,
      76419636272.78033
    ],
    [
      1779619877081,
      76424065983.84229
    ]
  ],
  "total_volumes": [
    [
      1779619498604,
      9374311493.936354
    ],
    [
      1779619877081,
      9390008044.485624
    ]
  ]
}
```


# Contract-Address-Market-Chart-Range

To get the historical chart data within certain time range in UNIX along with price, market cap and 24hrs volume based on asset platform and particular token contract address

```java
CompletableFuture<ApiResponse<CoinsMarketChart>> contractAddressMarketChartRangeAsync(
    final String id,
    final String contractAddress,
    final String vsCurrency,
    final int from,
    final int to,
    final Precision precision)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Asset platform ID.<br>*refers to [`/asset_platforms`](/reference/asset-platforms-list). |
| `contractAddress` | `String` | Template, Required | The contract address of token. |
| `vsCurrency` | `String` | Query, Required | Target currency of market data.<br>*refers to [`/simple/supported_vs_currencies`](/reference/simple-supported-currencies). |
| `from` | `int` | Query, Required | Starting date in UNIX timestamp. |
| `to` | `int` | Query, Required | Ending date in UNIX timestamp. |
| `precision` | [`Precision`](../../doc/models/precision.md) | Query, Optional | Decimal place for currency price value. |

## Response Type

**200**: Coin historical chart data within time range by token address

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsMarketChart`](../../doc/models/coins-market-chart.md).

## Example Usage

```java
String id = "ethereum";
String contractAddress = "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48";
String vsCurrency = "usd";
int from = 1767024000;
int to = 1777564800;

api.contractAddressMarketChartRangeAsync(id, contractAddress, vsCurrency, from, to, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "prices": [
    [
      1735689600000,
      1.000540738607754
    ],
    [
      1735776000000,
      0.9995995563541714
    ]
  ],
  "market_caps": [
    [
      1735689600000,
      43945617394.42927
    ],
    [
      1735776000000,
      43740787028.36501
    ]
  ],
  "total_volumes": [
    [
      1735689600000,
      6544488766.849924
    ],
    [
      1735776000000,
      5447401746.320422
    ]
  ]
}
```


# Asset-Platforms-List

To query all the supported asset platforms (blockchain networks) on CoinGecko

```java
CompletableFuture<ApiResponse<List<AssetPlatform>>> assetPlatformsListAsync(
    final Filter filter)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | [`Filter`](../../doc/models/filter.md) | Query, Optional | Apply relevant filters to results. |

## Response Type

**200**: List of asset platforms

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<AssetPlatform>`](../../doc/models/asset-platform.md).

## Example Usage

```java
api.assetPlatformsListAsync(null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "solana",
    "chain_identifier": null,
    "name": "Solana",
    "shortname": "Solana",
    "native_coin_id": "solana",
    "image": {
      "thumb": "https://coin-images.coingecko.com/asset_platforms/images/5/thumb/solana.png?1706606708",
      "small": "https://coin-images.coingecko.com/asset_platforms/images/5/small/solana.png?1706606708",
      "large": "https://coin-images.coingecko.com/asset_platforms/images/5/large/solana.png?1706606708"
    }
  },
  {
    "id": "flow-evm",
    "chain_identifier": 747,
    "name": "Flow EVM",
    "shortname": "",
    "native_coin_id": "flow",
    "image": {
      "thumb": "https://coin-images.coingecko.com/asset_platforms/images/22173/thumb/flow.jpg?1727072603",
      "small": "https://coin-images.coingecko.com/asset_platforms/images/22173/small/flow.jpg?1727072603",
      "large": "https://coin-images.coingecko.com/asset_platforms/images/22173/large/flow.jpg?1727072603"
    }
  }
]
```


# Token-Lists

To get full list of tokens of a blockchain network (asset platform) that is supported by [Ethereum token list standard](https://tokenlists.org/)

```java
CompletableFuture<ApiResponse<TokenLists>> tokenListsAsync(
    final String assetPlatformId)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assetPlatformId` | `String` | Template, Required | Asset platform ID.<br>*refers to [`/asset_platforms`](/reference/asset-platforms-list). |

## Response Type

**200**: Token list by asset platform

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`TokenLists`](../../doc/models/token-lists.md).

## Example Usage

```java
String assetPlatformId = "ethereum";

api.tokenListsAsync(assetPlatformId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "name": "CoinGecko",
  "logoURI": "https://static.coingecko.com/gecko-new.svg",
  "keywords": [
    "defi"
  ],
  "timestamp": "2026-05-26T04:03:03.404+00:00",
  "tokens": [
    {
      "chainId": 1,
      "address": "0x77c6e4a580c0dce4e5c7a17d0bc077188a83a059",
      "name": "Swerve.fi USD",
      "symbol": "SWUSD",
      "decimals": 18,
      "logoURI": "https://assets.coingecko.com/coins/images/12918/thumb/swerve.png?1696512706"
    },
    {
      "chainId": 1,
      "address": "0xf8e57ac2730d3088d98b79209739b0d5ba085a03",
      "name": "Optopia AI",
      "symbol": "OPAI",
      "decimals": 18,
      "logoURI": "https://assets.coingecko.com/coins/images/39332/thumb/OPAI.jpg?1721777150"
    }
  ],
  "version": {
    "major": 1491,
    "minor": 3,
    "patch": 0
  }
}
```


# Coins-Categories-List

To query all the supported coins categories on CoinGecko

```java
CompletableFuture<ApiResponse<List<CategoriesList>>> coinsCategoriesListAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: List of coin categories

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<CategoriesList>`](../../doc/models/categories-list.md).

## Example Usage

```java
api.coinsCategoriesListAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "category_id": "coinbase-ventures-portfolio",
    "name": "Coinbase Ventures Portfolio"
  },
  {
    "category_id": "gmci-index",
    "name": "GMCI Index"
  }
]
```


# Coins-Categories

To query all the coins categories with market data (market cap, volume, etc.) on CoinGecko

```java
CompletableFuture<ApiResponse<List<Category1>>> coinsCategoriesAsync(
    final Order2 order)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order` | [`Order2`](../../doc/models/order-2.md) | Query, Optional | Sort results by field.<br>Default: `market_cap_desc` |

## Response Type

**200**: List of coin categories with market data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<Category1>`](../../doc/models/category-1.md).

## Example Usage

```java
api.coinsCategoriesAsync(null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "smart-contract-platform",
    "name": "Smart Contract Platform",
    "market_cap": 2176528015490.1301,
    "market_cap_change_24h": -0.4907335508040635,
    "content": "Smart contract platforms are usually blockchains that host smart contracts or decentralized applications.",
    "top_3_coins_id": [
      "bitcoin",
      "ethereum",
      "binancecoin"
    ],
    "top_3_coins": [
      "https://coin-images.coingecko.com/coins/images/1/small/bitcoin.png",
      "https://coin-images.coingecko.com/coins/images/279/small/ethereum.png",
      "https://coin-images.coingecko.com/coins/images/825/small/bnb-icon2_2x.png"
    ],
    "volume_24h": 45616943988.58024,
    "updated_at": "2026-05-26T10:02:24.777Z"
  },
  {
    "id": "layer-1",
    "name": "Layer 1 (L1)",
    "market_cap": 2152576804747.1516,
    "market_cap_change_24h": -0.538526079299288,
    "content": "Layer 1 serves as the primary and autonomous chain on which transactions are directly executed and confirmed.",
    "top_3_coins_id": [
      "bitcoin",
      "ethereum",
      "binancecoin"
    ],
    "top_3_coins": [
      "https://coin-images.coingecko.com/coins/images/1/small/bitcoin.png",
      "https://coin-images.coingecko.com/coins/images/279/small/ethereum.png",
      "https://coin-images.coingecko.com/coins/images/825/small/bnb-icon2_2x.png"
    ],
    "volume_24h": 44289945362.19749,
    "updated_at": "2026-05-26T10:01:55.213Z"
  }
]
```


# Exchanges

To query all the supported exchanges with exchanges' data (ID, name, country, etc.) that have active trading volumes on CoinGecko

```java
CompletableFuture<ApiResponse<List<Exchange1>>> exchangesAsync(
    final Double perPage,
    final Double page)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perPage` | [`Double`](../../doc/models/precision.md) | Query, Optional | Total results per page.<br>Default: 100.<br>Valid values: 1...250 |
| `page` | [`Double`](../../doc/models/precision.md) | Query, Optional | Page through results.<br>Default: 1 |

## Response Type

**200**: List of exchanges with data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<Exchange1>`](../../doc/models/exchange-1.md).

## Example Usage

```java
api.exchangesAsync(null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "gdax",
    "name": "Coinbase Exchange",
    "year_established": 2012,
    "country": "United States",
    "description": "A leading U.S.-based exchange known for its regulatory compliance, user-friendly interface, and support for fiat-to-crypto transactions.",
    "url": "https://www.coinbase.com/",
    "image": "https://coin-images.coingecko.com/markets/images/23/small/Coinbase_Coin_Primary.png?1706864258",
    "has_trading_incentive": false,
    "trust_score": 10,
    "trust_score_rank": 1,
    "trade_volume_24h_btc": 13692.36253111657
  },
  {
    "id": "binance",
    "name": "Binance",
    "year_established": 2017,
    "country": "Cayman Islands",
    "description": "One of the world's largest cryptocurrency exchanges by trading volume.",
    "url": "https://www.binance.com/",
    "image": "https://coin-images.coingecko.com/markets/images/52/small/binance.jpg?1706864274",
    "has_trading_incentive": false,
    "trust_score": 10,
    "trust_score_rank": 2,
    "trade_volume_24h_btc": 95140.00808634966
  }
]
```


# Exchanges-List

To query all the supported exchanges with ID and name

```java
CompletableFuture<ApiResponse<List<ExchangesList>>> exchangesListAsync(
    final Status status)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status`](../../doc/models/status.md) | Query, Optional | Filter by status of exchanges.<br>Default: `active` |

## Response Type

**200**: List of exchanges

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<ExchangesList>`](../../doc/models/exchanges-list.md).

## Example Usage

```java
api.exchangesListAsync(null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "binance",
    "name": "Binance"
  },
  {
    "id": "bitget",
    "name": "Bitget"
  },
  {
    "id": "okex",
    "name": "OKX"
  }
]
```


# Exchanges-Id

To query exchange's data (name, year established, country, etc.), exchange volume in BTC and top 100 tickers based on exchange's ID

```java
CompletableFuture<ApiResponse<ExchangesId>> exchangesIdAsync(
    final String id,
    final DexPairFormat dexPairFormat)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Exchange ID.<br>*refers to [`/exchanges/list`](/reference/exchanges-list). |
| `dexPairFormat` | [`DexPairFormat`](../../doc/models/dex-pair-format.md) | Query, Optional | Set to `symbol` to display DEX pair base and target as symbols.<br>Default: `contract_address` |

## Response Type

**200**: Exchange data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ExchangesId`](../../doc/models/exchanges-id.md).

## Example Usage

```java
String id = "binance";

api.exchangesIdAsync(id, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "name": "Binance",
  "year_established": 2017,
  "country": "Cayman Islands",
  "description": "One of the world's largest cryptocurrency exchanges by trading volume.",
  "url": "https://www.binance.com/",
  "image": "https://coin-images.coingecko.com/markets/images/52/small/binance.jpg?1706864274",
  "facebook_url": "https://www.facebook.com/binanceexchange",
  "reddit_url": "https://www.reddit.com/r/binance/",
  "telegram_url": "",
  "slack_url": "",
  "other_url_1": "https://medium.com/binanceexchange",
  "other_url_2": "https://steemit.com/@binanceexchange",
  "twitter_handle": "binance",
  "has_trading_incentive": false,
  "centralized": true,
  "public_notice": "",
  "alert_notice": "",
  "trust_score": 10,
  "trust_score_rank": 2,
  "coins": 435,
  "pairs": 1391,
  "trade_volume_24h_btc": 95073.68489926813,
  "tickers": [
    {
      "base": "USDC",
      "target": "USDT",
      "market": {
        "name": "Binance",
        "identifier": "binance",
        "has_trading_incentive": false
      },
      "last": 1.00087,
      "volume": 2089887585.0,
      "converted_last": {
        "btc": 1.301E-05,
        "eth": 0.00047417,
        "usd": 0.999569
      },
      "converted_volume": {
        "btc": 27187,
        "eth": 990971,
        "usd": 2088986570
      },
      "trust_score": null,
      "bid_ask_spread_percentage": 0.010999,
      "timestamp": "2026-05-26T10:21:17+00:00",
      "last_traded_at": "2026-05-26T10:21:17+00:00",
      "last_fetch_at": "2026-05-26T10:23:00+00:00",
      "is_anomaly": false,
      "is_stale": false,
      "trade_url": "https://www.binance.com/en/trade/USDC_USDT?ref=37754157",
      "token_info_url": null,
      "coin_id": "usd-coin",
      "target_coin_id": "tether",
      "coin_mcap_usd": 76286248956.20789
    },
    {
      "base": "BTC",
      "target": "USDT",
      "market": {
        "name": "Binance",
        "identifier": "binance",
        "has_trading_incentive": false
      },
      "last": 76960.0,
      "volume": 9037.21995,
      "converted_last": {
        "btc": 1.000348,
        "eth": 36.491428,
        "usd": 76860
      },
      "converted_volume": {
        "btc": 9040,
        "eth": 329781,
        "usd": 694600292
      },
      "trust_score": null,
      "bid_ask_spread_percentage": 0.010013,
      "timestamp": "2026-05-26T10:21:39+00:00",
      "last_traded_at": "2026-05-26T10:21:39+00:00",
      "last_fetch_at": "2026-05-26T10:22:33+00:00",
      "is_anomaly": false,
      "is_stale": false,
      "trade_url": "https://www.binance.com/en/trade/BTC_USDT?ref=37754157",
      "token_info_url": null,
      "coin_id": "bitcoin",
      "target_coin_id": "tether",
      "coin_mcap_usd": 1536007329547.9153
    }
  ],
  "status_updates": [
    {
      "description": "Juventus and Paris Saint-Germain Fan Tokens on Binance Launchpool!",
      "category": "general",
      "created_at": "2020-12-14T11:18:49.085Z",
      "user": "Darc",
      "user_title": "Marketing",
      "pin": false,
      "project": {
        "type": "Market",
        "id": "binance",
        "name": "Binance",
        "image": {
          "thumb": "https://coin-images.coingecko.com/markets/images/52/thumb/binance.jpg?1706864274",
          "small": "https://coin-images.coingecko.com/markets/images/52/small/binance.jpg?1706864274",
          "large": "https://coin-images.coingecko.com/markets/images/52/large/binance.jpg?1706864274"
        }
      }
    }
  ]
}
```


# Exchanges-Id-Tickers

To query exchange's tickers based on exchange's ID

```java
CompletableFuture<ApiResponse<CoinsIdTickers>> exchangesIdTickersAsync(
    final String id,
    final String coinIds,
    final Boolean includeExchangeLogo,
    final Double page,
    final Boolean depth,
    final Order3 order,
    final DexPairFormat dexPairFormat)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Exchange ID.<br>*refers to [`/exchanges/list`](/reference/exchanges-list). |
| `coinIds` | `String` | Query, Optional | Filter tickers by coin IDs, comma-separated if querying more than 1 coin.<br>*refers to [`/coins/list`](/reference/coins-list). |
| `includeExchangeLogo` | `Boolean` | Query, Optional | Include exchange logo.<br>Default: false |
| `page` | [`Double`](../../doc/models/precision.md) | Query, Optional | Page through results. |
| `depth` | `Boolean` | Query, Optional | Include 2% orderbook depth (cost_to_move_up_usd and cost_to_move_down_usd).<br>Default: false |
| `order` | [`Order3`](../../doc/models/order-3.md) | Query, Optional | Sort the order of responses.<br>Default: `trust_score_desc` |
| `dexPairFormat` | [`DexPairFormat`](../../doc/models/dex-pair-format.md) | Query, Optional | Set to `symbol` to display DEX pair base and target as symbols.<br>Default: `contract_address` |

## Response Type

**200**: Exchange tickers

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CoinsIdTickers`](../../doc/models/coins-id-tickers.md).

## Example Usage

```java
String id = "binance";

api.exchangesIdTickersAsync(id, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "name": "Binance",
  "tickers": [
    {
      "base": "BTC",
      "target": "USDT",
      "market": {
        "name": "Binance",
        "identifier": "binance",
        "has_trading_incentive": false,
        "logo": "https://coin-images.coingecko.com/markets/images/52/small/binance.jpg?1706864274"
      },
      "last": 77172.88,
      "volume": 9243.62632,
      "cost_to_move_up_usd": 21983152.092277337,
      "cost_to_move_down_usd": 19695552.01703934,
      "converted_last": {
        "btc": 0.99912594,
        "eth": 36.349604,
        "usd": 77080
      },
      "converted_volume": {
        "btc": 9236,
        "eth": 336002,
        "usd": 712501236
      },
      "trust_score": null,
      "bid_ask_spread_percentage": 0.010013,
      "timestamp": "2026-05-26T10:32:37+00:00",
      "last_traded_at": "2026-05-26T10:32:37+00:00",
      "last_fetch_at": "2026-05-26T10:33:31+00:00",
      "is_anomaly": false,
      "is_stale": false,
      "trade_url": "https://www.binance.com/en/trade/BTC_USDT?ref=37754157",
      "token_info_url": null,
      "coin_id": "bitcoin",
      "target_coin_id": "tether",
      "coin_mcap_usd": 1545160286928.7285
    },
    {
      "base": "BTC",
      "target": "USDC",
      "market": {
        "name": "Binance",
        "identifier": "binance",
        "has_trading_incentive": false,
        "logo": "https://coin-images.coingecko.com/markets/images/52/small/binance.jpg?1706864274"
      },
      "last": 77189.96,
      "volume": 2736.40541,
      "cost_to_move_up_usd": 5747075.588603265,
      "cost_to_move_down_usd": 4869585.811774237,
      "converted_last": {
        "btc": 1.000158,
        "eth": 36.386207,
        "usd": 77159
      },
      "converted_volume": {
        "btc": 2737,
        "eth": 99567,
        "usd": 211138535
      },
      "trust_score": null,
      "bid_ask_spread_percentage": 0.010013,
      "timestamp": "2026-05-26T10:32:01+00:00",
      "last_traded_at": "2026-05-26T10:32:01+00:00",
      "last_fetch_at": "2026-05-26T10:33:30+00:00",
      "is_anomaly": false,
      "is_stale": false,
      "trade_url": "https://www.binance.com/en/trade/BTC_USDC?ref=37754157",
      "token_info_url": null,
      "coin_id": "bitcoin",
      "target_coin_id": "usd-coin",
      "coin_mcap_usd": 1545160286928.7285
    }
  ]
}
```


# Exchanges-Id-Volume-Chart

To query the historical volume chart data with time in UNIX and trading volume data in BTC based on exchange's ID

```java
CompletableFuture<ApiResponse<List<List<ExchangeVolumeChart>>>> exchangesIdVolumeChartAsync(
    final String id,
    final Days days)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Exchange ID or derivative exchange ID.<br>*refers to [`/exchanges/list`](/reference/exchanges-list) or [`/derivatives/exchanges/list`](/reference/derivatives-exchanges-list). |
| `days` | [`Days`](../../doc/models/days.md) | Query, Required | Data up to number of days ago. |

## Response Type

**200**: Exchange volume chart data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `List<List<ExchangeVolumeChart>>`.

## Example Usage

```java
String id = "binance";
Days days = Days.ENUM_1;

api.exchangesIdVolumeChartAsync(id, days).thenAccept(result -> {
    // TODO success callback handler
    result.getResult().forEach(i -> i.forEach(i1 -> i1.match(new ExchangeVolumeChart.Cases<Void>() {
        @Override
        public Void precision(double precision) {
            System.out.println(precision);
            return null;
        }

        @Override
        public Void string(String string) {
            System.out.println(string);
            return null;
        }
    })));
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response

```
[
  [
    1779719400000,
    "76327.6889417086372104"
  ],
  [
    1779720000000,
    "76335.761747668369059"
  ]
]
```


# Derivatives-Tickers

To query all the tickers from derivatives exchanges on CoinGecko

```java
CompletableFuture<ApiResponse<List<DerivativesTicker>>> derivativesTickersAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: List of derivative tickers

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<DerivativesTicker>`](../../doc/models/derivatives-ticker.md).

## Example Usage

```java
api.derivativesTickersAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "market": "Binance (Futures)",
    "symbol": "BTCUSDT",
    "index_id": "BTC",
    "price": "77034.8",
    "price_percentage_change_24h": -1.1733397846861013,
    "contract_type": "perpetual",
    "index": 76691.4276087,
    "basis": -0.138769748300737,
    "spread": 0.01,
    "funding_rate": 0.004308,
    "open_interest": 7497508223.83,
    "volume_24h": 9623150393.3656,
    "last_traded_at": 1779807819,
    "expired_at": null
  },
  {
    "market": "Binance (Futures)",
    "symbol": "ETHUSDT",
    "index_id": "ETH",
    "price": "2113.92",
    "price_percentage_change_24h": -1.213464572845443,
    "contract_type": "perpetual",
    "index": 2099.55744186,
    "basis": -0.19217332857957786,
    "spread": 0.01,
    "funding_rate": 0.005327,
    "open_interest": 4563725156.36,
    "volume_24h": 7655835901.46112,
    "last_traded_at": 1779807818,
    "expired_at": null
  }
]
```


# Derivatives-Exchanges

To query all the derivatives exchanges with related data (ID, name, open interest, ...) on CoinGecko

```java
CompletableFuture<ApiResponse<List<DerivativesExchange>>> derivativesExchangesAsync(
    final Order4 order,
    final Integer perPage,
    final Integer page)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order` | [`Order4`](../../doc/models/order-4.md) | Query, Optional | Sort order of responses.<br>Default: `open_interest_btc_desc` |
| `perPage` | `Integer` | Query, Optional | Total results per page. |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |

## Response Type

**200**: List of derivative exchanges with data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<DerivativesExchange>`](../../doc/models/derivatives-exchange.md).

## Example Usage

```java
api.derivativesExchangesAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "name": "Binance (Futures)",
    "id": "binance_futures",
    "open_interest_btc": 332790.5,
    "trade_volume_24h_btc": "588597.24",
    "number_of_perpetual_pairs": 592,
    "number_of_futures_pairs": 72,
    "image": "https://coin-images.coingecko.com/markets/images/466/small/binance_futures.jpg?1706864452",
    "year_established": 2019,
    "country": "Cayman Islands",
    "description": "",
    "url": "https://www.binance.com/"
  },
  {
    "name": "Bybit (Futures)",
    "id": "bybit",
    "open_interest_btc": 148377.99,
    "trade_volume_24h_btc": "162793.82",
    "number_of_perpetual_pairs": 673,
    "number_of_futures_pairs": 68,
    "image": "https://coin-images.coingecko.com/markets/images/460/small/photo_2021-08-12_18-27-50.jpg?1706864447",
    "year_established": 2018,
    "country": "Seychelles",
    "description": "Bybit is the world's second-largest cryptocurrency exchange by trading volume, serving a global community of over 60 million users.",
    "url": "https://www.bybit.com"
  }
]
```


# Derivatives-Exchanges-Id

To query the derivatives exchange's related data (name, open interest, trade volume, ...) based on the exchange's ID

```java
CompletableFuture<ApiResponse<DerivativesExchangesId>> derivativesExchangesIdAsync(
    final String id,
    final IncludeTickers includeTickers)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Derivative exchange ID.<br>*refers to [`/derivatives/exchanges/list`](/reference/derivatives-exchanges-list). |
| `includeTickers` | [`IncludeTickers`](../../doc/models/include-tickers.md) | Query, Optional | Include tickers data.<br>Default: tickers data is not included. |

## Response Type

**200**: Derivative exchange data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`DerivativesExchangesId`](../../doc/models/derivatives-exchanges-id.md).

## Example Usage

```java
String id = "binance_futures";

api.derivativesExchangesIdAsync(id, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "name": "Binance (Futures)",
  "open_interest_btc": 331945.73,
  "trade_volume_24h_btc": "587332.45",
  "number_of_perpetual_pairs": 592,
  "number_of_futures_pairs": 72,
  "image": "https://coin-images.coingecko.com/markets/images/466/small/binance_futures.jpg?1706864452",
  "year_established": 2019,
  "country": "Cayman Islands",
  "description": "",
  "url": "https://www.binance.com/",
  "tickers": [
    {
      "symbol": "0GUSDT",
      "base": "0G",
      "target": "USDT",
      "coin_id": "zero-gravity",
      "target_coin_id": "tether",
      "trade_url": "https://www.binance.com/en/futures/0GUSDT",
      "contract_type": "perpetual",
      "last": 0.473,
      "h24_percentage_change": -1.149,
      "index": 0.47388788,
      "index_basis_percentage": -0.066,
      "bid_ask_spread": 0.0004225649693639931,
      "funding_rate": 0.005,
      "open_interest_usd": 7505441.41551142,
      "h24_volume": 6822128.0,
      "converted_volume": {
        "btc": "42.0799463192663717990920674226785386061670893822933102624",
        "eth": "1536.67707296907453613610493674728740267430011541374571065838147892993088",
        "usd": "3222911.4917378246159226528"
      },
      "converted_last": {
        "btc": "0.0000061681554962419895667586517612508206539318947668958",
        "eth": "0.00022524893595797008442763092934452232539088978034621245902427827196",
        "usd": "0.4724202612055687926"
      },
      "last_traded": 1779809107,
      "expired_at": null
    },
    {
      "symbol": "1000000BOBUSDT",
      "base": "1000000BOB",
      "target": "USDT",
      "coin_id": "build-on-bnb",
      "target_coin_id": "tether",
      "trade_url": "https://www.binance.com/en/futures/1000000BOBUSDT",
      "contract_type": "perpetual",
      "last": 0.015,
      "h24_percentage_change": -3.331,
      "index": 0.01540057,
      "index_basis_percentage": 0.134,
      "bid_ask_spread": 0.001298701298701358,
      "funding_rate": 0.005,
      "open_interest_usd": 916291.34908113,
      "h24_volume": 44830706.0,
      "converted_volume": {
        "btc": "8.975935927077560026865126277039614163512381271518795395788",
        "eth": "327.26598326618858627284207444108921232850344104115627132937452733698970504",
        "usd": "688649.790093212658495595932"
      },
      "converted_last": {
        "btc": "0.000000200218482552506757909748873395828612726116364786198",
        "eth": "0.00000730004080832875097422829063724959433671429223178319501212794925284",
        "usd": "0.015361118562201823422"
      },
      "last_traded": 1779808948,
      "expired_at": null
    }
  ]
}
```


# Derivatives-Exchanges-List

To query all the supported derivatives exchanges with ID and name on CoinGecko

```java
CompletableFuture<ApiResponse<List<DerivativesExchangesList>>> derivativesExchangesListAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: List of derivative exchange identifiers and names

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<DerivativesExchangesList>`](../../doc/models/derivatives-exchanges-list.md).

## Example Usage

```java
api.derivativesExchangesListAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "binance_futures",
    "name": "Binance (Futures)"
  },
  {
    "id": "bybit",
    "name": "Bybit (Futures)"
  }
]
```


# Entities-List

To query all the supported entities on CoinGecko with entity ID, name, symbol, and country

```java
CompletableFuture<ApiResponse<List<EntitiesList>>> entitiesListAsync(
    final EntityType entityType,
    final Integer perPage,
    final Integer page)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entityType` | [`EntityType`](../../doc/models/entity-type.md) | Query, Optional | Filter by entity type. |
| `perPage` | `Integer` | Query, Optional | Total results per page.<br>Default value: 100<br>Valid values: 1...250 |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |

## Response Type

**200**: List of entities with ID, name, symbol, and country

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<EntitiesList>`](../../doc/models/entities-list.md).

## Example Usage

```java
api.entitiesListAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "texas",
    "symbol": "",
    "name": "Texas",
    "country": "US"
  },
  {
    "id": "digipowerx",
    "symbol": "DGX.V",
    "name": "DigiPowerX",
    "country": "US"
  }
]
```


# Companies-Public-Treasury

To query public companies' and governments' cryptocurrency holdings by coin ID

```java
CompletableFuture<ApiResponse<PublicTreasury>> companiesPublicTreasuryAsync(
    final Entity entity,
    final String coinId,
    final Integer perPage,
    final Integer page,
    final Order5 order)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entity` | [`Entity`](../../doc/models/entity.md) | Template, Required | Public company or government entity. |
| `coinId` | `String` | Template, Required | Coin ID.<br>e.g. `bitcoin`, `ethereum`, `solana`, `binancecoin` |
| `perPage` | `Integer` | Query, Optional | Total results per page.<br>Default value: 250<br>Valid values: 1...250 |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `order` | [`Order5`](../../doc/models/order-5.md) | Query, Optional | Sort order for results.<br>Default: `total_holdings_usd_desc` |

## Response Type

**200**: Public companies or governments crypto treasury holdings data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `PublicTreasury`.

## Example Usage

```java
Entity entity = Entity.COMPANIES;
String coinId = "bitcoin";

api.companiesPublicTreasuryAsync(entity, coinId, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    result.getResult().match(new PublicTreasury.Cases<Void>() {
        @Override
        public Void companyTreasury(CompanyTreasury companyTreasury) {
            System.out.println(companyTreasury);
            return null;
        }

        @Override
        public Void governmentTreasury(GovernmentTreasury governmentTreasury) {
            System.out.println(governmentTreasury);
            return null;
        }
    });
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response

```
{
  "total_holdings": 1272129.0267804659,
  "total_value_usd": 97225044888.65527,
  "market_cap_dominance": 6.06,
  "companies": [
    {
      "name": "Strategy",
      "symbol": "MSTR.US",
      "country": "US",
      "total_holdings": 843738.0,
      "total_entry_value_usd": 63870055699.0,
      "total_current_value_usd": 64484706340.107254,
      "percentage_of_total_supply": 4.018
    },
    {
      "name": "XXI",
      "symbol": "XXI.US",
      "country": "US",
      "total_holdings": 43514.0,
      "total_entry_value_usd": 0.0,
      "total_current_value_usd": 3325662126.967645,
      "percentage_of_total_supply": 0.207
    }
  ]
}
```


# Public-Treasury-Entity

To query public companies' and governments' cryptocurrency holdings by entity ID

```java
CompletableFuture<ApiResponse<PublicTreasuryEntity>> publicTreasuryEntityAsync(
    final String entityId,
    final String holdingAmountChange,
    final String holdingChangePercentage)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entityId` | `String` | Template, Required | Public company or government entity ID.<br>*refers to [`/entities/list`](/reference/entities-list). |
| `holdingAmountChange` | `String` | Query, Optional | Include holding amount change for specified timeframes, comma-separated if querying more than 1 timeframe.<br>Valid values: `7d`, `14d`, `30d`, `90d`, `1y`, `ytd` |
| `holdingChangePercentage` | `String` | Query, Optional | Include holding change percentage for specified timeframes, comma-separated if querying more than 1 timeframe.<br>Valid values: `7d`, `14d`, `30d`, `90d`, `1y`, `ytd` |

## Response Type

**200**: Public company or government crypto treasury holdings data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PublicTreasuryEntity`](../../doc/models/public-treasury-entity.md).

## Example Usage

```java
String entityId = "strategy";

api.publicTreasuryEntityAsync(entityId, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "name": "Strategy",
  "id": "strategy",
  "type": "company",
  "symbol": "MSTR.US",
  "country": "US",
  "website_url": "https://www.strategy.com/",
  "twitter_screen_name": "Strategy",
  "total_treasury_value_usd": 64383151578.86817,
  "unrealized_pnl": 513095879.8681717,
  "m_nav": 1.03,
  "total_asset_value_per_share_usd": 179.74079167746558,
  "holdings": [
    {
      "coin_id": "bitcoin",
      "amount": 843738.0,
      "percentage_of_total_supply": 4.018,
      "amount_per_share": 0.002355494137353434,
      "entity_value_usd_percentage": 100.0,
      "current_value_usd": 64383151578.86817,
      "total_entry_value_usd": 63870055699.0,
      "average_entry_value_usd": 75698.9203982753,
      "unrealized_pnl": 513095879.8681717,
      "holding_amount_change": {
        "7d": 0.0,
        "14d": 24869.0,
        "30d": 28677.0,
        "90d": 126016.0,
        "1y": 263488.0,
        "ytd": 171238.0
      },
      "holding_change_percentage": {
        "7d": 0.0,
        "14d": 3.037,
        "30d": 3.518,
        "90d": 17.558,
        "1y": 45.409,
        "ytd": 25.463
      }
    }
  ]
}
```


# Public-Treasury-Entity-Chart

To query historical cryptocurrency holdings chart of public companies and governments by entity ID and coin ID

```java
CompletableFuture<ApiResponse<PublicTreasuryEntityChart>> publicTreasuryEntityChartAsync(
    final String entityId,
    final String coinId,
    final String days,
    final Boolean includeEmptyIntervals)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entityId` | `String` | Template, Required | Public company or government entity ID.<br>*refers to [`/entities/list`](/reference/entities-list). |
| `coinId` | `String` | Template, Required | Coin ID.<br>e.g. `bitcoin`, `ethereum`, `solana`, `binancecoin` |
| `days` | `String` | Query, Required | Data up to number of days ago.<br>Valid values: `7`, `14`, `30`, `90`, `180`, `365` |
| `includeEmptyIntervals` | `Boolean` | Query, Optional | Include empty intervals with no transaction data.<br>Default: `false` |

## Response Type

**200**: Crypto treasury holdings historical chart data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PublicTreasuryEntityChart`](../../doc/models/public-treasury-entity-chart.md).

## Example Usage

```java
String entityId = "strategy";
String coinId = "bitcoin";
String days = "365";

api.publicTreasuryEntityChartAsync(entityId, coinId, days, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "holdings": [
    [
      1748736000000,
      580955.0
    ],
    [
      1749340800000,
      582000.0
    ]
  ],
  "holding_value_in_usd": [
    [
      1748736000000,
      60818730878.617355
    ],
    [
      1749340800000,
      61506606585.45032
    ]
  ]
}
```


# Public-Treasury-Transaction-History

To query public companies' and governments' cryptocurrency transaction history by entity ID

```java
CompletableFuture<ApiResponse<PublicTreasuryTransactionHistory>> publicTreasuryTransactionHistoryAsync(
    final String entityId,
    final Integer perPage,
    final Integer page,
    final Order6 order,
    final String coinIds)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entityId` | `String` | Template, Required | Public company or government entity ID.<br>*refers to [`/entities/list`](/reference/entities-list). |
| `perPage` | `Integer` | Query, Optional | Total results per page.<br>Default value: 100<br>Valid values: 1...250 |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `order` | [`Order6`](../../doc/models/order-6.md) | Query, Optional | Sort order of transactions.<br>Default: `date_desc` |
| `coinIds` | `String` | Query, Optional | Filter transactions by coin IDs, comma-separated if querying more than 1 coin.<br>*refers to [`/coins/list`](/reference/coins-list). |

## Response Type

**200**: Crypto treasury transaction history data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PublicTreasuryTransactionHistory`](../../doc/models/public-treasury-transaction-history.md).

## Example Usage

```java
String entityId = "strategy";

api.publicTreasuryTransactionHistoryAsync(entityId, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "transactions": [
    {
      "date": 1779062400000,
      "source_url": "https://assets.contentstack.io/v3/assets/bltf8d808d9b8cebd37/bltc0d0f9d2d325a368/6a0a710811de4f7e170ba045/form-8-k_05-18-2026.pdf",
      "coin_id": "bitcoin",
      "type": "buy",
      "holding_net_change": 24869.0,
      "transaction_value_usd": 2014015965.0,
      "holding_balance": 843738.0,
      "average_entry_value_usd": 80985.0
    },
    {
      "date": 1778457600000,
      "source_url": "https://assets.contentstack.io/v3/assets/bltf8d808d9b8cebd37/blt7653ead16575975e/6a01462c750c63f12be32cf8/form-8-k_05-11-2026.pdf",
      "coin_id": "bitcoin",
      "type": "buy",
      "holding_net_change": 535.0,
      "transaction_value_usd": 42981900.0,
      "holding_balance": 818869.0,
      "average_entry_value_usd": 80340.0
    }
  ]
}
```


# Nfts-List

To query all supported NFTs with ID, contract address, name, asset platform ID and symbol on CoinGecko

```java
CompletableFuture<ApiResponse<List<NfTsList>>> nftsListAsync(
    final Order7 order,
    final Integer perPage,
    final Integer page)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order` | [`Order7`](../../doc/models/order-7.md) | Query, Optional | Sort order of responses. |
| `perPage` | `Integer` | Query, Optional | Total results per page.<br>Valid values: 1...250 |
| `page` | `Integer` | Query, Optional | Page through results. |

## Response Type

**200**: List of supported NFTs

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<NfTsList>`](../../doc/models/nf-ts-list.md).

## Example Usage

```java
api.nftsListAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
[
  {
    "id": "cryptopunks",
    "contract_address": "0xb47e3cd837dDF8e4c57F05d70Ab865de6e193BBB",
    "name": "CryptoPunks",
    "asset_platform_id": "ethereum",
    "symbol": "PUNK"
  },
  {
    "id": "bored-ape-yacht-club",
    "contract_address": "0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d",
    "name": "Bored Ape Yacht Club",
    "asset_platform_id": "ethereum",
    "symbol": "BAYC"
  }
]
```


# Nfts-Id

To query all the NFT data (name, floor price, 24hr volume, ...) based on the NFT collection ID

```java
CompletableFuture<ApiResponse<NftData>> nftsIdAsync(
    final String id)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | NFT collection ID.<br>*refers to [`/nfts/list`](/reference/nfts-list). |

## Response Type

**200**: NFT collection data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`NftData`](../../doc/models/nft-data.md).

## Example Usage

```java
String id = "pudgy-penguins";

api.nftsIdAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "id": "pudgy-penguins",
  "web_slug": "pudgy-penguins",
  "contract_address": "0xBd3531dA5CF5857e7CfAA92426877b022e612cf8",
  "asset_platform_id": "ethereum",
  "name": "Pudgy Penguins",
  "symbol": "PPG",
  "image": {
    "small": "https://coin-images.coingecko.com/nft_contracts/images/38/small/pudgy.jpg?1730778323",
    "small_2x": "https://coin-images.coingecko.com/nft_contracts/images/38/small_2x/pudgy.jpg?1730778323"
  },
  "banner_image": "https://coin-images.coingecko.com/nft_contracts/images/38/pudgy-penguins-banner.jpg?1730778702",
  "description": "<h3>What Is the Pudgy Penguins NFT Collection?</h3>\n\n<p>Pudgy Penguins is a collection of 8,888 unique NFTs featuring cute cartoon penguins, which are generated from a collection of 150 different hand-drawn traits.",
  "native_currency": "ethereum",
  "native_currency_symbol": "ETH",
  "market_cap_rank": 3,
  "floor_price": {
    "native_currency": 4.67,
    "usd": 9713.91
  },
  "market_cap": {
    "native_currency": 41507,
    "usd": 86337207
  },
  "volume_24h": {
    "native_currency": 28.01,
    "usd": 58262
  },
  "floor_price_in_usd_24h_percentage_change": -1.78233,
  "floor_price_24h_percentage_change": {
    "usd": -1.782332967792004,
    "native_currency": -0.6361858762952403
  },
  "market_cap_24h_percentage_change": {
    "usd": -1.782332967792065,
    "native_currency": -0.6361858762952404
  },
  "volume_24h_percentage_change": {
    "usd": -41.588610680147845,
    "native_currency": -40.90698133583369
  },
  "number_of_unique_addresses": 5174.0,
  "number_of_unique_addresses_24h_percentage_change": -0.01932,
  "volume_in_usd_24h_percentage_change": -41.58861,
  "total_supply": 8888.0,
  "one_day_sales": 6.0,
  "one_day_sales_24h_percentage_change": -40.0,
  "one_day_average_sale_price": 4.668316666666667,
  "one_day_average_sale_price_24h_percentage_change": -1.511635559722812,
  "links": {
    "homepage": "https://www.pudgypenguins.com/",
    "twitter": "https://twitter.com/pudgypenguins",
    "discord": "https://discord.gg/pudgypenguins"
  },
  "floor_price_7d_percentage_change": {
    "usd": -2.6085983246414655,
    "native_currency": -1.1974800093036855
  },
  "floor_price_14d_percentage_change": {
    "usd": -24.816051386825123,
    "native_currency": -16.157991023339317
  },
  "floor_price_30d_percentage_change": {
    "usd": -20.72768500482924,
    "native_currency": -12.366254928188072
  },
  "floor_price_60d_percentage_change": {
    "usd": 15.176366939745344,
    "native_currency": 13.07508549033547
  },
  "floor_price_1y_percentage_change": {
    "usd": -60.37112564100154,
    "native_currency": -51.85567113402062
  },
  "explorers": [
    {
      "name": "Etherscan",
      "link": "https://etherscan.io/token/0xBd3531dA5CF5857e7CfAA92426877b022e612cf8"
    },
    {
      "name": "Ethplorer",
      "link": "https://ethplorer.io/address/0xBd3531dA5CF5857e7CfAA92426877b022e612cf8"
    }
  ],
  "user_favorites_count": 10135,
  "ath": {
    "native_currency": 36.33,
    "usd": 145728
  },
  "ath_change_percentage": {
    "native_currency": -87.1456099642169,
    "usd": -93.3388047739623
  },
  "ath_date": {
    "native_currency": "2024-12-17T07:50:05.897Z",
    "usd": "2024-12-17T08:35:07.390Z"
  }
}
```


# Nfts-Contract-Address

To query all the NFT data (name, floor price, 24hr volume, ...) based on the NFT collection contract address and respective asset platform

```java
CompletableFuture<ApiResponse<NftData>> nftsContractAddressAsync(
    final String assetPlatformId,
    final String contractAddress)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assetPlatformId` | `String` | Template, Required | Asset platform ID.<br>*refers to [`/asset_platforms`](/reference/asset-platforms-list). |
| `contractAddress` | `String` | Template, Required | Contract address of the NFT collection. |

## Response Type

**200**: NFT collection data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`NftData`](../../doc/models/nft-data.md).

## Example Usage

```java
String assetPlatformId = "ethereum";
String contractAddress = "0xBd3531dA5CF5857e7CfAA92426877b022e612cf8";

api.nftsContractAddressAsync(assetPlatformId, contractAddress).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "id": "pudgy-penguins",
  "web_slug": "pudgy-penguins",
  "contract_address": "0xBd3531dA5CF5857e7CfAA92426877b022e612cf8",
  "asset_platform_id": "ethereum",
  "name": "Pudgy Penguins",
  "symbol": "PPG",
  "image": {
    "small": "https://coin-images.coingecko.com/nft_contracts/images/38/small/pudgy.jpg?1730778323",
    "small_2x": "https://coin-images.coingecko.com/nft_contracts/images/38/small_2x/pudgy.jpg?1730778323"
  },
  "banner_image": "https://coin-images.coingecko.com/nft_contracts/images/38/pudgy-penguins-banner.jpg?1730778702",
  "description": "<h3>What Is the Pudgy Penguins NFT Collection?</h3>\n\n<p>Pudgy Penguins is a collection of 8,888 unique NFTs featuring cute cartoon penguins, which are generated from a collection of 150 different hand-drawn traits.",
  "native_currency": "ethereum",
  "native_currency_symbol": "ETH",
  "market_cap_rank": 3,
  "floor_price": {
    "native_currency": 4.67,
    "usd": 9708.85
  },
  "market_cap": {
    "native_currency": 41507,
    "usd": 86292262
  },
  "volume_24h": {
    "native_currency": 28.01,
    "usd": 58232
  },
  "floor_price_in_usd_24h_percentage_change": -1.78233,
  "floor_price_24h_percentage_change": {
    "usd": -1.782332967792004,
    "native_currency": -0.6361858762952403
  },
  "market_cap_24h_percentage_change": {
    "usd": -1.782332967792065,
    "native_currency": -0.6361858762952404
  },
  "volume_24h_percentage_change": {
    "usd": -41.588610680147845,
    "native_currency": -40.90698133583369
  },
  "number_of_unique_addresses": 5174.0,
  "number_of_unique_addresses_24h_percentage_change": -0.01932,
  "volume_in_usd_24h_percentage_change": -41.58861,
  "total_supply": 8888.0,
  "one_day_sales": 6.0,
  "one_day_sales_24h_percentage_change": -40.0,
  "one_day_average_sale_price": 4.668316666666667,
  "one_day_average_sale_price_24h_percentage_change": -1.511635559722812,
  "links": {
    "homepage": "https://www.pudgypenguins.com/",
    "twitter": "https://twitter.com/pudgypenguins",
    "discord": "https://discord.gg/pudgypenguins"
  },
  "floor_price_7d_percentage_change": {
    "usd": -2.6085983246414655,
    "native_currency": -1.1974800093036855
  },
  "floor_price_14d_percentage_change": {
    "usd": -24.816051386825123,
    "native_currency": -16.157991023339317
  },
  "floor_price_30d_percentage_change": {
    "usd": -20.72768500482924,
    "native_currency": -12.366254928188072
  },
  "floor_price_60d_percentage_change": {
    "usd": 15.176366939745344,
    "native_currency": 13.07508549033547
  },
  "floor_price_1y_percentage_change": {
    "usd": -60.37112564100154,
    "native_currency": -51.85567113402062
  },
  "explorers": [
    {
      "name": "Etherscan",
      "link": "https://etherscan.io/token/0xBd3531dA5CF5857e7CfAA92426877b022e612cf8"
    },
    {
      "name": "Ethplorer",
      "link": "https://ethplorer.io/address/0xBd3531dA5CF5857e7CfAA92426877b022e612cf8"
    }
  ],
  "user_favorites_count": 10135,
  "ath": {
    "native_currency": 36.33,
    "usd": 145728
  },
  "ath_change_percentage": {
    "native_currency": -87.1456099642169,
    "usd": -93.3388047739623
  },
  "ath_date": {
    "native_currency": "2024-12-17T07:50:05.897Z",
    "usd": "2024-12-17T08:35:07.390Z"
  }
}
```


# Exchange-Rates

To query BTC exchange rates with other currencies

```java
CompletableFuture<ApiResponse<ExchangeRates>> exchangeRatesAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: BTC exchange rates with other currencies

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ExchangeRates`](../../doc/models/exchange-rates.md).

## Example Usage

```java
api.exchangeRatesAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "rates": {
    "btc": {
      "name": "Bitcoin",
      "unit": "BTC",
      "value": 1.0,
      "type": "crypto"
    },
    "eth": {
      "name": "Ether",
      "unit": "ETH",
      "value": 36.856,
      "type": "crypto"
    },
    "ltc": {
      "name": "Litecoin",
      "unit": "LTC",
      "value": 1467.048,
      "type": "crypto"
    },
    "bch": {
      "name": "Bitcoin Cash",
      "unit": "BCH",
      "value": 220.614,
      "type": "crypto"
    },
    "bnb": {
      "name": "Binance Coin",
      "unit": "BNB",
      "value": 115.992,
      "type": "crypto"
    },
    "eos": {
      "name": "EOS",
      "unit": "EOS",
      "value": 966946.841,
      "type": "crypto"
    },
    "xrp": {
      "name": "XRP",
      "unit": "XRP",
      "value": 57106.503,
      "type": "crypto"
    },
    "xlm": {
      "name": "Lumens",
      "unit": "XLM",
      "value": 516007.211,
      "type": "crypto"
    },
    "link": {
      "name": "Chainlink",
      "unit": "LINK",
      "value": 8071.362,
      "type": "crypto"
    },
    "dot": {
      "name": "Polkadot",
      "unit": "DOT",
      "value": 60793.71,
      "type": "crypto"
    },
    "yfi": {
      "name": "Yearn.finance",
      "unit": "YFI",
      "value": 31.064,
      "type": "crypto"
    },
    "sol": {
      "name": "Solana",
      "unit": "SOL",
      "value": 910.892,
      "type": "crypto"
    },
    "usd": {
      "name": "US Dollar",
      "unit": "$",
      "value": 75817.765,
      "type": "fiat"
    },
    "aed": {
      "name": "United Arab Emirates Dirham",
      "unit": "DH",
      "value": 278488.131,
      "type": "fiat"
    },
    "ars": {
      "name": "Argentine Peso",
      "unit": "$",
      "value": 106789785.77,
      "type": "fiat"
    },
    "aud": {
      "name": "Australian Dollar",
      "unit": "A$",
      "value": 105840.918,
      "type": "fiat"
    },
    "bdt": {
      "name": "Bangladeshi Taka",
      "unit": "৳",
      "value": 9307822.089,
      "type": "fiat"
    },
    "bhd": {
      "name": "Bahraini Dinar",
      "unit": "BD",
      "value": 28600.735,
      "type": "fiat"
    },
    "bmd": {
      "name": "Bermudian Dollar",
      "unit": "$",
      "value": 75817.765,
      "type": "fiat"
    },
    "brl": {
      "name": "Brazil Real",
      "unit": "R$",
      "value": 382288.415,
      "type": "fiat"
    },
    "cad": {
      "name": "Canadian Dollar",
      "unit": "CA$",
      "value": 104717.981,
      "type": "fiat"
    },
    "chf": {
      "name": "Swiss Franc",
      "unit": "Fr.",
      "value": 59575.401,
      "type": "fiat"
    },
    "clp": {
      "name": "Chilean Peso",
      "unit": "CLP$",
      "value": 67941058.208,
      "type": "fiat"
    },
    "cny": {
      "name": "Chinese Yuan",
      "unit": "¥",
      "value": 515083.156,
      "type": "fiat"
    },
    "czk": {
      "name": "Czech Koruna",
      "unit": "Kč",
      "value": 1582693.892,
      "type": "fiat"
    },
    "dkk": {
      "name": "Danish Krone",
      "unit": "kr.",
      "value": 487401.483,
      "type": "fiat"
    },
    "eur": {
      "name": "Euro",
      "unit": "€",
      "value": 65223.37,
      "type": "fiat"
    },
    "gbp": {
      "name": "British Pound Sterling",
      "unit": "£",
      "value": 56399.471,
      "type": "fiat"
    },
    "gel": {
      "name": "Georgian Lari",
      "unit": "₾",
      "value": 201993.691,
      "type": "fiat"
    },
    "hkd": {
      "name": "Hong Kong Dollar",
      "unit": "HK$",
      "value": 594140.994,
      "type": "fiat"
    },
    "huf": {
      "name": "Hungarian Forint",
      "unit": "Ft",
      "value": 23216805.355,
      "type": "fiat"
    },
    "idr": {
      "name": "Indonesian Rupiah",
      "unit": "Rp",
      "value": 1350406835.492,
      "type": "fiat"
    },
    "ils": {
      "name": "Israeli New Shekel",
      "unit": "₪",
      "value": 215451.345,
      "type": "fiat"
    },
    "inr": {
      "name": "Indian Rupee",
      "unit": "₹",
      "value": 7255573.761,
      "type": "fiat"
    },
    "jpy": {
      "name": "Japanese Yen",
      "unit": "¥",
      "value": 12079021.102,
      "type": "fiat"
    },
    "krw": {
      "name": "South Korean Won",
      "unit": "₩",
      "value": 114295300.075,
      "type": "fiat"
    },
    "kwd": {
      "name": "Kuwaiti Dinar",
      "unit": "KD",
      "value": 23466.584,
      "type": "fiat"
    },
    "lkr": {
      "name": "Sri Lankan Rupee",
      "unit": "Rs",
      "value": 24658404.204,
      "type": "fiat"
    },
    "mmk": {
      "name": "Burmese Kyat",
      "unit": "K",
      "value": 159202903.032,
      "type": "fiat"
    },
    "mxn": {
      "name": "Mexican Peso",
      "unit": "MX$",
      "value": 1312974.009,
      "type": "fiat"
    },
    "myr": {
      "name": "Malaysian Ringgit",
      "unit": "RM",
      "value": 300716.004,
      "type": "fiat"
    },
    "ngn": {
      "name": "Nigerian Naira",
      "unit": "₦",
      "value": 104085661.749,
      "type": "fiat"
    },
    "nok": {
      "name": "Norwegian Krone",
      "unit": "kr",
      "value": 703191.355,
      "type": "fiat"
    },
    "nzd": {
      "name": "New Zealand Dollar",
      "unit": "NZ$",
      "value": 129943.993,
      "type": "fiat"
    },
    "php": {
      "name": "Philippine Peso",
      "unit": "₱",
      "value": 4669881.64,
      "type": "fiat"
    },
    "pkr": {
      "name": "Pakistani Rupee",
      "unit": "₨",
      "value": 21107508.631,
      "type": "fiat"
    },
    "pln": {
      "name": "Polish Zloty",
      "unit": "zł",
      "value": 276389.874,
      "type": "fiat"
    },
    "rub": {
      "name": "Russian Ruble",
      "unit": "₽",
      "value": 5459045.262,
      "type": "fiat"
    },
    "sar": {
      "name": "Saudi Riyal",
      "unit": "SR",
      "value": 283561.022,
      "type": "fiat"
    },
    "sek": {
      "name": "Swedish Krona",
      "unit": "kr",
      "value": 706593.222,
      "type": "fiat"
    },
    "sgd": {
      "name": "Singapore Dollar",
      "unit": "S$",
      "value": 96873.041,
      "type": "fiat"
    },
    "thb": {
      "name": "Thai Baht",
      "unit": "฿",
      "value": 2477440.273,
      "type": "fiat"
    },
    "try": {
      "name": "Turkish Lira",
      "unit": "₺",
      "value": 3480331.296,
      "type": "fiat"
    },
    "twd": {
      "name": "New Taiwan Dollar",
      "unit": "NT$",
      "value": 2384248.866,
      "type": "fiat"
    },
    "uah": {
      "name": "Ukrainian hryvnia",
      "unit": "₴",
      "value": 3356872.299,
      "type": "fiat"
    },
    "vef": {
      "name": "Venezuelan bolívar fuerte",
      "unit": "Bs.F",
      "value": 7591.632,
      "type": "fiat"
    },
    "vnd": {
      "name": "Vietnamese đồng",
      "unit": "₫",
      "value": 1997306794.202,
      "type": "fiat"
    },
    "zar": {
      "name": "South African Rand",
      "unit": "R",
      "value": 1242588.207,
      "type": "fiat"
    },
    "xdr": {
      "name": "IMF Special Drawing Rights",
      "unit": "XDR",
      "value": 53137.563,
      "type": "fiat"
    },
    "xag": {
      "name": "Silver - Troy Ounce",
      "unit": "XAG",
      "value": 995.118,
      "type": "commodity"
    },
    "xau": {
      "name": "Gold - Troy Ounce",
      "unit": "XAU",
      "value": 16.843,
      "type": "commodity"
    },
    "bits": {
      "name": "Bits",
      "unit": "μBTC",
      "value": 1000000.0,
      "type": "crypto"
    },
    "sats": {
      "name": "Satoshi",
      "unit": "sats",
      "value": 100000000.0,
      "type": "crypto"
    },
    "cop": {
      "name": "Colombian Peso",
      "unit": "$",
      "value": 279126134.558,
      "type": "fiat"
    },
    "kes": {
      "name": "Kenyan Shilling",
      "unit": "KSh",
      "value": 9815367.857,
      "type": "fiat"
    },
    "ron": {
      "name": "Romanian Leu",
      "unit": "lei",
      "value": 341733.412,
      "type": "fiat"
    },
    "dop": {
      "name": "Dominican Peso",
      "unit": "RD$",
      "value": 4460079.423,
      "type": "fiat"
    },
    "crc": {
      "name": "Costa Rican Colón",
      "unit": "₡",
      "value": 34279241.577,
      "type": "fiat"
    },
    "hnl": {
      "name": "Honduran Lempira",
      "unit": "L",
      "value": 2016966.507,
      "type": "fiat"
    },
    "zmw": {
      "name": "Zambian Kwacha",
      "unit": "ZK",
      "value": 1419566.341,
      "type": "fiat"
    },
    "svc": {
      "name": "Salvadoran Colón",
      "unit": "₡",
      "value": 663313.856,
      "type": "fiat"
    },
    "bam": {
      "name": "Bosnia and Herzegovina Convertible Mark",
      "unit": "KM",
      "value": 127362.018,
      "type": "fiat"
    },
    "pen": {
      "name": "Peruvian Sol",
      "unit": "S/",
      "value": 258167.906,
      "type": "fiat"
    },
    "gtq": {
      "name": "Guatemalan Quetzal",
      "unit": "Q",
      "value": 578018.87,
      "type": "fiat"
    },
    "lbp": {
      "name": "Lebanese Pound",
      "unit": "ل.ل",
      "value": 6790586630.179,
      "type": "fiat"
    },
    "amd": {
      "name": "Armenian Dram",
      "unit": "֏",
      "value": 27881224.901,
      "type": "fiat"
    }
  }
}
```


# Trending-Search

To query trending search coins, NFTs and categories on CoinGecko in the last 24 hours

```java
CompletableFuture<ApiResponse<TrendingSearch>> trendingSearchAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: Trending search coins, NFTs and categories

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`TrendingSearch`](../../doc/models/trending-search.md).

## Example Usage

```java
api.trendingSearchAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "coins": [
    {
      "item": {
        "id": "bonk",
        "coin_id": 28600,
        "name": "Bonk",
        "symbol": "BONK",
        "market_cap_rank": 103,
        "thumb": "https://coin-images.coingecko.com/coins/images/28600/standard/bonk.jpg?1696527587",
        "small": "https://coin-images.coingecko.com/coins/images/28600/small/bonk.jpg?1696527587",
        "large": "https://coin-images.coingecko.com/coins/images/28600/large/bonk.jpg?1696527587",
        "slug": "bonk",
        "price_btc": 7.821066970851871E-11,
        "score": 0,
        "data": {
          "price": 5.938674704566297E-06,
          "price_btc": "0.00000000007821066970851871",
          "price_change_percentage_24h": {
            "usd": -3.2712597351582655,
            "btc": -1.2567575303632434
          },
          "market_cap": "$521,967,819",
          "market_cap_btc": "6883.418982779206",
          "total_volume": "$31,701,707",
          "total_volume_btc": "417.50253280497",
          "sparkline": "https://www.coingecko.com/coins/28600/sparkline.svg",
          "content": null
        }
      }
    }
  ],
  "nfts": [
    {
      "id": "beeple-everydays-the-2020-collection",
      "name": "BEEPLE: EVERYDAYS - THE 2020 COLLECTION",
      "symbol": "BEEPLE2",
      "thumb": "https://coin-images.coingecko.com/nft_contracts/images/1327/standard/beeple-everydays-the-2020-collection.jpg?1707287783",
      "nft_contract_id": 1327,
      "native_currency_symbol": "eth",
      "floor_price_in_native_currency": 6.98,
      "floor_price_24h_percentage_change": 8.231790820932737,
      "data": {
        "floor_price": "6.98 ETH",
        "floor_price_in_usd_24h_percentage_change": "8.231790820932737",
        "h24_volume": "6.10 ETH",
        "h24_average_sale_price": "6.10 ETH",
        "sparkline": "https://www.coingecko.com/nft/1327/sparkline.svg",
        "content": null
      }
    }
  ],
  "categories": [
    {
      "id": 102120809,
      "name": "Base Native",
      "top_3_coins_images": [
        "https://assets.coingecko.com/coins/images/40008/small/USR_LOGO.png?1725222638",
        "https://assets.coingecko.com/coins/images/13187/small/7739.png?1696512969",
        "https://assets.coingecko.com/coins/images/70556/small/elizaOS_token_logo_high_quality.png?1763494093"
      ],
      "market_cap_1h_change": 0.1591461077485745,
      "slug": "base-native",
      "coins_count": "573",
      "data": {
        "market_cap": 117316549202.14426,
        "market_cap_btc": 1545658.5276991604,
        "total_volume": 16971131961.734743,
        "total_volume_btc": 223596.5430262045,
        "market_cap_change_percentage_24h": {
          "usd": 0.14714515711689605,
          "btc": 1.5918443786835867
        },
        "sparkline": "https://www.coingecko.com/categories/102120809/sparkline.svg"
      }
    }
  ]
}
```


# Crypto-Global

To query cryptocurrency global data including active cryptocurrencies, markets, total crypto market cap and etc

```java
CompletableFuture<ApiResponse<Global>> cryptoGlobalAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: Cryptocurrency global market data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Global`](../../doc/models/global.md).

## Example Usage

```java
api.cryptoGlobalAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "active_cryptocurrencies": 17397,
    "upcoming_icos": 0,
    "ongoing_icos": 49,
    "ended_icos": 3376,
    "markets": 1476,
    "total_market_cap": {
      "btc": 34570737.199462704,
      "eth": 1259418635.423994,
      "usd": 2621040321355.0405
    },
    "total_volume": {
      "btc": 1254779.1727158197,
      "eth": 45711847.69194817,
      "usd": 95133256404.37308
    },
    "market_cap_percentage": {
      "btc": 57.9539332566265,
      "eth": 9.58227145398409,
      "usdt": 7.223241338072757
    },
    "market_cap_change_percentage_24h_usd": -1.6081983639177684,
    "volume_change_percentage_24h_usd": 33.064521460740046,
    "updated_at": 1779878351
  }
}
```


# Global-Defi

To query top 100 cryptocurrency global decentralized finance (DeFi) data including DeFi market cap, trading volume

```java
CompletableFuture<ApiResponse<GlobalDeFi>> globalDefiAsync()
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Response Type

**200**: Global decentralized finance (DeFi) market data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GlobalDeFi`](../../doc/models/global-de-fi.md).

## Example Usage

```java
api.globalDefiAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "defi_market_cap": "93264745839.10368680452390205264",
    "eth_market_cap": "250923489878.18163813287624277972",
    "defi_to_eth_ratio": "37.1685990356589832537094209337357070624927603988429231656080063710045566",
    "trading_volume_24h": "3779246981.777563895687957584391",
    "defi_dominance": "3.5568819863542411077651904276222133821656380942701140395041020219966392",
    "top_coin_name": "Lido Staked Ether",
    "top_coin_defi_dominance": 19.77898778734103
  }
}
```


# Pool-Address

To query the specific pool based on the provided network and pool address

```java
CompletableFuture<ApiResponse<PoolAddressData>> poolAddressAsync(
    final String network,
    final String address,
    final String include,
    final Boolean includeVolumeBreakdown,
    final Boolean includeComposition)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `address` | `String` | Template, Required | Pool address. |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `includeVolumeBreakdown` | `Boolean` | Query, Optional | Include volume breakdown.<br>Default: `false` |
| `includeComposition` | `Boolean` | Query, Optional | Include pool composition.<br>Default: `false` |

## Response Type

**200**: Specific pool data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PoolAddressData`](../../doc/models/pool-address-data.md).

## Example Usage

```java
String network = "eth";
String address = "0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640";

api.poolAddressAsync(network, address, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "eth_0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640",
    "type": "pool",
    "attributes": {
      "base_token_price_usd": "2087.83402802406",
      "base_token_price_native_currency": "1.0",
      "base_token_balance": "21389.8183230254",
      "base_token_liquidity_usd": "44682614.543365459190858949279370927520536805",
      "quote_token_price_usd": "1.00238840383302",
      "quote_token_price_native_currency": "0.000480112806762164",
      "quote_token_balance": "54351838.715647",
      "quote_token_liquidity_usd": "54511610.488634398923096739735612698563218038285229066528",
      "base_token_price_quote_token": "2082.843835689",
      "quote_token_price_base_token": "0.0004801128068",
      "address": "0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640",
      "name": "WETH / USDC 0.05%",
      "pool_name": "WETH / USDC",
      "pool_fee_percentage": "0.05",
      "pool_created_at": "2021-12-29T12:35:14Z",
      "fdv_usd": "4706830691.85796",
      "market_cap_usd": "4714013620.15169",
      "price_change_percentage": {
        "m5": "0.001",
        "m15": "0.339",
        "m30": "0.197",
        "h1": "0.157",
        "h6": "0.651",
        "h24": "-1.403"
      },
      "transactions": {
        "m5": {
          "buys": 13,
          "sells": 10,
          "buyers": 11,
          "sellers": 9
        },
        "m15": {
          "buys": 34,
          "sells": 40,
          "buyers": 20,
          "sellers": 26
        },
        "m30": {
          "buys": 61,
          "sells": 60,
          "buyers": 35,
          "sellers": 36
        },
        "h1": {
          "buys": 88,
          "sells": 119,
          "buyers": 52,
          "sellers": 75
        },
        "h6": {
          "buys": 473,
          "sells": 510,
          "buyers": 214,
          "sellers": 288
        },
        "h24": {
          "buys": 2443,
          "sells": 2402,
          "buyers": 876,
          "sellers": 998
        }
      },
      "volume_usd": {
        "m5": "716095.073293581",
        "m15": "4099160.04970219",
        "m30": "6269664.41220889",
        "h1": "7654944.73813995",
        "h6": "22795729.3374518",
        "h24": "126052349.380686"
      },
      "net_buy_volume_usd": {
        "m5": "25349.579300599",
        "m15": "44021.13947472",
        "m30": "785680.21125136",
        "h1": "621530.32432932",
        "h6": "768429.1331717",
        "h24": "-4911114.3005293"
      },
      "buy_volume_usd": {
        "m5": "370722.32629709",
        "m15": "2071590.59458845",
        "m30": "3527672.31173012",
        "h1": "4138237.53123463",
        "h6": "11782079.2353117",
        "h24": "60570617.5400784"
      },
      "sell_volume_usd": {
        "m5": "345372.746996491",
        "m15": "2027569.45511373",
        "m30": "2741992.10047876",
        "h1": "3516707.20690531",
        "h6": "11013650.10214",
        "h24": "65481731.8406077"
      },
      "reserve_in_usd": "99194225.032",
      "locked_liquidity_percentage": "0.0"
    },
    "relationships": {
      "base_token": {
        "data": {
          "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
          "type": "token"
        }
      },
      "quote_token": {
        "data": {
          "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
          "type": "token"
        }
      },
      "dex": {
        "data": {
          "id": "uniswap_v3",
          "type": "dex"
        }
      }
    }
  },
  "included": [
    {
      "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "type": "token",
      "attributes": {
        "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/2518/large/weth.png?1696503332",
        "coingecko_coin_id": "weth"
      }
    },
    {
      "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
      "type": "token",
      "attributes": {
        "address": "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
        "name": "USD Coin",
        "symbol": "USDC",
        "decimals": 6,
        "image_url": "https://coin-images.coingecko.com/coins/images/6319/large/USDC.png?1769615602",
        "coingecko_coin_id": "usd-coin"
      }
    },
    {
      "id": "uniswap_v3",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V3"
      }
    }
  ]
}
```


# Trending-Pools-List

To query all the trending pools across all networks on GeckoTerminal

```java
CompletableFuture<ApiResponse<Pool>> trendingPoolsListAsync(
    final String include,
    final Integer page,
    final Duration duration,
    final Boolean includeGtCommunityData)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex`, `network` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `duration` | [`Duration`](../../doc/models/duration.md) | Query, Optional | Duration to sort trending list by.<br>Default: `24h` |
| `includeGtCommunityData` | `Boolean` | Query, Optional | Include GeckoTerminal community data (sentiment votes, suspicious reports).<br>Default: `false` |

## Response Type

**200**: Trending pools across all networks

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Pool`](../../doc/models/pool.md).

## Example Usage

```java
api.trendingPoolsListAsync(null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "base_0xec33256bf1ded407a57fd3c1965e7556e42ac14db09bc4e6fef57d5e2eb0b0b9",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "0.0000738759066917531",
        "base_token_price_native_currency": "0.0000000363525310457453",
        "quote_token_price_usd": "2076.36",
        "quote_token_price_native_currency": "1.0",
        "base_token_price_quote_token": "0.00000003635253105",
        "quote_token_price_base_token": "27508400.9622774",
        "address": "0xec33256bf1ded407a57fd3c1965e7556e42ac14db09bc4e6fef57d5e2eb0b0b9",
        "name": "GITLAWB / WETH",
        "pool_created_at": "2026-03-11T02:00:07Z",
        "fdv_usd": "7378641.34604051",
        "market_cap_usd": "7387590.669",
        "price_change_percentage": {
          "m5": "-0.298",
          "m15": "-0.016",
          "m30": "-4.618",
          "h1": "-9.394",
          "h6": "-19.15",
          "h24": "-30.893"
        },
        "transactions": {
          "m5": {
            "buys": 9,
            "sells": 1,
            "buyers": 9,
            "sellers": 1
          },
          "m15": {
            "buys": 28,
            "sells": 9,
            "buyers": 22,
            "sellers": 9
          },
          "m30": {
            "buys": 100,
            "sells": 42,
            "buyers": 76,
            "sellers": 37
          },
          "h1": {
            "buys": 187,
            "sells": 77,
            "buyers": 125,
            "sellers": 62
          },
          "h6": {
            "buys": 396,
            "sells": 206,
            "buyers": 237,
            "sellers": 159
          },
          "h24": {
            "buys": 1827,
            "sells": 1119,
            "buyers": 874,
            "sellers": 642
          }
        },
        "volume_usd": {
          "m5": "4903.1102054097",
          "m15": "10538.6429382093",
          "m30": "79639.1969896469",
          "h1": "144469.00760098",
          "h6": "361229.128078271",
          "h24": "2108583.76373177"
        },
        "reserve_in_usd": "2471839.0983",
        "sentiment_vote_positive_percentage": 83.33333333333334,
        "sentiment_vote_negative_percentage": 16.666666666666664,
        "community_sus_report": 6
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "base_0x5f980dcfc4c0fa3911554cf5ab288ed0eb13dba3",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "base_0x4200000000000000000000000000000000000006",
            "type": "token"
          }
        },
        "network": {
          "data": {
            "id": "base",
            "type": "network"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap-v4-base",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "base_0x5f980dcfc4c0fa3911554cf5ab288ed0eb13dba3",
      "type": "token",
      "attributes": {
        "address": "0x5f980dcfc4c0fa3911554cf5ab288ed0eb13dba3",
        "name": "gitlawb",
        "symbol": "GITLAWB",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/102172941/large/b16bfbf1-8384-43fc-9797-88fba91ddca5.png?1776736251",
        "coingecko_coin_id": "gitlawb"
      }
    },
    {
      "id": "base_0x4200000000000000000000000000000000000006",
      "type": "token",
      "attributes": {
        "address": "0x4200000000000000000000000000000000000006",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/39810/large/weth.png?1724139790",
        "coingecko_coin_id": "l2-standard-bridged-weth-base"
      }
    },
    {
      "id": "uniswap-v4-base",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V4 (Base)"
      }
    },
    {
      "id": "base",
      "type": "network",
      "attributes": {
        "name": "Base",
        "coingecko_asset_platform_id": "base"
      }
    }
  ]
}
```


# Trending-Pools-Network

To query the trending pools based on the provided network

```java
CompletableFuture<ApiResponse<Pool>> trendingPoolsNetworkAsync(
    final String network,
    final String include,
    final Integer page,
    final Duration duration,
    final Boolean includeGtCommunityData)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `duration` | [`Duration`](../../doc/models/duration.md) | Query, Optional | Duration to sort trending list by.<br>Default: `24h` |
| `includeGtCommunityData` | `Boolean` | Query, Optional | Include GeckoTerminal community data (sentiment votes, suspicious reports).<br>Default: `false` |

## Response Type

**200**: Trending pools on a network

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Pool`](../../doc/models/pool.md).

## Example Usage

```java
String network = "eth";

api.trendingPoolsNetworkAsync(network, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_0x76a411f14a704099ba476ce8dffc288a53295218",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "0.000157869028295179",
        "base_token_price_native_currency": "0.000000076174152494787",
        "quote_token_price_usd": "2066.59098774463",
        "quote_token_price_native_currency": "1.0",
        "base_token_price_quote_token": "0.00000007617415249",
        "quote_token_price_base_token": "13127812.6142386",
        "address": "0x76a411f14a704099ba476ce8dffc288a53295218",
        "name": "ASTEROID / WETH",
        "pool_created_at": "2024-09-10T10:18:23Z",
        "fdv_usd": "66412125.220192",
        "market_cap_usd": "66413921.515527",
        "price_change_percentage": {
          "m5": "-0.355",
          "m15": "-0.228",
          "m30": "0.284",
          "h1": "-4.605",
          "h6": "-13.908",
          "h24": "-20.721"
        },
        "transactions": {
          "m5": {
            "buys": 7,
            "sells": 4,
            "buyers": 7,
            "sellers": 4
          },
          "m15": {
            "buys": 24,
            "sells": 11,
            "buyers": 24,
            "sellers": 11
          },
          "m30": {
            "buys": 62,
            "sells": 40,
            "buyers": 54,
            "sellers": 34
          },
          "h1": {
            "buys": 218,
            "sells": 174,
            "buyers": 153,
            "sellers": 116
          },
          "h6": {
            "buys": 784,
            "sells": 520,
            "buyers": 422,
            "sellers": 344
          },
          "h24": {
            "buys": 3175,
            "sells": 2431,
            "buyers": 1290,
            "sellers": 1169
          }
        },
        "volume_usd": {
          "m5": "5610.858166059",
          "m15": "10926.8813342462",
          "m30": "92508.9175387338",
          "h1": "471159.035768368",
          "h6": "1738275.01961596",
          "h24": "7900631.31777918"
        },
        "reserve_in_usd": "2471711.2255",
        "sentiment_vote_positive_percentage": 0,
        "sentiment_vote_negative_percentage": 0,
        "community_sus_report": 4
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0xf280b16ef293d8e534e370794ef26bf312694126",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap_v2",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "eth_0xf280b16ef293d8e534e370794ef26bf312694126",
      "type": "token",
      "attributes": {
        "address": "0xf280b16ef293d8e534e370794ef26bf312694126",
        "name": "Asteroid Shiba",
        "symbol": "ASTEROID",
        "decimals": 9,
        "image_url": "https://coin-images.coingecko.com/coins/images/50333/large/IMG_0728.jpeg?1727384521",
        "coingecko_coin_id": "asteroid-shiba"
      }
    },
    {
      "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "type": "token",
      "attributes": {
        "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/2518/large/weth.png?1696503332",
        "coingecko_coin_id": "weth"
      }
    },
    {
      "id": "uniswap_v2",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V2"
      }
    }
  ]
}
```


# Top-Pools-Network

To query all the top pools based on the provided network

```java
CompletableFuture<ApiResponse<Pool>> topPoolsNetworkAsync(
    final String network,
    final String include,
    final Integer page,
    final Sort sort,
    final Boolean includeGtCommunityData)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `sort` | [`Sort`](../../doc/models/sort.md) | Query, Optional | Sort the pools by field.<br>Default: `h24_tx_count_desc` |
| `includeGtCommunityData` | `Boolean` | Query, Optional | Include GeckoTerminal community data (sentiment votes, suspicious reports).<br>Default: `false` |

## Response Type

**200**: Top pools on a network

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Pool`](../../doc/models/pool.md).

## Example Usage

```java
String network = "eth";

api.topPoolsNetworkAsync(network, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_0xe0554a476a092703abdb3ef35c80e0d76d32939f",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "1.00416362400354",
        "base_token_price_native_currency": "0.000486360749106006",
        "quote_token_price_usd": "2062.64658353477",
        "quote_token_price_native_currency": "1.0",
        "base_token_price_quote_token": "0.0004863607491",
        "quote_token_price_base_token": "2056.086972146",
        "address": "0xe0554a476a092703abdb3ef35c80e0d76d32939f",
        "name": "USDC / WETH 0.01%",
        "pool_created_at": "2021-12-30T20:32:10Z",
        "fdv_usd": "52795390278.303",
        "market_cap_usd": "76649272425.414",
        "price_change_percentage": {
          "m5": "0.355",
          "m15": "0.217",
          "m30": "0.422",
          "h1": "-0.011",
          "h6": "0.521",
          "h24": "0.621"
        },
        "transactions": {
          "m5": {
            "buys": 46,
            "sells": 47,
            "buyers": 29,
            "sellers": 37
          },
          "m15": {
            "buys": 125,
            "sells": 133,
            "buyers": 90,
            "sellers": 98
          },
          "m30": {
            "buys": 216,
            "sells": 208,
            "buyers": 148,
            "sellers": 139
          },
          "h1": {
            "buys": 429,
            "sells": 521,
            "buyers": 277,
            "sellers": 286
          },
          "h6": {
            "buys": 2174,
            "sells": 2154,
            "buyers": 1195,
            "sellers": 956
          },
          "h24": {
            "buys": 8688,
            "sells": 8756,
            "buyers": 3656,
            "sellers": 2830
          }
        },
        "volume_usd": {
          "m5": "295843.242851232",
          "m15": "610802.206180104",
          "m30": "1007505.50492217",
          "h1": "3248217.38569341",
          "h6": "12299601.042572",
          "h24": "39081025.0003669"
        },
        "reserve_in_usd": "4558978.8435",
        "sentiment_vote_positive_percentage": 0,
        "sentiment_vote_negative_percentage": 0,
        "community_sus_report": 2
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap_v3",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
      "type": "token",
      "attributes": {
        "address": "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
        "name": "USD Coin",
        "symbol": "USDC",
        "decimals": 6,
        "image_url": "https://coin-images.coingecko.com/coins/images/6319/large/USDC.png?1769615602",
        "coingecko_coin_id": "usd-coin"
      }
    },
    {
      "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "type": "token",
      "attributes": {
        "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/2518/large/weth.png?1696503332",
        "coingecko_coin_id": "weth"
      }
    },
    {
      "id": "uniswap_v3",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V3"
      }
    }
  ]
}
```


# Top-Pools-Dex

To query all the top pools based on the provided network and decentralized exchange (DEX)

```java
CompletableFuture<ApiResponse<Pool>> topPoolsDexAsync(
    final String network,
    final String dex,
    final String include,
    final Integer page,
    final Sort sort,
    final Boolean includeGtCommunityData)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `dex` | `String` | Template, Required | DEX ID.<br>*refers to [`/onchain/networks/{network}/dexes`](/reference/dexes-list). |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `sort` | [`Sort`](../../doc/models/sort.md) | Query, Optional | Sort the pools by field.<br>Default: `h24_tx_count_desc` |
| `includeGtCommunityData` | `Boolean` | Query, Optional | Include GeckoTerminal community data (sentiment votes, suspicious reports).<br>Default: `false` |

## Response Type

**200**: Top pools on a network's DEX

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Pool`](../../doc/models/pool.md).

## Example Usage

```java
String network = "eth";
String dex = "sushiswap";

api.topPoolsDexAsync(network, dex, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_0x6469b34a2a4723163c4902dbbdea728d20693c12",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "2.53037158380141",
        "base_token_price_native_currency": "0.00122586914090918",
        "quote_token_price_usd": "2062.57293793663",
        "quote_token_price_native_currency": "1.0",
        "base_token_price_quote_token": "0.001225869141",
        "quote_token_price_base_token": "815.74775531",
        "address": "0x6469b34a2a4723163c4902dbbdea728d20693c12",
        "name": "NEAR / WETH",
        "pool_created_at": "2021-10-11T01:52:05Z",
        "fdv_usd": "8774304.71122981",
        "market_cap_usd": "8774304.71122981",
        "price_change_percentage": {
          "m5": "0",
          "m15": "0",
          "m30": "0.049",
          "h1": "0.428",
          "h6": "-0.885",
          "h24": "-12.097"
        },
        "transactions": {
          "m5": {
            "buys": 0,
            "sells": 0,
            "buyers": 0,
            "sellers": 0
          },
          "m15": {
            "buys": 0,
            "sells": 0,
            "buyers": 0,
            "sellers": 0
          },
          "m30": {
            "buys": 1,
            "sells": 2,
            "buyers": 1,
            "sellers": 2
          },
          "h1": {
            "buys": 6,
            "sells": 4,
            "buyers": 2,
            "sellers": 3
          },
          "h6": {
            "buys": 39,
            "sells": 37,
            "buyers": 24,
            "sellers": 16
          },
          "h24": {
            "buys": 172,
            "sells": 180,
            "buyers": 62,
            "sellers": 55
          }
        },
        "volume_usd": {
          "m5": "0.0",
          "m15": "0.0",
          "m30": "215.04729883",
          "h1": "572.0025141642",
          "h6": "7298.4165779336",
          "h24": "38207.6214949268"
        },
        "reserve_in_usd": "54784.7204",
        "sentiment_vote_positive_percentage": 0,
        "sentiment_vote_negative_percentage": 0,
        "community_sus_report": 0
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0x85f17cf997934a597031b2e18a9ab6ebd4b9f6a4",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "sushiswap",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "eth_0x85f17cf997934a597031b2e18a9ab6ebd4b9f6a4",
      "type": "token",
      "attributes": {
        "address": "0x85f17cf997934a597031b2e18a9ab6ebd4b9f6a4",
        "name": "NEAR",
        "symbol": "NEAR",
        "decimals": 24,
        "image_url": "https://coin-images.coingecko.com/coins/images/71681/large/near.png?1768905174",
        "coingecko_coin_id": "rainbow-bridged-near-ethereum"
      }
    },
    {
      "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "type": "token",
      "attributes": {
        "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/2518/large/weth.png?1696503332",
        "coingecko_coin_id": "weth"
      }
    },
    {
      "id": "sushiswap",
      "type": "dex",
      "attributes": {
        "name": "SushiSwap"
      }
    }
  ]
}
```


# Top-Pools-Contract-Address

To query top pools based on the provided token contract address on a network

```java
CompletableFuture<ApiResponse<Pool>> topPoolsContractAddressAsync(
    final String network,
    final String tokenAddress,
    final String include,
    final Boolean includeInactiveSource,
    final Integer page,
    final Sort2 sort,
    final Boolean includeGtCommunityData)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `tokenAddress` | `String` | Template, Required | Token contract address. |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `includeInactiveSource` | `Boolean` | Query, Optional | Include tokens from inactive pools using the most recent swap.<br>Default: `false` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `sort` | [`Sort2`](../../doc/models/sort-2.md) | Query, Optional | Sort the pools by field.<br>Default: `h24_volume_usd_liquidity_desc` |
| `includeGtCommunityData` | `Boolean` | Query, Optional | Include GeckoTerminal community data (sentiment votes, suspicious reports).<br>Default: `false` |

## Response Type

**200**: Top pools for a token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Pool`](../../doc/models/pool.md).

## Example Usage

```java
String network = "eth";
String tokenAddress = "0xdac17f958d2ee523a2206206994597c13d831ec7";

api.topPoolsContractAddressAsync(network, tokenAddress, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_0x395f91b34aa34a477ce3bc6505639a821b286a62b1a164fc1887fa3a5ef713a5",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "1.0008763651",
        "base_token_price_native_currency": "0.000482317790072442",
        "quote_token_price_usd": "0.998449563724543",
        "quote_token_price_native_currency": "0.000481148325490986",
        "base_token_price_quote_token": "1.0024305698",
        "quote_token_price_base_token": "0.9975753236",
        "address": "0x395f91b34aa34a477ce3bc6505639a821b286a62b1a164fc1887fa3a5ef713a5",
        "name": "USDC / USDT",
        "pool_created_at": "2025-04-13T14:45:47Z",
        "token_price_usd": "0.998449563724543",
        "fdv_usd": "96921299344.3568",
        "market_cap_usd": "189288747230.058",
        "price_change_percentage": {
          "m5": "0",
          "m15": "-0.08",
          "m30": "-0.02",
          "h1": "-0.55",
          "h6": "0.23",
          "h24": "-0.21"
        },
        "transactions": {
          "m5": {
            "buys": 1,
            "sells": 0,
            "buyers": 1,
            "sellers": 0
          },
          "m15": {
            "buys": 2,
            "sells": 13,
            "buyers": 2,
            "sellers": 12
          },
          "m30": {
            "buys": 16,
            "sells": 22,
            "buyers": 15,
            "sellers": 21
          },
          "h1": {
            "buys": 44,
            "sells": 50,
            "buyers": 41,
            "sellers": 46
          },
          "h6": {
            "buys": 306,
            "sells": 373,
            "buyers": 240,
            "sellers": 305
          },
          "h24": {
            "buys": 1062,
            "sells": 1217,
            "buyers": 677,
            "sellers": 803
          }
        },
        "volume_usd": {
          "m5": "100.4170370205",
          "m15": "44354.6645720277",
          "m30": "2972422.02951497",
          "h1": "6273480.14455755",
          "h6": "31080731.7699018",
          "h24": "65665560.4792908"
        },
        "reserve_in_usd": "545933958.0815",
        "sentiment_vote_positive_percentage": 0,
        "sentiment_vote_negative_percentage": 0,
        "community_sus_report": 2
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0xdac17f958d2ee523a2206206994597c13d831ec7",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap-v4-ethereum",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
      "type": "token",
      "attributes": {
        "address": "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
        "name": "USD Coin",
        "symbol": "USDC",
        "decimals": 6,
        "image_url": "https://coin-images.coingecko.com/coins/images/6319/large/USDC.png?1769615602",
        "coingecko_coin_id": "usd-coin"
      }
    },
    {
      "id": "eth_0xdac17f958d2ee523a2206206994597c13d831ec7",
      "type": "token",
      "attributes": {
        "address": "0xdac17f958d2ee523a2206206994597c13d831ec7",
        "name": "Tether USD",
        "symbol": "USDT",
        "decimals": 6,
        "image_url": "https://coin-images.coingecko.com/coins/images/325/large/Tether.png?1696501661",
        "coingecko_coin_id": "tether"
      }
    },
    {
      "id": "uniswap-v4-ethereum",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V4 (Ethereum)"
      }
    }
  ]
}
```


# Token-Data-Contract-Address

To query specific token data based on the provided token contract address on a network

```java
CompletableFuture<ApiResponse<TokenData>> tokenDataContractAddressAsync(
    final String network,
    final String address,
    final Include include,
    final Boolean includeComposition,
    final Boolean includeInactiveSource)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `address` | `String` | Template, Required | Token contract address. |
| `include` | [`Include`](../../doc/models/include.md) | Query, Optional | Attributes to include. |
| `includeComposition` | `Boolean` | Query, Optional | Include pool composition.<br>Default: `false` |
| `includeInactiveSource` | `Boolean` | Query, Optional | Include token data from inactive pools using the most recent swap.<br>Default: `false` |

## Response Type

**200**: Token data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`TokenData`](../../doc/models/token-data.md).

## Example Usage

```java
String network = "eth";
String address = "0xdac17f958d2ee523a2206206994597c13d831ec7";

api.tokenDataContractAddressAsync(network, address, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "eth_0xdac17f958d2ee523a2206206994597c13d831ec7",
    "type": "token",
    "attributes": {
      "address": "0xdac17f958d2ee523a2206206994597c13d831ec7",
      "name": "Tether USD",
      "symbol": "USDT",
      "decimals": 6,
      "image_url": "https://coin-images.coingecko.com/coins/images/325/large/Tether.png?1696501661",
      "coingecko_coin_id": "tether",
      "total_supply": "97071854588430319.0",
      "normalized_total_supply": "97071854588.4303",
      "price_usd": "0.9976477279",
      "fdv_usd": "96843463696.399",
      "total_reserve_in_usd": "2701052887.0071499413427031774184",
      "volume_usd": {
        "h24": "572433180.559528"
      },
      "market_cap_usd": "189135294432.762",
      "last_trade_timestamp": "1779897731"
    },
    "relationships": {
      "top_pools": {
        "data": [
          {
            "id": "eth_0x395f91b34aa34a477ce3bc6505639a821b286a62b1a164fc1887fa3a5ef713a5",
            "type": "pool"
          }
        ]
      }
    }
  },
  "included": [
    {
      "id": "eth_0x395f91b34aa34a477ce3bc6505639a821b286a62b1a164fc1887fa3a5ef713a5",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "1.00076841159283",
        "base_token_price_native_currency": "0.000482652821375511",
        "quote_token_price_usd": "0.99764772791269",
        "quote_token_price_native_currency": "0.000481147771090756",
        "base_token_price_quote_token": "1.0031280417",
        "quote_token_price_base_token": "0.9968817124",
        "address": "0x395f91b34aa34a477ce3bc6505639a821b286a62b1a164fc1887fa3a5ef713a5",
        "name": "USDC / USDT",
        "pool_created_at": "2025-04-13T14:45:47Z",
        "token_price_usd": "0.99764772791269",
        "fdv_usd": "96843463696.399",
        "market_cap_usd": "189136733045.442",
        "price_change_percentage": {
          "m5": "0.74",
          "m15": "0.52",
          "m30": "0.41",
          "h1": "0.49",
          "h6": "0.73",
          "h24": "0.1"
        },
        "transactions": {
          "m5": {
            "buys": 0,
            "sells": 6,
            "buyers": 0,
            "sellers": 6
          },
          "m15": {
            "buys": 11,
            "sells": 23,
            "buyers": 11,
            "sellers": 13
          },
          "m30": {
            "buys": 15,
            "sells": 41,
            "buyers": 15,
            "sellers": 28
          },
          "h1": {
            "buys": 53,
            "sells": 60,
            "buyers": 50,
            "sellers": 45
          },
          "h6": {
            "buys": 314,
            "sells": 393,
            "buyers": 247,
            "sellers": 311
          },
          "h24": {
            "buys": 1066,
            "sells": 1219,
            "buyers": 682,
            "sellers": 800
          }
        },
        "volume_usd": {
          "m5": "5390.4353119892",
          "m15": "73424.879752289",
          "m30": "2984135.66431702",
          "h1": "6251379.50994286",
          "h6": "31152723.862617",
          "h24": "64799943.9574331"
        },
        "reserve_in_usd": "548688496.6398",
        "last_trade_timestamp": "1779897791"
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0xdac17f958d2ee523a2206206994597c13d831ec7",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap-v4-ethereum",
            "type": "dex"
          }
        }
      }
    }
  ]
}
```


# Tokens-Data-Contract-Addresses

To query multiple tokens data based on the provided token contract addresses on a network

```java
CompletableFuture<ApiResponse<MultiTokenData>> tokensDataContractAddressesAsync(
    final String network,
    final String addresses,
    final Include include,
    final Boolean includeComposition,
    final Boolean includeInactiveSource)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `addresses` | `String` | Template, Required | Token contract address, comma-separated if more than one token contract address. |
| `include` | [`Include`](../../doc/models/include.md) | Query, Optional | Attributes to include. |
| `includeComposition` | `Boolean` | Query, Optional | Include pool composition.<br>Default: `false` |
| `includeInactiveSource` | `Boolean` | Query, Optional | Include tokens from inactive pools using the most recent swap.<br>Default: `false` |

## Response Type

**200**: Multiple tokens data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`MultiTokenData`](../../doc/models/multi-token-data.md).

## Example Usage

```java
String network = "solana";
String addresses = "6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN,2g4LS3y2myPe6vj9wTvoBE1wKqxvhnZPoZA9QU9upump";

api.tokensDataContractAddressesAsync(network, addresses, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "solana_6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN",
      "type": "token",
      "attributes": {
        "address": "6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN",
        "name": "OFFICIAL TRUMP",
        "symbol": "TRUMP",
        "decimals": 6,
        "image_url": "https://coin-images.coingecko.com/coins/images/53746/large/trump.png?1737171561",
        "coingecko_coin_id": "official-trump",
        "total_supply": "999999108407137.0",
        "normalized_total_supply": "999999108.407137",
        "price_usd": "2.0174050182",
        "fdv_usd": "2017403219.4789",
        "total_reserve_in_usd": "38853273.6350283264033294",
        "volume_usd": {
          "h24": "2099707.5067169"
        },
        "market_cap_usd": "478960276.377951"
      },
      "relationships": {
        "top_pools": {
          "data": [
            {
              "id": "solana_9d9mb8kooFfaD3SctgZtkxQypkshx6ezhbKio89ixyy2",
              "type": "pool"
            }
          ]
        }
      }
    },
    {
      "id": "solana_2g4LS3y2myPe6vj9wTvoBE1wKqxvhnZPoZA9QU9upump",
      "type": "token",
      "attributes": {
        "address": "2g4LS3y2myPe6vj9wTvoBE1wKqxvhnZPoZA9QU9upump",
        "name": "SORACAT",
        "symbol": "SORACAT",
        "decimals": 6,
        "image_url": "https://assets.geckoterminal.com/o6djbxjg7ne8k1swjpybmdvtu11s",
        "coingecko_coin_id": null,
        "total_supply": "1000000000000000.0",
        "normalized_total_supply": "1000000000.0",
        "price_usd": null,
        "fdv_usd": null,
        "total_reserve_in_usd": "5234.61248798976042147487629165",
        "volume_usd": {
          "h24": "0.0"
        },
        "market_cap_usd": null,
        "launchpad_details": {
          "graduation_percentage": 2.16,
          "completed": false,
          "completed_at": null,
          "migrated_destination_pool_address": null
        }
      },
      "relationships": {
        "top_pools": {
          "data": []
        }
      }
    }
  ],
  "included": [
    {
      "id": "solana_9d9mb8kooFfaD3SctgZtkxQypkshx6ezhbKio89ixyy2",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "2.01740501818281139006336492319318380811954562178395002842369476",
        "base_token_price_native_currency": "0.0239250580677484",
        "quote_token_price_usd": "0.999569304917712897234320781454435071561674967628724909109738",
        "quote_token_price_native_currency": "0.0118488106949705",
        "base_token_price_quote_token": "2.0191948951",
        "quote_token_price_base_token": "0.4952468939",
        "address": "9d9mb8kooFfaD3SctgZtkxQypkshx6ezhbKio89ixyy2",
        "name": "TRUMP / USDC",
        "pool_created_at": "2025-01-18T10:39:31Z",
        "fdv_usd": "2017403219.49608",
        "market_cap_usd": "478960276.377951",
        "price_change_percentage": {
          "m5": "0",
          "m15": "-0.065",
          "m30": "-0.321",
          "h1": "0.023",
          "h6": "0.217",
          "h24": "-0.584"
        },
        "transactions": {
          "m5": {
            "buys": 0,
            "sells": 0,
            "buyers": 0,
            "sellers": 0
          },
          "m15": {
            "buys": 0,
            "sells": 2,
            "buyers": 0,
            "sellers": 2
          },
          "m30": {
            "buys": 4,
            "sells": 5,
            "buyers": 3,
            "sellers": 2
          },
          "h1": {
            "buys": 10,
            "sells": 22,
            "buyers": 6,
            "sellers": 7
          },
          "h6": {
            "buys": 61,
            "sells": 90,
            "buyers": 26,
            "sellers": 25
          },
          "h24": {
            "buys": 252,
            "sells": 327,
            "buyers": 64,
            "sellers": 60
          }
        },
        "volume_usd": {
          "m5": "0.0",
          "m15": "597.6697876563",
          "m30": "11191.1430985437",
          "h1": "22383.1305344185",
          "h6": "149655.009727483",
          "h24": "524824.856290105"
        },
        "reserve_in_usd": "34848559.9613"
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "solana_6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "solana_EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "meteora",
            "type": "dex"
          }
        }
      }
    }
  ]
}
```


# Token-Info-Contract-Address

To query token metadata (name, symbol, CoinGecko ID, image, socials, websites, description, etc.) based on a provided token contract address on a network

```java
CompletableFuture<ApiResponse<TokenInfo>> tokenInfoContractAddressAsync(
    final String network,
    final String address)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `address` | `String` | Template, Required | Token contract address. |

## Response Type

**200**: Token info data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`TokenInfo`](../../doc/models/token-info.md).

## Example Usage

```java
String network = "solana";
String address = "Dfh5DzRgSvvCFDoYc2ciTkMrbDfRKybA4SoFbPmApump";

api.tokenInfoContractAddressAsync(network, address).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "solana_Dfh5DzRgSvvCFDoYc2ciTkMrbDfRKybA4SoFbPmApump",
    "type": "token",
    "attributes": {
      "address": "Dfh5DzRgSvvCFDoYc2ciTkMrbDfRKybA4SoFbPmApump",
      "name": "Pippin",
      "symbol": "pippin",
      "decimals": 6,
      "image_url": "https://coin-images.coingecko.com/coins/images/51589/large/pippin_logo.png?1731570163",
      "image": {
        "thumb": "https://coin-images.coingecko.com/coins/images/51589/thumb/pippin_logo.png?1731570163",
        "small": "https://coin-images.coingecko.com/coins/images/51589/small/pippin_logo.png?1731570163",
        "large": "https://coin-images.coingecko.com/coins/images/51589/large/pippin_logo.png?1731570163"
      },
      "banner_image_url": "https://assets.geckoterminal.com/kn680ou6904r03syp0ecu52ihy9c",
      "coingecko_coin_id": "pippin",
      "websites": [
        "https://pippin.love",
        "https://www.yohei.me"
      ],
      "discord_url": null,
      "farcaster_url": null,
      "zora_url": null,
      "telegram_handle": "ThePippinCo",
      "twitter_handle": "pippinlovesyou",
      "description": "Pippin is an SVG unicorn drawn using the latest LLM benchmarks on ChatGPT 4o. It is an autonomous AI agent on X.",
      "gt_score": 86.54440366972477,
      "gt_score_details": {
        "pool": 87.5,
        "transaction": 66.667,
        "creation": 100.0,
        "info": 100.0,
        "holders": 100.0
      },
      "gt_verified": true,
      "categories": [
        "Pump Fun",
        "Ai Agents"
      ],
      "gt_category_ids": [
        "pump-fun",
        "ai-agents"
      ],
      "holders": {
        "count": 47911,
        "distribution_percentage": {
          "top_10": "73.7977",
          "11_20": "8.7309",
          "21_40": "5.6147",
          "rest": "11.8567"
        },
        "last_updated": "2026-05-27T17:41:13Z"
      },
      "mint_authority": "no",
      "freeze_authority": "no",
      "is_honeypot": "unknown",
      "developer_address": "4t7dHZcUzNC96d79won5TRZsvwP1bumhPNf3awR5BHdu",
      "developer_holding_percentage": "0.0"
    }
  }
}
```


# Pool-Token-Info-Contract-Address

To query pool metadata (base and quote token details, image, socials, websites, description, contract address, etc.) based on a provided pool contract address on a network

```java
CompletableFuture<ApiResponse<PoolTokensInfo>> poolTokenInfoContractAddressAsync(
    final String network,
    final String poolAddress,
    final Include2 include)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `poolAddress` | `String` | Template, Required | Pool contract address. |
| `include` | [`Include2`](../../doc/models/include-2.md) | Query, Optional | Attributes to include. |

## Response Type

**200**: Pool tokens info data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PoolTokensInfo`](../../doc/models/pool-tokens-info.md).

## Example Usage

```java
String network = "solana";
String poolAddress = "8WwcNqdZjCY5Pt7AkhupAFknV2txca9sq6YBkGzLbvdt";

api.poolTokenInfoContractAddressAsync(network, poolAddress, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Tokens-Info-Recent-Updated

To query 100 most recently updated tokens info of a specific network or across all networks on GeckoTerminal

```java
CompletableFuture<ApiResponse<TokenInfoRecentlyUpdated>> tokensInfoRecentUpdatedAsync(
    final Include3 include,
    final String network)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `include` | [`Include3`](../../doc/models/include-3.md) | Query, Optional | Attributes for related resources to include. |
| `network` | `String` | Query, Optional | Filter tokens by provided network.<br>*refers to [`/onchain/networks`](/reference/networks-list). |

## Response Type

**200**: Most recently updated tokens info

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`TokenInfoRecentlyUpdated`](../../doc/models/token-info-recently-updated.md).

## Example Usage

```java
api.tokensInfoRecentUpdatedAsync(null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "ton_EQDCSrwrZPe4ZW-OBU1vxxalRxDeozKl_mU9Onhj-amUwHD-",
      "type": "token",
      "attributes": {
        "address": "EQDCSrwrZPe4ZW-OBU1vxxalRxDeozKl_mU9Onhj-amUwHD-",
        "name": "abrdn Physical Platinum Shares xStock",
        "symbol": "PPLTx",
        "decimals": 9,
        "image_url": "https://coin-images.coingecko.com/coins/images/102171960/large/Ticker_PPLTx__Company_Name_Physical_Platinum_Shares_ETF__Size_64x64.png?1770653933",
        "coingecko_coin_id": "abrdn-physical-platinum-shares-xstock",
        "websites": [
          "https://xstocks.fi"
        ],
        "discord_url": null,
        "farcaster_url": null,
        "zora_url": null,
        "telegram_handle": "xstocksfi",
        "twitter_handle": "xstocksfi",
        "description": "For too long, investing has come with barriers. Borders. Brokers. Limitations.",
        "gt_score": null,
        "metadata_updated_at": "2026-05-28T01:52:27Z"
      },
      "relationships": {
        "network": {
          "data": {
            "id": "ton",
            "type": "network"
          }
        }
      }
    },
    {
      "id": "solana_Xst6eFD4YT6sz9RLMysN9SyvaZWtraSdVJQGu5ZkAme",
      "type": "token",
      "attributes": {
        "address": "Xst6eFD4YT6sz9RLMysN9SyvaZWtraSdVJQGu5ZkAme",
        "name": "abrdn Physical Platinum Shares xStock",
        "symbol": "PPLTx",
        "decimals": 8,
        "image_url": "https://coin-images.coingecko.com/coins/images/102171960/large/Ticker_PPLTx__Company_Name_Physical_Platinum_Shares_ETF__Size_64x64.png?1770653933",
        "coingecko_coin_id": "abrdn-physical-platinum-shares-xstock",
        "websites": [
          "https://xstocks.fi"
        ],
        "discord_url": null,
        "farcaster_url": null,
        "zora_url": null,
        "telegram_handle": "xstocksfi",
        "twitter_handle": "xstocksfi",
        "description": "For too long, investing has come with barriers. Borders. Brokers. Limitations.",
        "gt_score": null,
        "metadata_updated_at": "2026-05-28T01:52:27Z"
      },
      "relationships": {
        "network": {
          "data": {
            "id": "solana",
            "type": "network"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "ton",
      "type": "network",
      "attributes": {
        "name": "TON",
        "coingecko_asset_platform_id": "the-open-network"
      }
    },
    {
      "id": "solana",
      "type": "network",
      "attributes": {
        "name": "Solana",
        "coingecko_asset_platform_id": "solana"
      }
    }
  ]
}
```


# Pool-Ohlcv-Contract-Address

To get the OHLCV chart (Open, High, Low, Close, Volume) of a pool based on the provided pool address on a network

```java
CompletableFuture<ApiResponse<Ohlcv>> poolOhlcvContractAddressAsync(
    final String network,
    final String poolAddress,
    final Timeframe timeframe,
    final String aggregate,
    final Integer beforeTimestamp,
    final Integer limit,
    final Currency currency,
    final String token,
    final Boolean includeEmptyIntervals)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `poolAddress` | `String` | Template, Required | Pool contract address. |
| `timeframe` | [`Timeframe`](../../doc/models/timeframe.md) | Template, Required | Timeframe of the OHLCV chart. |
| `aggregate` | `String` | Query, Optional | Time period to aggregate each OHLCV.<br>Available values (day): `1`<br>Available values (hour): `1`, `4`, `12`<br>Available values (minute): `1`, `5`, `15`<br>Default value: 1 |
| `beforeTimestamp` | `Integer` | Query, Optional | Return OHLCV data before this timestamp (integer seconds since epoch). |
| `limit` | `Integer` | Query, Optional | Number of OHLCV results to return, maximum 1000.<br>Default value: 100 |
| `currency` | [`Currency`](../../doc/models/currency.md) | Query, Optional | Return OHLCV in USD or quote token.<br>Default: `usd` |
| `token` | `String` | Query, Optional | Return OHLCV for token, use this to invert the chart.<br>Available values: `base`, `quote`, or token address.<br>Default: `base` |
| `includeEmptyIntervals` | `Boolean` | Query, Optional | Include empty intervals with no trade data.<br>Default: `false` |

## Response Type

**200**: Pool OHLCV chart data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Ohlcv`](../../doc/models/ohlcv.md).

## Example Usage

```java
String network = "eth";
String poolAddress = "0x06da0fd433c1a5d7a4faa01111c044910a184553";
Timeframe timeframe = Timeframe.DAY;

api.poolOhlcvContractAddressAsync(network, poolAddress, timeframe, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "c2728da2-1bc8-4b3a-94ca-6248a3c6e966",
    "type": "ohlcv_request_response",
    "attributes": {
      "ohlcv_list": [
        [
          1779926400,
          1.00208165944741,
          1.00257871811779,
          0.985925654401274,
          1.00027690571219,
          3481.679733097695
        ],
        [
          1779840000,
          0.996152188066521,
          1.0040610548489,
          0.996152188066521,
          1.00208165944741,
          11911.669491500581
        ]
      ]
    }
  },
  "meta": {
    "base": {
      "name": "Tether USD",
      "symbol": "USDT",
      "coingecko_coin_id": "tether",
      "address": "0xdac17f958d2ee523a2206206994597c13d831ec7"
    },
    "quote": {
      "name": "Wrapped Ether",
      "symbol": "WETH",
      "coingecko_coin_id": "weth",
      "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2"
    }
  }
}
```


# Pool-Trades-Contract-Address

To query the last 300 trades in the past 24 hours based on the provided pool address

```java
CompletableFuture<ApiResponse<Trades>> poolTradesContractAddressAsync(
    final String network,
    final String poolAddress,
    final Double tradeVolumeInUsdGreaterThan,
    final String token)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `poolAddress` | `String` | Template, Required | Pool contract address. |
| `tradeVolumeInUsdGreaterThan` | [`Double`](../../doc/models/precision.md) | Query, Optional | Filter trades by trade volume in USD greater than this value.<br>Default value: 0 |
| `token` | `String` | Query, Optional | Return trades for token, use this to invert the chart.<br>Available values: `base`, `quote`, or token address.<br>Default: `base` |

## Response Type

**200**: Last 300 trades in past 24 hours from a pool

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Trades`](../../doc/models/trades.md).

## Example Usage

```java
String network = "eth";
String poolAddress = "0x06da0fd433c1a5d7a4faa01111c044910a184553";

api.poolTradesContractAddressAsync(network, poolAddress, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_25191329_0x90a746e28f4db27b2595b8ac55ef999914ed09453d5924b1424b2c050fd053c3_99_1779941075",
      "type": "trade",
      "attributes": {
        "block_number": 25191329,
        "tx_hash": "0x90a746e28f4db27b2595b8ac55ef999914ed09453d5924b1424b2c050fd053c3",
        "tx_from_address": "0x0b0d1579b739b1996d28c53c4ff11e2c541a1188",
        "from_token_amount": "0.106968578509495",
        "to_token_amount": "211.331589",
        "price_from_in_currency_token": "1.0",
        "price_to_in_currency_token": "0.000506164643987487",
        "price_from_in_usd": "1976.18881048696",
        "price_to_in_usd": "1.00027690571219",
        "block_timestamp": "2026-05-28T04:04:11Z",
        "kind": "buy",
        "volume_in_usd": "211.39010792416",
        "from_token_address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
        "to_token_address": "0xdac17f958d2ee523a2206206994597c13d831ec7"
      }
    },
    {
      "id": "eth_25191103_0x8c7d19881344e94e69f69f44a3910a32183652b84156537ec23313bfa01ff054_804_1779938350",
      "type": "trade",
      "attributes": {
        "block_number": 25191103,
        "tx_hash": "0x8c7d19881344e94e69f69f44a3910a32183652b84156537ec23313bfa01ff054",
        "tx_from_address": "0x39b9a705f5aa2fdf315bf5cc8ecd71dc821f45b1",
        "from_token_amount": "192.459164",
        "to_token_amount": "0.096413761161719",
        "price_from_in_currency_token": "0.000500956977874636",
        "price_to_in_currency_token": "1.0",
        "price_from_in_usd": "0.992388076121959",
        "price_to_in_usd": "1980.98463531194",
        "block_timestamp": "2026-05-28T03:18:47Z",
        "kind": "sell",
        "volume_in_usd": "190.994179494001",
        "from_token_address": "0xdac17f958d2ee523a2206206994597c13d831ec7",
        "to_token_address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2"
      }
    }
  ]
}
```


# Latest-Pools-List

To query all the latest pools across all networks on GeckoTerminal

```java
CompletableFuture<ApiResponse<Pool>> latestPoolsListAsync(
    final String include,
    final Integer page,
    final Boolean includeGtCommunityData)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex`, `network` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `includeGtCommunityData` | `Boolean` | Query, Optional | Include GeckoTerminal community data (sentiment votes, suspicious reports).<br>Default: `false` |

## Response Type

**200**: Latest pools across all networks

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Pool`](../../doc/models/pool.md).

## Example Usage

```java
api.latestPoolsListAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "solana_6EiJDBoHqRA3m6FqYBphpGomspmFxtj4mawUKYMZtcVG",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "0.00000148440590295321912651916468624641639408545041453058498522449228",
        "base_token_price_native_currency": null,
        "quote_token_price_usd": "83.768359508641337467584153811084885016464255852",
        "quote_token_price_native_currency": null,
        "base_token_price_quote_token": null,
        "quote_token_price_base_token": null,
        "address": "6EiJDBoHqRA3m6FqYBphpGomspmFxtj4mawUKYMZtcVG",
        "name": "MadDonkey / SOL",
        "pool_created_at": "2026-05-27T14:58:17Z",
        "fdv_usd": "3847.309588",
        "market_cap_usd": null,
        "price_change_percentage": {
          "m5": "-18.046",
          "m15": "-18.046",
          "m30": "-18.046",
          "h1": "-18.046",
          "h6": "-18.046",
          "h24": "-18.046"
        },
        "transactions": {
          "m5": {
            "buys": 1,
            "sells": 1,
            "buyers": 1,
            "sellers": 1
          },
          "m15": {
            "buys": 1,
            "sells": 1,
            "buyers": 1,
            "sellers": 1
          },
          "m30": {
            "buys": 1,
            "sells": 1,
            "buyers": 1,
            "sellers": 1
          },
          "h1": {
            "buys": 1,
            "sells": 1,
            "buyers": 1,
            "sellers": 1
          },
          "h6": {
            "buys": 1,
            "sells": 1,
            "buyers": 1,
            "sellers": 1
          },
          "h24": {
            "buys": 1,
            "sells": 1,
            "buyers": 1,
            "sellers": 1
          }
        },
        "volume_usd": {
          "m5": "6.7101798706",
          "m15": "6.7101798706",
          "m30": "6.7101798706",
          "h1": "6.7101798706",
          "h6": "6.7101798706",
          "h24": "6.7101798706"
        },
        "reserve_in_usd": null,
        "sentiment_vote_positive_percentage": 0,
        "sentiment_vote_negative_percentage": 0,
        "community_sus_report": 0
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "solana_2R33cGC6WaP1j2wcvmkAvGjTeEy1N1hvwZtBykmypump",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "solana_So11111111111111111111111111111111111111112",
            "type": "token"
          }
        },
        "network": {
          "data": {
            "id": "solana",
            "type": "network"
          }
        },
        "dex": {
          "data": {
            "id": "pump-fun",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "solana_2R33cGC6WaP1j2wcvmkAvGjTeEy1N1hvwZtBykmypump",
      "type": "token",
      "attributes": {
        "address": "2R33cGC6WaP1j2wcvmkAvGjTeEy1N1hvwZtBykmypump",
        "name": "Donkey",
        "symbol": "MadDonkey",
        "decimals": 6,
        "image_url": null,
        "coingecko_coin_id": null
      }
    },
    {
      "id": "solana_So11111111111111111111111111111111111111112",
      "type": "token",
      "attributes": {
        "address": "So11111111111111111111111111111111111111112",
        "name": "Wrapped SOL",
        "symbol": "SOL",
        "decimals": 9,
        "image_url": "https://coin-images.coingecko.com/coins/images/21629/large/solana.jpg?1696520989",
        "coingecko_coin_id": "wrapped-solana"
      }
    },
    {
      "id": "pump-fun",
      "type": "dex",
      "attributes": {
        "name": "Pump.fun"
      }
    }
  ]
}
```


# Latest-Pools-Network

To query all the latest pools based on the provided network

```java
CompletableFuture<ApiResponse<Pool>> latestPoolsNetworkAsync(
    final String network,
    final String include,
    final Integer page,
    final Boolean includeGtCommunityData)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |
| `includeGtCommunityData` | `Boolean` | Query, Optional | Include GeckoTerminal community data (sentiment votes, suspicious reports).<br>Default: `false` |

## Response Type

**200**: Latest pools on a network

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`Pool`](../../doc/models/pool.md).

## Example Usage

```java
String network = "eth";

api.latestPoolsNetworkAsync(network, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_0x4b025567ef3e47e7c6f091ba2e224d250eaeedadfddcee292c5281f632fbea07",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "0.0000462785114387554",
        "base_token_price_native_currency": "0.0000000194777059991249",
        "quote_token_price_usd": "2064.36505232757",
        "quote_token_price_native_currency": "1.0",
        "base_token_price_quote_token": "0.000000019477706",
        "quote_token_price_base_token": "51340748.2403178",
        "address": "0x4b025567ef3e47e7c6f091ba2e224d250eaeedadfddcee292c5281f632fbea07",
        "name": "GOSLINGS / ETH 1%",
        "pool_created_at": "2026-05-27T15:05:59Z",
        "fdv_usd": "46060.39188",
        "market_cap_usd": null,
        "price_change_percentage": {
          "m5": "46.095",
          "m15": "46.095",
          "m30": "46.095",
          "h1": "46.095",
          "h6": "46.095",
          "h24": "46.095"
        },
        "transactions": {
          "m5": {
            "buys": 5,
            "sells": 1,
            "buyers": 5,
            "sellers": 1
          },
          "m15": {
            "buys": 5,
            "sells": 1,
            "buyers": 5,
            "sellers": 1
          },
          "m30": {
            "buys": 5,
            "sells": 1,
            "buyers": 5,
            "sellers": 1
          },
          "h1": {
            "buys": 5,
            "sells": 1,
            "buyers": 5,
            "sellers": 1
          },
          "h6": {
            "buys": 5,
            "sells": 1,
            "buyers": 5,
            "sellers": 1
          },
          "h24": {
            "buys": 5,
            "sells": 1,
            "buyers": 5,
            "sellers": 1
          }
        },
        "volume_usd": {
          "m5": "1522.0126601069",
          "m15": "1522.0126601069",
          "m30": "1522.0126601069",
          "h1": "1522.0126601069",
          "h6": "1522.0126601069",
          "h24": "1522.0126601069"
        },
        "reserve_in_usd": "-97.3671492356286",
        "sentiment_vote_positive_percentage": 0,
        "sentiment_vote_negative_percentage": 0,
        "community_sus_report": 0
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0xd4c24d1172813702439ab03b914a7c6e1c65b110",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0x0000000000000000000000000000000000000000",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap-v4-ethereum",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "eth_0xd4c24d1172813702439ab03b914a7c6e1c65b110",
      "type": "token",
      "attributes": {
        "address": "0xd4c24d1172813702439ab03b914a7c6e1c65b110",
        "name": "Justice for Goslings",
        "symbol": "GOSLINGS",
        "decimals": 18,
        "image_url": null,
        "coingecko_coin_id": null
      }
    },
    {
      "id": "eth_0x0000000000000000000000000000000000000000",
      "type": "token",
      "attributes": {
        "address": "0x0000000000000000000000000000000000000000",
        "name": "Ether",
        "symbol": "ETH",
        "decimals": 18,
        "image_url": null,
        "coingecko_coin_id": null
      }
    },
    {
      "id": "uniswap-v4-ethereum",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V4 (Ethereum)"
      }
    }
  ]
}
```


# Pools-Addresses

To query multiple pools based on the provided network and pool addresses

```java
CompletableFuture<ApiResponse<MultiPoolAddressData>> poolsAddressesAsync(
    final String network,
    final String addresses,
    final String include,
    final Boolean includeVolumeBreakdown,
    final Boolean includeComposition)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `addresses` | `String` | Template, Required | Pool contract address, comma-separated if more than one pool contract address. |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `includeVolumeBreakdown` | `Boolean` | Query, Optional | Include volume breakdown.<br>Default: `false` |
| `includeComposition` | `Boolean` | Query, Optional | Include pool composition.<br>Default: `false` |

## Response Type

**200**: Multiple pools data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`MultiPoolAddressData`](../../doc/models/multi-pool-address-data.md).

## Example Usage

```java
String network = "eth";
String addresses = "0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640";

api.poolsAddressesAsync(network, addresses, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "2087.84394126108",
        "base_token_price_native_currency": "1.0",
        "base_token_balance": "21341.2567581564",
        "base_token_liquidity_usd": "44581759.9202084558888866184853251251371757144338",
        "quote_token_price_usd": "1.00206113475649",
        "quote_token_price_native_currency": "0.000479959386437488",
        "quote_token_balance": "54447706.143913",
        "quote_token_liquidity_usd": "54591030.8544913961746207304067005997478464613757298294624",
        "base_token_price_quote_token": "2083.509622392",
        "quote_token_price_base_token": "0.0004799593864",
        "address": "0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640",
        "name": "WETH / USDC 0.05%",
        "pool_name": "WETH / USDC",
        "pool_fee_percentage": "0.05",
        "pool_created_at": "2021-12-29T12:35:14Z",
        "fdv_usd": "4706853532.94868",
        "market_cap_usd": "4714036496.09939",
        "price_change_percentage": {
          "m5": "0",
          "m15": "0.001",
          "m30": "0.339",
          "h1": "0.157",
          "h6": "0.64",
          "h24": "-1.403"
        },
        "transactions": {
          "m5": {
            "buys": 6,
            "sells": 5,
            "buyers": 6,
            "sellers": 4
          },
          "m15": {
            "buys": 39,
            "sells": 16,
            "buyers": 29,
            "sellers": 12
          },
          "m30": {
            "buys": 75,
            "sells": 52,
            "buyers": 44,
            "sellers": 34
          },
          "h1": {
            "buys": 101,
            "sells": 108,
            "buyers": 63,
            "sellers": 64
          },
          "h6": {
            "buys": 486,
            "sells": 514,
            "buyers": 221,
            "sellers": 288
          },
          "h24": {
            "buys": 2447,
            "sells": 2405,
            "buyers": 878,
            "sellers": 1000
          }
        },
        "volume_usd": {
          "m5": "169302.729000635",
          "m15": "1135682.71288074",
          "m30": "5933192.37924989",
          "h1": "7342742.90980712",
          "h6": "23039712.0227694",
          "h24": "126282664.514509"
        },
        "net_buy_volume_usd": {
          "m5": "-150936.4938119748",
          "m15": "124495.452251326",
          "m30": "1272049.71489431",
          "h1": "310733.1474086",
          "h6": "704731.2010502",
          "h24": "-4997173.0542116"
        },
        "buy_volume_usd": {
          "m5": "9183.1175943302",
          "m15": "630089.082566032",
          "m30": "3602621.04707209",
          "h1": "3826738.02860785",
          "h6": "11872221.6119098",
          "h24": "60642745.7301488"
        },
        "sell_volume_usd": {
          "m5": "160119.611406305",
          "m15": "505593.630314706",
          "m30": "2330571.33217778",
          "h1": "3516004.88119925",
          "h6": "11167490.4108596",
          "h24": "65639918.7843604"
        },
        "reserve_in_usd": "99172790.7747",
        "locked_liquidity_percentage": "0.0"
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap_v3",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "type": "token",
      "attributes": {
        "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/2518/large/weth.png?1696503332",
        "coingecko_coin_id": "weth"
      }
    },
    {
      "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
      "type": "token",
      "attributes": {
        "address": "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
        "name": "USD Coin",
        "symbol": "USDC",
        "decimals": 6,
        "image_url": "https://coin-images.coingecko.com/coins/images/6319/large/USDC.png?1769615602",
        "coingecko_coin_id": "usd-coin"
      }
    },
    {
      "id": "uniswap_v3",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V3"
      }
    }
  ]
}
```


# Search-Pools

To search for pools across all networks by pool address, token name, token symbol, or token contract address

```java
CompletableFuture<ApiResponse<PoolSearch>> searchPoolsAsync(
    final String query,
    final String network,
    final String include,
    final Integer page)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query` | `String` | Query, Optional | Search query: pool contract address, token name, token symbol, or token contract address.<br><br>**Default**: `"weth"` |
| `network` | `String` | Query, Optional | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `include` | `String` | Query, Optional | Attributes to include, comma-separated if more than one.<br>Available values: `base_token`, `quote_token`, `dex` |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |

## Response Type

**200**: Pool search results

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PoolSearch`](../../doc/models/pool-search.md).

## Example Usage

```java
String query = "weth";

api.searchPoolsAsync(query, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth_0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640",
      "type": "pool",
      "attributes": {
        "base_token_price_usd": "2084.57214039429",
        "base_token_price_native_currency": "1.0",
        "quote_token_price_usd": "1.00359565004917",
        "quote_token_price_native_currency": "0.00048094599624371",
        "base_token_price_quote_token": "2079.235522928",
        "quote_token_price_base_token": "0.0004809459962",
        "address": "0x88e6a0c2ddd26feeb64f039a2c41296fcb3f5640",
        "name": "WETH / USDC 0.05%",
        "pool_created_at": "2021-12-29T12:35:14Z",
        "fdv_usd": "4700091001.66103",
        "market_cap_usd": "4706648770.97887",
        "price_change_percentage": {
          "m5": "0",
          "m15": "0",
          "m30": "0",
          "h1": "0",
          "h6": "0.599",
          "h24": "-1.887"
        },
        "transactions": {
          "m5": {
            "buys": 1,
            "sells": 1,
            "buyers": 1,
            "sellers": 1
          },
          "m15": {
            "buys": 7,
            "sells": 24,
            "buyers": 7,
            "sellers": 18
          },
          "m30": {
            "buys": 21,
            "sells": 53,
            "buyers": 15,
            "sellers": 41
          },
          "h1": {
            "buys": 57,
            "sells": 123,
            "buyers": 39,
            "sellers": 88
          },
          "h6": {
            "buys": 431,
            "sells": 477,
            "buyers": 194,
            "sellers": 279
          },
          "h24": {
            "buys": 2436,
            "sells": 2385,
            "buyers": 863,
            "sellers": 989
          }
        },
        "volume_usd": {
          "m5": "2407.6289853096",
          "m15": "210244.509017768",
          "m30": "1067809.71712486",
          "h1": "2766027.68033409",
          "h6": "17336676.2757229",
          "h24": "122795216.58555"
        },
        "reserve_in_usd": "101050763.5099"
      },
      "relationships": {
        "base_token": {
          "data": {
            "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
            "type": "token"
          }
        },
        "quote_token": {
          "data": {
            "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
            "type": "token"
          }
        },
        "dex": {
          "data": {
            "id": "uniswap_v3",
            "type": "dex"
          }
        }
      }
    }
  ],
  "included": [
    {
      "id": "eth_0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "type": "token",
      "attributes": {
        "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "decimals": 18,
        "image_url": "https://coin-images.coingecko.com/coins/images/2518/large/weth.png?1696503332",
        "coingecko_coin_id": "weth"
      }
    },
    {
      "id": "eth_0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
      "type": "token",
      "attributes": {
        "address": "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
        "name": "USD Coin",
        "symbol": "USDC",
        "decimals": 6,
        "image_url": "https://coin-images.coingecko.com/coins/images/6319/large/USDC.png?1769615602",
        "coingecko_coin_id": "usd-coin"
      }
    },
    {
      "id": "uniswap_v3",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V3"
      }
    }
  ]
}
```


# Onchain-Simple-Price

To get token price based on the provided token contract address on a network

```java
CompletableFuture<ApiResponse<OnchainSimplePrice>> onchainSimplePriceAsync(
    final String network,
    final String addresses,
    final Boolean includeMarketCap,
    final Boolean mcapFdvFallback,
    final Boolean include24HrVol,
    final Boolean include24HrPriceChange,
    final Boolean includeTotalReserveInUsd,
    final Boolean includeInactiveSource)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `addresses` | `String` | Template, Required | Token contract address, comma-separated if more than one token contract address. |
| `includeMarketCap` | `Boolean` | Query, Optional | Include market capitalization.<br>Default: `false` |
| `mcapFdvFallback` | `Boolean` | Query, Optional | Return FDV if market cap is not available.<br>Default: `false` |
| `include24HrVol` | `Boolean` | Query, Optional | Include 24hr volume.<br>Default: `false` |
| `include24HrPriceChange` | `Boolean` | Query, Optional | Include 24hr price change.<br>Default: `false` |
| `includeTotalReserveInUsd` | `Boolean` | Query, Optional | Include total reserve in USD.<br>Default: `false` |
| `includeInactiveSource` | `Boolean` | Query, Optional | Include token price data from inactive pools using the most recent swap.<br>Default: `false` |

## Response Type

**200**: Token price data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`OnchainSimplePrice`](../../doc/models/onchain-simple-price.md).

## Example Usage

```java
String network = "eth";
String addresses = "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2";

api.onchainSimplePriceAsync(network, addresses, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "49dd0b90-d99d-48b6-8fe2-03e826fbcef2",
    "type": "simple_token_price",
    "attributes": {
      "token_prices": {
        "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2": "2084.57379936447"
      },
      "market_cap_usd": {
        "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2": "4706652516.682727"
      },
      "h24_volume_usd": {
        "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2": "313441016.145429"
      },
      "h24_price_change_percentage": {
        "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2": "-1.8867250098940773"
      },
      "total_reserve_in_usd": {
        "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2": "1015673598.896450024556193850116628967"
      },
      "last_trade_timestamp": {
        "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2": "1779882383"
      }
    }
  }
}
```


# Networks-List

To retrieve a list of all supported networks on GeckoTerminal

```java
CompletableFuture<ApiResponse<NetworksList>> networksListAsync(
    final Integer page)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |

## Response Type

**200**: List of supported networks

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`NetworksList`](../../doc/models/networks-list.md).

## Example Usage

```java
api.networksListAsync(null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "eth",
      "type": "network",
      "attributes": {
        "name": "Ethereum",
        "coingecko_asset_platform_id": "ethereum"
      }
    },
    {
      "id": "bsc",
      "type": "network",
      "attributes": {
        "name": "BNB Chain",
        "coingecko_asset_platform_id": "binance-smart-chain"
      }
    }
  ]
}
```


# Dexes-List

To query all the supported decentralized exchanges (DEXs) based on the provided network on GeckoTerminal

```java
CompletableFuture<ApiResponse<DexesList>> dexesListAsync(
    final String network,
    final Integer page)
```

## Authentication

This endpoint requires [headerAuth](../../doc/auth/custom-header-signature.md) **OR** [queryAuth](../../doc/auth/custom-query-parameter.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `String` | Template, Required | Network ID.<br>*refers to [`/onchain/networks`](/reference/networks-list). |
| `page` | `Integer` | Query, Optional | Page through results.<br>Default value: 1 |

## Response Type

**200**: List of supported DEXs on a network

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`DexesList`](../../doc/models/dexes-list.md).

## Example Usage

```java
String network = "eth";

api.dexesListAsync(network, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "uniswap_v2",
      "type": "dex",
      "attributes": {
        "name": "Uniswap V2"
      }
    },
    {
      "id": "sushiswap",
      "type": "dex",
      "attributes": {
        "name": "SushiSwap"
      }
    }
  ]
}
```

