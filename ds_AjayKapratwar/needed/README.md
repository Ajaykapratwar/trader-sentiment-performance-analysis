# Trader Behavior & Market Sentiment Analysis

## 📌 Objective
This project explores the relationship between **market sentiment** (Fear/Greed Index) and **trader performance** using historical trading data from Hyperliquid.  
The goal is to identify patterns, correlations, and actionable insights that can drive smarter trading strategies.

---

## 📂 Datasets
1. **Bitcoin Market Sentiment Dataset**  
   - Columns: `timestamp`, `value`, `classification`, `date`  
   - Classification categories: *Extreme Fear, Fear, Neutral, Greed, Extreme Greed*

2. **Historical Trader Data (Hyperliquid)**  
   - Columns include: `Account`, `Coin`, `Execution Price`, `Size Tokens`, `Size USD`, `Side`, `Timestamp IST`, `Start Position`, `Direction`, `Closed PnL`, `Leverage`, etc.

---

## 🛠️ Steps & Methodology
1. **Data Cleaning**
   - Checked for missing values and duplicates (none found).
   - Standardized column names.
   - Converted timestamps to `datetime` format.
   - Adjusted for time zone differences (IST → UTC).
   - Extracted only the date for alignment.

2. **Data Merging**
   - Joined sentiment data with trading data on the `date` column.

3. **Exploratory Data Analysis (EDA)**
   - Average Closed PnL by sentiment classification.
   - Leverage usage patterns in different sentiment regimes.
   - Win rate comparisons across sentiments.
   - Trade volume distribution by sentiment.
   - Identification of top-performing traders per sentiment.

4. **Correlation Analysis**
   - Encoded sentiment scores and checked correlation with PnL, leverage, and trade size.

5. **Key Metrics Calculated**
   - Average PnL
   - Win Rate (%)
   - Average Leverage
   - Average Trade Size (USD)
   - Trader rankings by sentiment

---

## 📊 Key Findings
- **Contrarian Potential**: In some cases, “Fear” and “Extreme Fear” periods showed higher win rates than “Greed” phases.
- **Risk Behavior**: Leverage usage spikes in “Greed” phases, increasing both profit potential and loss risk.
- **Trader Specialization**: Certain traders consistently outperform in specific sentiment regimes, suggesting adaptable or contrarian strategies.
- **Correlation Insights**: Sentiment has a moderate relationship with leverage but a weaker direct link to PnL — other factors play a big role.

---

## 💡 Recommendations
1. **Contrarian Strategy**: Explore opportunities in Fear-dominated markets rather than chasing Greed.
2. **Dynamic Leverage**: Adjust leverage based on sentiment — higher in favorable setups, lower in risky emotional phases.
3. **Track Top Performers**: Monitor and learn from traders who excel in specific sentiment regimes.
4. **Combine Signals**: Use sentiment in conjunction with technical and on-chain data for stronger predictions.

---

## 📦 How to Run
1. Clone the repository or download the notebook.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scikit-learn
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Trader_Behavior_Sentiment_Analysis.ipynb
   ```
4. Run all cells to reproduce the analysis.

---
