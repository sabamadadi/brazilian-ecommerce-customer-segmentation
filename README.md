# Segmenting Brazilian E-Commerce Customers and Testing Free-Shipping Uplift

[Full Report](https://drive.google.com/file/d/16Yll-TLgkBZLYHGpmfuqecWZ8Bna47QZ/view?usp=sharing)

This project explores the Olist public e-commerce dataset, which includes anonymized, multi-year transaction-level data from 2016–2018. The goal is to segment Brazilian customers and evaluate the impact of free-shipping incentives.

Data preprocessing involved cleaning, merging multiple CSVs, converting Portuguese categories to English, and deriving features such as total spend, order cadence, average basket, tenure, and sentiment scores from reviews. Outliers were Winsorised and sampling was applied to manage RAM constraints.

Three clustering approaches were tested: k-means, DBSCAN, and hierarchical (Ward/average linkage). K-means with eight clusters was selected for interpretability and stability, supported by PCA and t-SNE visualizations. UMAP was used for storytelling but not for production scoring due to its non-parametric nature. Gaussian Mixture Models confirmed temporal stability between 2017 and 2018.

Clusters were profiled by customer value, average spend, review scores, favorite categories, and acquisition channels. Premium customers showed high spend and positive sentiment, whereas price-sensitive segments were more responsive to free-shipping promotions.

Acquisition channels mapped differently across clusters, highlighting opportunities for targeted marketing. Most orders lacked attribution, emphasizing the need for proper UTM tracking.

Key takeaways: eight interpretable behavioral clusters provide actionable insights, acquisition channels align with segments, and free-shipping incentives are most effective for price-sensitive customers. Future work could include transformer-based sentiment analysis, HDBSCAN clustering, and formal causal modeling for uplift.
