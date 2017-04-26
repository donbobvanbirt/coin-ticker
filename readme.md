# coin-ticker-jlp

This is my first Javascript library so a sort of learning exercise for now

## Below is original readme from coin-ticker unmodified

Easily get the latest exchange data of Bitcoin, Etherium, Litecoin, and other assets from a variety of exchanges including Bitfinex, Bitstamp, Kraken, Poloniex and others.


[![CircleCI](https://circleci.com/gh/donbobvanbirt/coin-ticker.svg?style=svg)](https://circleci.com/gh/donbobvanbirt/coin-ticker)

## Install

```bash
$ npm install --save coin-ticker
```

## Usage
**Require:**
```js
TODO: will change
const coinTicker = require('coin-ticker');

```

**Syntax:**
```js
TODO: will change
coinTicker(exchange, currency-pair)
```

**Parameters:**

**exchange:**
A string declaring one of the available exchanges:

    * 'bitfinex'
    * 'bitstamp'
    * 'poloniex'
    * 'btce'
    * 'kraken'
    * 'okcoin'
    * 'exmo'

**currency-pair:**
An optional string declaring the currencies or assets to retrieve. Default is 'btcusd'.

Available asset pairs by exchange:

**Bitfinex:**

    * 'btcusd'
    * 'ltcusd'
    * 'ltcbtc'
    * 'ethusd'
    * 'ethbtc'
    * 'etcbtc'
    * 'etcusd'
    * 'rrtusd'
    * 'rrtbtc'
    * 'zecusd'
    * 'zecbtc'

**Bitstamp:**

    * 'btcusd'
    * 'btceur'
    * 'eurusd'
    * 'xrpusd'
    * 'xrpeur'

**Poloniex:**

    * 'btcusd'
    * 'ethbtc'
    * 'xrpbtc'
    * 'dashbtc'
    * 'ethusd'
    * 'xmrbtc'
    * 'etcbtc'
    * 'fctbtc'
    * 'zecbtc'
    * 'ltcbtc'
    * 'dashusd'
    * 'gntbtc'
    * 'xrpusd'
    * 'dcrbtc'
    * 'repbtc'
    * 'maidbtc'
    * 'lskbtc'
    * 'xmrusd'
    * 'dogebtc'
    * 'ampbtc'
    * 'xembtc'
    * 'sjcxbtc'
    * 'etcusd'
    * 'steembtc'
    * 'etceth'
    * 'navbtc'
    * 'sysbtc'
    * 'gnteth'
    * 'zecusd'
    * 'ltcusd'

**BTC-e:**

    * 'btcusd'
    * 'btcrur'
    * 'btceur'
    * 'ltcbtc'
    * 'ltcusd'
    * 'ltcrur'
    * 'ltceur'
    * 'nmcbtc'
    * 'nmcusd'
    * 'nvcbtc'
    * 'nvcusd'
    * 'usdrur'
    * 'eurusd'
    * 'eurrur'
    * 'ppcbtc'
    * 'ppcusd'
    * 'dshbtc'
    * 'dshusd'
    * 'ethbtc'
    * 'ethusd'
    * 'etheur'
    * 'ethltc'
    * 'ethrur'

**Kraken:**

    * 'etcbtc'
    * 'etceur'
    * 'etcusd'
    * 'ethbtc'
    * 'ethcad'
    * 'etheur'
    * 'ethgbp'
    * 'ethjpy'
    * 'ethusd'
    * 'ltcbtc'
    * 'ltceur'
    * 'ltcusd'
    * 'btccad'
    * 'btceur'
    * 'btcgbp'
    * 'btcjpy'
    * 'btcusd'

**Okcoin:**

    * 'btcusd'
    * 'ltcusd'


**Exmo:**

    * 'btcusd'
    * 'btceur'
    * 'btcrub'
    * 'btcuah'
    * 'dashbtc'
    * 'dashusd'
    * 'ethbtc'
    * 'ethusd'
    * 'ethrub'
    * 'dogebtc'
    * 'ltcbtc'
    * 'ltcrub'


**Response Data:**

  An object containing the following values:

```js
{
  last: // the last traded price
  ask:  // current ask
  bid: // current bid
  low: // 24 hour low
  high: // 24 hour high
  vol: // 24 hour volume
  timestamp: // precise time
  exchange: // the current exchange, i.e. 'bitfinex'
  pair: // the asset pair, i.e. 'btcusd'
}
```

**Examples:**

Get the current ticker data of ETH/USD from BTC-e:
```js
coinTicker('btce', 'ethusd');
```

Get the current ticker data of BTC/USD from Bitfinex:
```js
coinTicker('bitfinex'); // when no asset pair is specified, coinTicker will default to 'btcusd'
```

Example response data:
```js
{
  last: '1034.8',
  ask: '1034.8',
  bid: '1034.7',
  low: '1001.6',
  high: '1040.0',
  vol: '15112.8733725',
  timestamp: '1486238356.227418953',
  exchange: 'bitfinex',
  pair: 'btcusd'
}
```
