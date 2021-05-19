

In this paper, I use a publicly available food commodity prices at select Ethiopian markets from the Famine Early Warning Systems Network (FEWS NET) to explore price transmission and market integration in Ethiopia. 

I narrowed the study first to Maize Grain (White), restricting the dataset to seven markets from January 2020 to March 2021 due to data availability. In Figure 1, above, we can see at first glance that prices trend upwards together in this period. Maize is the second most produced crop in Ethiopia, after teff, at 9,635,735 metric tons in 2019 (FAOSTAT).  Maize is also an incredibly important staple in the Ethiopian diet; domestic production meets 95% of national consumption (Abate et al. 2015). 


This study primarily follows the work of Nicholas Minot and his paper on the “Transmission of World Food Price Changes to Market” (Minot 2010). We rely on a Vector Error Correction Model (VECM) to explore the link between Domestic prices for given commodities in Ethiopia. The VECM will test two markets at a time, allowing us to understand (1) the long-run elasticity of one market’s price with respect to the other market’s price, (2) the speed of adjustment, and (3) the short-run elasticity of one price with respect to the other.

As in Minot (2010), the analysis begins with confirming that the VECM is appropriate by setting two pre-conditions: (1) The variable is Non-Stationary and integrated to degree 1, I(1), meaning it follows random walk, but first difference (Xt - Xt-1) is stationary. We use the Augmented Dickey-Fuller (ADF) test to determine stationarity. (2) The two variables of interest are cointegrated, such that PriceBt = α + β PriceAt + ε or PriceBt - α - βPriceAt = ε, where ε is stationary. This is done using the Johansen test.


With these conditions met, we can proceed with estimating a VECM. Minot simplifies a standard VECM to the context by (1) assuming that all domestic markets are in small countries such that they do not influence the world price and (2) using only one lag as tests indicate this is sufficient. We are only looking at domestic markets and therefore assumption (1) does not hold. To account for this, we will test for granger-causality. Our specification will make the same (2) assumption that one lag is sufficient. The specification is as follows:

```math
\Delta. Dometic Price_{t} = \alpha + \Theta.(Domestic Price_{t-1} - \beta. World Price_{t-1} ) + \delta.\Delta. World Price_{t-1} + \rho.\Delta. Domestic Price_{t-1} + \epsilon_{t}
```
where `$ Domestic Price_{t} $` is the log of domestic price converted to real U.S. dollars. 

`$ World Price_{t} $` is the log of world price of the same commodity in real U.S. dollars, 

`$ \Delta $` is the difference operator, so `$ \Delta. Price_{t} = Price_{t} – Price_{t-1} $`.  

Finally, `$ \alpha. , \Theta. , \beta. , \delta. , and \rho. $` are estimated parameters and εt is the error term in time t.

