# Nasdaq Stock Recommendation Project
Stock recommendation system that recommends potential Nasdaq shares considering both investment habits and risk management considerations of the investors.

## Project Purpose
Developing recommendation system which identifies potential shares for the holder of a specific share where the recommended share is distant enough for risk management purposes but carries similar financial attributes with the currently held share.

## Dataset

### Data Source
* Wharton Research Data Services
* Nasdaq

### Data Description
* 2014-2018 financial data of 2000 common shares (68 financial features)
* 2017-2018 share prices

### Feature Examples
#### Balance Sheet Ratio Examples: 
* Asset turnover rate
* Debt to equity
* Debt to assets
#### Income Statement Ratio Examples: 
* Gross profit margin
* Operating margin
* Interest to average debt
#### Return Ratio Examples: 
* Price to earnings
* Dividend pay-out
* Return on invested capital
#### Cash Flow Ratio Examples: 
* Current ratio
* Free cash flow to operating cash
* Acid test ratio

## Project Outline
* Data Collection
* Data Preprocessing & Scaling
* Dimensionality Reduction with **PCA & t-SNE** (2D & 3D t-SNE applied separately)
* Clustering of Both 2D & 3D t-SNE Results Separately with **K-Means** and **DBSCAN**
* Cluster Predictions of New Stocks with **Random Forest** (stocks with new IPOs)
* Model Selection with **Variation Analysis** of new stocks
* **Evaluation Metric** used for Variation Analysis : (1 - (Predicted Share’s Return% - Cluster’s Return%)  / (Predicted Share’s Return% - Nasdaq Index Return% ))
* Selected Clustering Model: **DBSCAN & 2D t-SNE**
* Stock Recommendation with **Cosine Similarity**
* **Recommendation Method:** For each share, the highest similar share from the clusters different from its own is selected. (Recommended stocks are selected from different clusters due to risk management purposes)
