# Global Food Production Clustering

This project uses unsupervised learning techniques to analyze global food production patterns based on FAO data. By applying clustering methods, this analysis aims to reveal trends in food and feed production, helping to inform food security strategies and resource allocation.

## Project Overview

- **Project Type**: Unsupervised Learning
- **Dataset**: [FAO Food Production Data (1961-2013)](https://www.kaggle.com/datasets/fauzantaufik/faocsv)
- **Clustering Algorithms**: K-Means and Hierarchical Clustering
- **Objective**: Cluster countries based on food production trends to provide insights into global food supply patterns and support food security initiatives.

## Dataset Description

The **FAO dataset** contains annual food production data for over 245 countries from 1961 to 2013, including key details such as:
- **Area Abbreviation/Code/Name**: Geographical identifiers for each country.
- **Item**: Type of agricultural product (e.g., Wheat, Rice, Maize).
- **Element**: Type of production, distinguishing between food for human consumption and feed for animals.
- **Annual Production Data**: Yearly production quantities in specified units, allowing trend analysis over time.

This dataset offers a comprehensive view of global food supply, critical for clustering countries based on production capacity and types.

## Methodology

### Data Preprocessing
- **Handling Missing Values**: Missing values in columns for specific years (e.g., Y2009, Y2010, Y2011) were filled with column averages to maintain continuity.
- **Encoding Categorical Variables**: Categorical columns like country names and product types were one-hot encoded to prepare the data for clustering.
- **Feature Engineering**: Aggregated data by country to analyze and compare food production trends across countries.

### Clustering Techniques
1. **K-Means Clustering**:
   - **Elbow Method**: Determined the optimal number of clusters by observing the elbow point at 2 clusters, indicating a primary split between high-production and lower-production countries.
   - **Cluster Assignments**:
     - **Cluster 1**: High-production countries, including China, the United States, and India, characterized by substantial food and feed output.
     - **Cluster 2**: Remaining countries with comparatively lower production levels.
   
2. **Hierarchical Clustering**:
   - **Dendrogram Analysis**: Confirmed the two-cluster structure, with visual cues for hierarchical relationships among countries based on food production levels.
   - This technique validated the initial K-Means clusters, ensuring robust and meaningful groupings.

## Results and Insights

- **Clustering Results**: Countries grouped by their food production capacity, with high-production nations (China, US, India) forming a distinct cluster. This division highlights the disparity in global food production and can guide focused resource distribution.
- **Implications**:
  - **Food Security**: Insights from clustering can aid policymakers in identifying key contributors to global food supply and planning interventions for countries with lower production.
  - **Resource Allocation**: High-production countries could be prioritized for strategic reserves and international aid coordination, while support for low-production countries could focus on boosting local food production.

## Project Structure

- **unsupervised_fao_food_clustering.ipynb**: Jupyter notebook containing the full analysis, including data preprocessing, K-Means and hierarchical clustering, and data visualizations.
- **FAO.csv**: The dataset used for this analysis, covering food production statistics by country and year.

## Visualizations

The project includes various plots for exploring and understanding food production patterns:
- **Country Production Trends**: Yearly production trends for major producers like China, US, and India, illustrating their dominant roles in global food supply.
- **Food vs. Feed Production**: Comparison of food and feed production to highlight agricultural output aimed at human consumption versus animal feed.

## Requirements

- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/global-food-production-clustering.git
   ```
2. Open the Jupyter notebook:

    ```bash
    jupyter notebook unsupervised_fao_food_clustering.ipynb
    ```

3. Execute cells sequentially to replicate the analysis and view results.

## Conclusion

This project demonstrates how unsupervised learning can uncover hidden patterns in global food production data. The clustering results offer a foundation for understanding the distribution of food resources and can support data-driven decision-making for global food security initiatives.

## License

This project is licensed under the MIT License.
