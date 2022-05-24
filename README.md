# Options Analysis

`analysis.jl` is a [Pluto Notebook](https://github.com/fonsp/Pluto.jl) that
graphs options properties in a 3D format. (For example, time until expiration
and delta versus volatility). You can load this notebook in a Pluto notebook to
interactively understand options greeks. Examples are displayed on [my
blog](http://addcnin.blue/2022/05/23/options_analysis/).

Included is SPY options chain data as of 5/20, retrieved from TD Ameritrade. If
you would like to use your own data, use the following commands.

```sh
$ export API_KEY=YOUR_API_KEY
$ export SYMBOL=SPY
$ export DATE="2022-05-22"
$ curl -X GET --header "Authorization: " "https://api.tdameritrade.com/v1/marketdata/chains?apikey=$API_KEY&symbol=$SYMBOL&contractType=ALL&strikeCount=16&includeQuotes=TRUE&strategy=ANALYTICAL&interval=1&range=ALL&fromDate=$DATE"
```
