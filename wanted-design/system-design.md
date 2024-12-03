## Overal concept

Dashboard to facilitate trading multiple stocks by setting up rules ahead when entering the trade.
The system will use a live algo-trading framework to keep track of positions (handle risk management to protect open positions and taking profit rules).
Dashboard will show at a glance on main page most important information about the trading day, stocks portfolio, potential entries for the day.

## Requirements

### Server-side

24/7 running server

- to host the broker gateway, always connected
- to run always-on live algo-trading framework ([nautilustrader](https://github.com/nautechsystems/nautilus_trader) / [quantconnect lean](https://github.com/QuantConnect/Lean))
- for alerts and auto order execution
- for scheduled tasks like pulling account statements, trades history

### Client-side

- webpage accessible on desktop and more importantly **_mobile_**
- Charts like TradingView [lightweight charts](https://github.com/tradingview/lightweight-charts) / advanced charts

## Functionality

### Server

- always on algo-trading for following open positions
- storing data

  - historical trades
  - everyday account snapshot

- python backtesting

  #### Alerts system (Telegram)

  - if system is down
  - positions tracking: negative P/L, take profit attained
  - new posts on tradingedge about positions / watchlist

### Client webapp

#### Main page

- Most imporant info at a glance:
  - Calender week and month view: day of week, hour of trading day, upcoming bank holidays, upcoming earnings of positions/watchlist
  - tradingedge posts about positions/watchlist; potential new stocks

#### Portfolio page

- current portfolio state, vs target portfolio

#### Positions page

- selecting one ticker at a time
- showing charts:
  - all time period with 1D bar (showing as well Earnings dates (previous and upcoming))
  - few days period with 1 minute bar
  - (all charts show horizontal line of current poosition AvgCost)
- history of buy&sell trades up to current quantity
- P&L chart of current position

#### Orders page

- adding new orders with
  - ticker + strategy pair
  - order expiration: max loss %, max time in days
  - take profit target: %
  - calcualting R ratio from data above
  - visual display of the two possible scenarios
  - visual display of new portfolio if order will be placed
  - note adding, with links

#### Statements page

- Shows total P&L by:
  - taking data from account snapshots
  - keep track of deposits (and handle currency exchange)
