# Dataframe: `hw2:fed_funds_futures` - 30-Day Fed Funds Futures (ZQ)

Daily ohlcv-1d bars from the CME Globex dataset (GLBX.MDP3), requested with the parent symbol ZQ.FUT so that one query returns every listed ZQ contract. Columns: date (trading date, tz-naive), symbol, open, high, low, close, volume. Outright contracts look like ZQU6 (month code plus one year digit); calendar spreads look like ZQU6-ZQZ6 and should be dropped with fedwatch.filter_outright_contracts. A contract settles at 100 minus the calendar-day average EFFR over its month, so 100 - close is the implied average rate in percent. Thin, far-dated contracts may be missing on some days.


## DataFrame Glimpse

```
Rows: 11751
Columns: 7
$ date   <datetime[ns]> 2026-10-25 00:00:00
$ symbol          <str> 'ZQF7'
$ open            <f64> 95.895
$ high            <f64> 95.895
$ low             <f64> 95.89
$ close           <f64> 95.895
$ volume          <u64> 396


```

## Dataframe Manifest

| Dataframe Name                 | 30-Day Fed Funds Futures (ZQ)                                                          |
|--------------------------------|--------------------------------------------------------------------------------------|
| Dataframe ID                   | [fed_funds_futures](../dataframes/hw2/fed_funds_futures.md)                                       |
| Sources                        | CME Group                                          |
| Providers                      | Databento                                        |
| Provider Links                 | https://databento.com/datasets/GLBX.MDP3                                   |
| Tags                           | Monetary Policy, Futures, Fed Funds                                             |
| Access Types                   |                                       |
| How is data pulled?            | Databento API via Python                                                   |
| Data available up to (min)     | 2026-10-25 00:00:00                                                             |
| Data available up to (max)     | 2026-10-25 00:00:00                                                             |
| Dataframe Path                 | /Users/franklinliu/Projects/hw2-frank22lin/_data/fed_funds_futures.parquet                                             |


**Linked Charts:**


- [hw2:fedwatch_latest_forecast](../../charts/hw2.fedwatch_latest_forecast.md)



## Pipeline Manifest

| Pipeline Name                   | HW 2: The Yield Curve and the Policy Path                       |
|---------------------------------|--------------------------------------------------------|
| Pipeline ID                     | [hw2](../../../index.md)              |
| Maintainer                      | Jeremiah Bejarano               |
| Contributors                    | Jeremiah Bejarano |
| Repository                     | https://github.com/hw-finm-32800/hw2                  |
| Pipeline Web Page               | <a href="file:///Users/franklinliu/Projects/hw2-frank22lin/docs/index.html">Pipeline Web Page      |
| Date of Last Code Update        | 2026-10-26 16:07:40           |
| OS Compatibility                | Windows, Linux, macOS |
| Linked Dataframes               |  [hw2:crsp_treasury_consolidated](../../dataframes/hw2/crsp_treasury_consolidated.md)<br>  [hw2:fed_yield_curve](../../dataframes/hw2/fed_yield_curve.md)<br>  [hw2:fed_funds_futures](../../dataframes/hw2/fed_funds_futures.md)<br>  |


**Build Commands:**
```
doit

```

