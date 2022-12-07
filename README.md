# Parex PublicAPI

### 1.  RestAPI commands :

##### Summary Endpoint

```
"https://publicapi.parex.exchange/v1/tickers"
```
- Overview of market data for all tickers and all markets.

```
  {
    "trading_pairs": "XRP_BTC",
    "last_price": 0.0000203,
    "lowest_ask": 0.0000213,
    "highest_bid": 0.0000202,
    "base_volume": 350700,
    "quote_volume": 7.139649999999999,
    "price_change_percent_24h": -0.49019607843137253,
    "highest_price_24h": 0.0000204,
    "lowest_price_24h": 0.0000203
  },"
```



##### Endpoint A1

```
"https://publicapi.parex.exchange/v1/assets"
```
- In depth details on crypto currencies available on the exchange.
```
{  
   "BTC":{  
      "name":"bitcoin",
      "unified_cryptoasset_id" :"1",
      "can_withdraw":"true",
      "can_deposit":"true",
      "min_withdraw":"0.01",
      "max_withdraw ":"100" 
      "name":"bitcoin",
      "maker_fee":"0.01",
      "taker_fee":"0.01",
   },
   "ETH":{  
      "name":"ethereum",
      "unified_cryptoasset_id":"1027",
      "can_withdraw":"false",
      "can_deposit":"false",
      "min_withdraw":"10.00",
      "max_withdraw ":"0.00" 
      "maker_fee":"0.01",
      "taker_fee":"0.01",
   }
}
```


##### Endpoint A2

```
"https://publicapi.parex.exchange/v1/ticker?market_pair=PRX_USDT"
```
- 24-hour rolling window price change statistics for all markets.
- /market_pair={market_pair}
```
{  
   "BTC_USDT":{  
      "base_id":"1",
      "quote_id":"825",
      "last_price":"10000",
      "quote_volume":"20000",
      "base_volume":"2",   
      "isFrozen":"0"
   },
   "LTC_BTC":{  
      "base_id":"2",
      "quote_id":"1",
      "last_price":"0.00699900",
      "base_volume":"20028,526",
      "quote_volume":"279594",
      "isFrozen":"0"
   },
"BNB_BTC":{  
      "base_id":"1839",
      "quote_id":"1",
      "last_price":"0.00699900",
      "base_volume":"53819",
      "quote_volume":"99.3459",      
      "isFrozen":"0"
   }
}
```

##### Endpoint A3

```
"https://publicapi.parex.exchange/v1/orderbook?market_pair=PRX_USDT&depth=10"
```
- Market depth of a trading pair. One array containing a list of ask prices and another array containing bid prices. Query for level 2 order book with full depth available as minimum requirement.
- /market_pair={market_pair}
- /depth={depth}

```
{  
   "timestamp":"‭1585177482652‬",
   "bids":[  
      [  
         "12462000",
         "0.04548320"
      ],
      [  
         "12457000",
         "3.00000000"
      ]
   ],
   "asks":[  
      [  
         "12506000",
         "2.73042000"
      ],
      [  
         "12508000",
         "0.33660000"
      ]
   ]
}
```


##### Endpoint A4

```
"https://publicapi.parex.exchange/v1/trades?market_pair=PRX_USDT&depth=10"
```
- Recently completed trades for a given market. 24 hour historical full trades available as minimum requirement.
- /market_pair={market_pair}
- /depth={depth}

```
[   
   {         
      "trade_id":3523643,
      "price":"0.01",
      "base_volume":"569000",
      "quote_volume":"0.01000000",
      "timestamp":"‭1585177482652‬",
      "type":"sell"
   }
]
```





