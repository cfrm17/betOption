# Bet Option Valuation

A pricing model for bet options is presented by using Monte Carlo simulation.  A bet option is a bet on a basket of stocks.  There are multiple reset periods before the maturity of the option.  At the end of each period, if all the stocks in the basket are above their respective strikes, the option will payout a rebate amount for this period at maturity.

Let m be the number of assets in a given basket,   be the price process of the jth underlying asset in the basket and  .  Let   be a set of reset dates and   be a payoff settlement date or maturity.  The bet option on the basket of stocks is a European style derivative security whose matured payoff at the settlement date T is given by

				  

where   is the rebate amount, I is the indicator function, and   is the strike for each individual stock in the basket.  The bet option defined above is essentially a series of multivariate digital options with a common payoff settlement date.

Let t be the current value date, then the current value of this derivative security can be written as

			 

where   is the discount factor at the value date (see https://finpricing.com/lib/FxForwardCurve.html). The above formulae are in a world that is forward risk-neutral with respect to a specific currency  .  

If an underlying asset j is measured in another currency  , the governing price dynamics of this underlying asset in the risk-neutral world of   should be written as

			 

where   is the short rate of  ,   is the dividend yield of the asset,   is the correlation coefficient between the asset price and the cross-currency exchange rate,   is the volatility of the asset price,   is the volatility of the exchange price, and   is the Wiener process.  

Asset prices in the basket are correlated with   where  ’s are constant correlation coefficients between the logarithmic asset prices.  All these parameters are assumed deterministic.

Monte Carlo simulation associated with stratified sampling variance deduction is employed to evaluate the option.  


