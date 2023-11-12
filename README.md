# Financial-Security-Institute-NH
## Analysis and Prediction Model Development of the Correlation between Online Item-specific Consumer Data and Stock Indices

### Background and Significance:
- Increasing Interest in Consumer Behavior: The importance of consumer behavior has been highlighted due to the COVID-19 pandemic.  
- Rise in Online Consumption Amidst COVID-19: A growing trend in online consumption and increased participation of individual investors in the stock market.  
- Heightened Individual Interest in Stocks.

<p align="center">
 <img src="https://github.com/rootofdata/Financial-Security-Institute-NH/assets/86711374/4c58d1fe-5ab5-43fc-8201-3481bf6da632",width="500" height="400/">
</p> 

### Idea and Analysis:
- Understanding the Relationship between Consumption and Stocks: Analyze the correlation between online consumption and stock indices to develop a predictive model.
- Visualization of Consumption Data: Derive major categories through visualization of online item-specific consumer data.
- Setting Stock Indices for Four Categories: Set stock indices according to major categories and calculate market capitalization for relevant stocks.

<p align="center">
 <img src="https://github.com/rootofdata/Financial-Security-Institute-NH/assets/86711374/1e36ff19-ada3-4625-bcc2-a5653e2103c6",width="550" height="350/">
</p> 

- Upsampling of Data: Generate more data through upsampling of online consumer data.
- Handling Multicollinearity: Reduce explanatory variables using correlation analysis and PCA techniques to handle multicollinearity.
- Regression Analysis for Stock Indices: Use models like RandomForestRegressor for predicting stock indices, enhancing model performance through hyperparameter tuning.
- Analysis of Variable Importance in Regression Equation: Analyze importance of variables in the model after dimensionality reduction using PCA.
- Comparison of Actual Values and Predicted Stock Trends for Proof of Concept (PoC): Validate the model by comparing the directionality of actual and predicted values.

<p align="center">
 <img src="https://github.com/rootofdata/Financial-Security-Institute-NH/assets/86711374/f3c85b95-fce7-46c5-8dd8-ed3a55eb0f7e",width="450" height="300/">
</p> 

### Summary of Analysis:
- Confirmed strong positive correlation between online consumption and stock indices.
- E-commerce products/services played a crucial role in predicting stock trends among major categories.
- Enhanced model accuracy through handling multicollinearity and variable reduction.
- Validation of model accuracy through PoC, comparing actual and predicted trends.

|Algorithm|MSE|R2MSE|Variancescore|
|:------:|---|:---:|:---:|
|RandomForestRegressor|0.093|0.305|0.750|
|GBMR80egressor|0.115|0.339|0.692|
|XGBRegressor|0.102|0.319|0.727|
|LGBMGRegressor|0.579|0.761|-0.556|

### Analysis Results:
- Indicators closely related to consumption can increase expected returns.
- Future stock price prediction using regression models: Identified variables highly correlated with consumption patterns, indicating age groups above 30 exhibit significant correlation with stock movements. By monitoring these variables, future stock fluctuations can be predicted in advance, leading to potentially profitable investments.
- Consequently, making investments based on these findings could increase expected returns and guide successful investments.

### Expected Impact:

#### Increased Expected Returns through Correlated Indicators:
- Identified variables closely related to consumption. For instance, consumption patterns among age groups above 30 showed significant correlation with stock movements. By monitoring variables strongly correlated with stock indices, anticipating stock fluctuations becomes possible, potentially increasing expected returns.

#### Future Stock Price Prediction Using Regression Models:
- The developed regression model can be used to predict the directionality of future stock prices. Investors can narrow down their choices of related companies based on these predictions, reducing investment risks.

#### Potential Advancements in Regression Models:
- The developed regression model demonstrated minimal discrepancies between predicted and actual values. This is highly promising, indicating that with increased data volume, the model can further evolve into a more precise and accurate tool for future predictions.

### Utilized Data Sources:
- BC Card Online Item-specific Consumer Data
- KRX (Korea Exchange) All Stock Price Changes [http://data.krx.co.kr/contents/MDC/MAIN/main/index.cmd]
- KRX All Stock Market Prices [http://data.krx.co.kr/contents/MDC/MAIN/main/index.cmd]
- Online Shopping Trends Survey [https://kosis.kr/index/index.do]
- Consumer Sentiment Index [https://kosis.kr/index/index.do]
- Private Consumption Growth Rate (Real, Seasonally Adjusted, Year-on-Year) [https://ecos.bok.or.kr/jsp/vis/keystat/#/key]
- COVID-19 Confirmed Cases [http://ncov.mohw.go.kr/]
- Consumer Price Index [https://kostat.go.kr/incomeNcpi/cpi/cpi_td/2/1/index.action?bmode=cpidtval]
- Economic Sentiment Index [https://ecos.bok.or.kr/jsp/vis/keystat/#/key]
