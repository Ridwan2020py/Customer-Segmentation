🎯 Project Overview
This project implements unsupervised machine learning techniques to segment mall customers based on their annual income and spending patterns. The analysis identifies distinct customer groups that can be leveraged for:

Targeted Marketing Campaigns
Product Development Strategies
Customer Retention Programs
Personalized Shopping Experiences
Resource Optimization

⭐ Key Features
🔍 Comprehensive Data Analysis

Exploratory Data Analysis with statistical summaries
Outlier detection using box plots
Missing value analysis
Feature correlation analysis

🎯 Advanced Clustering Techniques

K-Means Clustering with optimal cluster determination
DBSCAN Clustering as an alternative approach
Parameter tuning and optimization
Silhouette analysis for cluster validation

📊 Rich Visualizations

Elbow method for optimal K selection
2D cluster scatter plots (original and scaled features)
Cluster size distribution charts
Average spending analysis by cluster
Interactive and publication-ready plots

🧮 Statistical Analysis

Detailed cluster characteristics
Customer segment interpretation
Advanced statistical summaries
Performance metrics comparison

📊 Dataset Information
Source: Mall Customer Dataset (Kaggle)

Size: 200 customer records
Features Used:

Annual Income (k$): Customer's yearly income in thousands USD
Spending Score (1-100): Score based on customer behavior and spending nature



Data Quality:

✅ No missing values
✅ No duplicate records
✅ Minimal outliers detected
✅ Features are well-distributed

🚀 Installation & Setup
Prerequisites
bashPython 3.7 or higher

Install Dependencies
bashpip install pandas numpy matplotlib seaborn scikit-learn
Or using requirements.txt:
bashpip install -r requirements.txt
Download Dataset

Download Mall_Customers.csv from Kaggle
Place the file in the project directory or update the file path in the script

💻 Usage
Basic Execution
bashpython mall_customer_segmentation.py
In Jupyter Notebook
python# Import and run the analysis
exec(open('mall_customer_segmentation.py').read())
Google Colab

Upload the script to Google Colab
Upload the dataset to /content/sample_data/
Run all cells

🔬 Methodology
1. Data Preprocessing
python# Feature selection and scaling
features = df[['Annual Income (k$)', 'Spending Score (1-100)']]
scaler = StandardScaler()
features_scaled = scaler.fit_transform(features)
2. Optimal Cluster Selection

Elbow Method: Analyzes Within-Cluster Sum of Squares (WCSS)
Silhouette Analysis: Measures cluster cohesion and separation
Results: Optimal K = 5 clusters

3. K-Means Implementation
python# Apply K-Means clustering
optimal_k = 5
kmeans = KMeans(n_clusters=optimal_k, random_state=42, n_init=10)
cluster_labels = kmeans.fit_predict(features_scaled)
4. Alternative Clustering (DBSCAN)
python# Parameter tuning for DBSCAN
eps_values = [0.3, 0.5, 0.7]
min_samples_values = [3, 5, 7]
# Best parameters automatically selected based on silhouette score
📈 Results & Insights
🎯 Customer Segments Identified
ClusterSizeAvg IncomeAvg SpendingInterpretation022%$26k20Budget Conscious Customers118%$87k17Conservative High Earners221%$27k79Young/Impulsive Spenders320%$88k82High Value Customers419%$56k49Average Customers
🔍 Key Findings

High Value Customers (20%): Target audience for premium products
Conservative High Earners (18%): Potential for conversion campaigns
Young Spenders (21%): Opportunity for credit/financing products
Budget Conscious (22%): Focus on value-based marketing
Average Customers (19%): Standard marketing approaches

📊 Model Performance

Silhouette Score: 0.554 (Good cluster separation)
WCSS: Optimal elbow at K=5
Cluster Validation: Clear, well-separated segments

💼 Business Applications
🎯 Marketing Strategy

Personalized Campaigns: Tailor messages for each segment
Product Recommendations: Segment-specific product suggestions
Pricing Optimization: Dynamic pricing based on customer value

📈 Revenue Optimization

Cross-selling: Target high-value customers with premium products
Up-selling: Convert conservative earners to higher spending
Retention: Develop loyalty programs for valuable segments

🎨 Customer Experience

Store Layout: Optimize based on customer shopping patterns
Service Level: Provide premium service to high-value segments
Communication: Customize interaction style per segment

Areas for Contribution

 Additional clustering algorithms (Hierarchical, Gaussian Mixture)
 Interactive dashboards using Plotly/Streamlit
 Advanced feature engineering
 Model deployment using Flask/FastAPI
 Real-time clustering pipeline

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
📞 Contact
Ridwan Hamzah - hamzahridwan2018@gmail.com
Project Link: https://github.com/Ridwan2020py/Customer-Segmentation
LinkedIn: https://www.linkedin.com/in/ridwan-hamzah-798865292/

🌟 If you found this project helpful, please give it a star! ⭐

🎖️ Acknowledgments

Dataset provided by Kaggle
Inspired by real-world retail analytics challenges
Built with ❤️ for the data science community.
