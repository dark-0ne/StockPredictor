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
2 LSTM layers with 2 dense fully-connected layers are used.
![Model screenshot](/screenshots/model.png)
### Results
The results shown below are acheived with minimal hyperparameter tuning and short training time.
For better results you can try tweaking the parameters and letting the model train longer.
<br>![Train Performance Screenshot](/screenshots/train.png)![Validation Performance Screenshot](/screenshots/val.png)
<br>![Train and loss error screenshot](/screenshots/loss.png)


#### Note
This work is mainly based on [this article](https://towardsdatascience.com/aifortrading-2edd6fac689d). Due to the fact that the original author refrained from providing the source code for the work claimed done, in this project I tried to implement some of the methods mentioned by him to best of my understanding. Some major parts mentioned by him (such as ARIMA - NLP analysis - GAN and RL techniques - ...) are completely left out of this project as of now but may be added in near future. <br>It should be mentioned that the stock market prediction is a highly complex and volatile matter and accurate prediction requires much more knowledge than simple stock prices and indices. Therefore the results shown above could be highly improved by adding mentioned methods to the existing model.
