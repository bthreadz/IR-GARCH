# Index Reversion GARCH

Generalized Auto-Regressive Conditional Heteroscedasticity (GARCH) is a time series model used to forecast variance on top of some mean process. In this notebook this model is applied to the daily returns of three equities: International Consolidated Airlines Group (IAG.L), Renault (RNO.PA) and Wells Fargo & Company (WFC) for the purpose of forecasting daily Value at Risk (VaR). The concept of VaR is explained and an introduction to GARCH models is provided.

Various of combinations of GARCH models, sample sizes and mean processes are compared over a test period from 1<sup>st</sup> March to 1<sup>st</sup> October 2020. Observing an underestimation of risk for RNO.PA and WFC across the test period, a new model is proposed in which the reversion term omega is modified to include the 30 day rolling variance average of a given equity index. We call this adjustment Index Reversion (IR) GARCH and an improvement in results is observed for both equities.

The code for this project can be found within IR_GARCH.ipynb, to render this file in full please use [this link](https://nbviewer.jupyter.org/github/bthreadz/IR-GARCH/blob/main/IR_GARCH.ipynb). With the exception of the FTSE data, all data was acquired through Yahoo Finance directly using pandas datareader. Unable to extract the data directly, the FTSE data was manually extracted and is located within ^FTSE.csv.