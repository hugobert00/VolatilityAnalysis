# VolatilityAnalysis
The goal of this program is to have a great streamline interface on which you can do all your volatility analysis, you can just plug and play your data base/API (own sheets, Refinitiv, Barnhart's...). 

The language used is Python 

What are the different volatility analysis available ? 

1- A complete historical analysis : 
you just have to choose the Underlying you are interested in/ you have data for, and you can have different computations with different methods, you can choose the best method for you, the rolling window in the caculation... Mathod available are:
      - Clasic CLose To Close --> Simple to compute using readily available daily closing prices, but ery inefficient, discards intraday price information, leading to significant        sampling error​.
      - Parkinson --> Around five times more efficient than close-to-close by incorporating daily high-low ranges, but downwards biased due to ignoring opening jumps and assuming        continuous prices​.
      - Yang Zang --> Corrects for both drift and opening jumps, achieving very high efficiency (up to 14 times that of close-to-close), but performance declines when volatility         is dominated by overnight gaps, and it is more complex to implement​.
      - I have excluded Garman - Klass but you can easily add it

The display are the same for each computation method: 
      - A simple display of the volatility available for different windows that you can have on the same graphic to compare (20d, 40d, 60d, 120d) 
      - A continuous display of the volatility along years (available windows = 20d, 40d, 60d, 80d) 
      - Volatility cones
      - Volatility ratios --> ex VolParkinson/ Close to Close

2- A complete Implied volatility analysis, for a selected Underlying A :
      - Volatility Smiles 
      - IVM term curve 
      - 3D surface 
      - a supperposition of the smile/IVM term curve or Smile Vs historical vol is possible and soon t-with the forcast
      - a heat map with for each strike the spread between the Historical Vol and the IVM 
      - a heat map with for each strike the spread between the forcasted vol and the IVM 


3- Incoming : Integration of volatility forecasting 
