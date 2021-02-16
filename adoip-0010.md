# ADOIP-0010 : Registered IDs for EIP-2362

```
Number:  ADOIP-0010
Title:   Registered IDs for EIP-2362
Type:    Informational
Status:  Draft
Authors: Adán SDPC <@aesedepece>
Created: 2021-02-16
```

## Abstract

[EIP-2362] defines a standard interface for numeric pull oracles.
This document lists IDs to be used when querying [EIP-2362] compliant oracles.

## Motivation

As stated in the [EIP-2362] specification:

> Registration of IDs is done with informative purposes only.
>
> Registration of an ID is not compulsory, and unregistered IDs can be used without any restrictions.
>
> However, it is recommended that commonly used value pairs are registered and have an ID publicly assigned to them, so that it becomes much easier to find multiple oracles that provide uniform data points that can be aggregated together without formatting risks (e.g. different oracles using a different number of decimal places when encoding floating point numbers).

Due to the informational nature of this document, new IDs can be added liberally.
Special attention should be given however to giving special visibility to those that have been proven specially useful to the ecosystem.

## Registered IDs

These are the registered IDs for usage in [EIP-2362].

### Price

Price data points represent the value of an asset in reference to a second asset.

| Type  | Caption | DecimalPlaces | String            | ID                                                                 |
|-------|---------|---------------|-------------------|--------------------------------------------------------------------|
| Price | ETH/USD | 3             | `Price-ETH/USD-3` | `dfaa6f747f0f012e8f2069d6ecacff25f5cdf0258702051747439949737fc0b5` |
| Price | BTC/USD | 3             | `Price-BTC/USD-3` | `637b7efb6b620736c247aaa282f3898914c0bef6c12faff0d3fe9d4bea783020` |
| Price | XAU/USD | 3             | `Price-XAU/USD-3` | `2dfb033e1ae0529b328985942d27f2d5a62213f3a2d97ca8e27ad2864c5af942` |
| Price | DAI/USD | 6             | `Price-DAI/USD-6` | `9899e35601719f1348e09967349f72c7d04800f17c14992d6dcf2f17fac713ea` |

### Environment

Environment data points provide information about changeable, real time data that comes from the real world, e.g. timestamps, temperatures, etc.

| Type        | Caption | DecimalPlaces | String                  | ID                                                                 |
|-------------|---------|---------------|-------------------------|--------------------------------------------------------------------|
| Environment | UTCTIME | 0             | `Environment-UTCTIME-0` | `0dcebd6dce29e76a6fe1e9a230e4dbbdfd7e3addc3a7462a117e3ea49f7bf9ef` |

### Constants

Constants are expected never to change, i.e. queries for these IDs should always return the same value.

| Type     | Caption | DecimalPlaces | String           | ID                                                                 |
|----------|---------|---------------|------------------|--------------------------------------------------------------------|
| Constant | PI      | 18            | `Constant-PI-18` | `7f9b64e3f037f57a314e11c8a78fb02cda69a8e3a5b4ba868cc2bf6494ba51be` |


[EIP-2362]: https://github.com/adoracles/EIPs/blob/eip-2362/EIPS/eip-2362.md
