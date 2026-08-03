
# Public Treasury

## Class Name

`PublicTreasury`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`CompanyTreasury`](../../../doc/models/company-treasury.md) | PublicTreasury.fromCompanyTreasury(CompanyTreasury companyTreasury) |
| [`GovernmentTreasury`](../../../doc/models/government-treasury.md) | PublicTreasury.fromGovernmentTreasury(GovernmentTreasury governmentTreasury) |

## CompanyTreasury

### Initialization Code

#### Example

```java
PublicTreasury.fromCompanyTreasury(
        new CompanyTreasury.Builder(
            108.16D,
            48.48D,
            226.16D,
            Arrays.asList(
                new Company.Builder(
                    "name2",
                    "symbol4",
                    "country6",
                    92.32D,
                    132.18D,
                    9.16D,
                    23.92D
                )
                .build()
            )
        )
        .build()
    )
```

## GovernmentTreasury

### Initialization Code

#### Example

```java
PublicTreasury.fromGovernmentTreasury(
        new GovernmentTreasury.Builder(
            165.3D,
            8.66D,
            169.02D,
            Arrays.asList(
                new Government.Builder(
                    "name4",
                    "symbol4",
                    "country8",
                    170.96D,
                    124.9D,
                    254.12D,
                    16.64D
                )
                .build()
            )
        )
        .build()
    )
```

