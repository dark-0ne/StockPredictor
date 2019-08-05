## Stock market prediction using LSTM
Stock prices are Sequential in nature and are best analyzed as time series data. Therefore I used a Long short-term memory here to predict a stock in FOREX market.

### Data
Stock predicted is EURUSD (Euro to U.S. Dollar ratio). Along daily closing prices I used other inputs and indicators such as:
* EURCAD and GBPUSD daily closing prices
* Market indicators of stock exchanges
  * NASDAQ and NYSE for U.S. stock exchange
  * BSE SENSEX for Indian stock exchange
  * HSI for Hong Kong stock exchange
  * Nikkei225 for Tokyo stock exchange
* Global economy indices
  * Daily volatile index (VIX)
  * London Inter-Bank Offered Rate (LIBOR)
* Technical indicators
  * Standard moving averages and exponential moving averages
  * MACD
  * Bollinger Bands
  * Momentum
* Fourier Transforms for trend detection
### Model
2 LSTM layers with 2 dense fully-connected layer is used. The results shown below are acheived with minimal hyperparameter tuning and short training time.
For better results you can try tweaking the parameters and letting the model train longer.
