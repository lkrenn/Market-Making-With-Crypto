# Market Making Strategy with Crypto

In this notebook, I will be implementing the market-making methodology outlined in Avellaneda and Stoikov's popular market making whitepaper titled High-Frequency Trading in a Limit Order Book. The paper can be found for free here: https://www.math.nyu.edu/~avellane/HighFrequencyTrading.pdf

In the whitepaper, the optimal behaviour of a market maker given certain assumptions is derived. Ultimately, this derivation yields a spread used to calculate the optimal placement for limit order, which is defined as follows:

<p align="center">
  <img src="./img/spread.png" width="350" title="hover text">
</p>

This spread is defined around a reservation price i.e. a price at which a market maker is indifferent between their current portfolio and their current portfolio $\pm$ a new share. The reservation price is derived in the whitepaper as follows:

<p align="center">
  <img src="./img/r_price.png" width="350" title="hover text">
</p>

We can get an idea of how this model works by considering the chart below. Red dots indicate that a market order has been submitted and has filled one of our ask-limit-orders. Similarly, a green dot indicates that a market order has filled one of our buy-limit-orders. 

<p align="center">
  <img src="./img/sim.png" width="1000" title="hover text">
</p>

# Partial Results

While the model still has a ways to go to be considered sufficient, the following chart demonstrates how it works thus far: 

<p align="center">
  <img src="./img/ETH_backtest.png" width="1000" title="hover text">
</p>

The ask-limit-order line appears to be covered by the mid-price line. This means that at this point in time, the model seeks to sell more inventory than buy. 
