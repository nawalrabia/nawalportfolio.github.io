# USED CAR SALES IN GERMANY 
![fe_329171_1600](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/cb4d510e-f030-42ec-a777-fb1f90dfb056)
### Abstract
This study investigates the factors influencing used car prices in Germany using a comprehensive Kaggle dataset. By applying data analysis and machine learning techniques, we identify key relationships between car attributes and selling prices. Utilizing Linear Regression, Decision Tree Regression, Random Forest Regression, and Gradient Boosting Regression for predictive modeling, the Gradient Boosting model demonstrates the highest accuracy. Leveraging PySpark for big data processing and visualization tools like Tableau, Matplotlib, Pandas, and Seaborn, we provide valuable insights for optimizing pricing strategies in the used car market.
### Objectives
1. **Employ PySpark for data loading and processing:** Utilize PySpark to handle and process the dataset efficiently.
2. **Perform data exploration and analysis:** Apply suitable techniques to explore and understand the data.
3. **Visualize data using Tableau or Python libraries:** Use visualization tools to interpret findings effectively.
4. **Implement machine learning models:** Evaluate and apply models like Linear Regression, Decision Tree, Random Forest, and Gradient Boosting for price prediction.
5. **Discuss findings and insights:** Present a detailed discussion of the results and their implications for the used car market.
### Dataset
This study investigates factors influencing used car prices in Germany using a comprehensive dataset from eBay. The dataset contains 371,539 rows with various attributes related to used cars. Extensive data cleaning was performed, including removing non-contributing features and outliers, such as cars with implausible registration years. The summarized dataset, consisting of 371,539 rows and 11 columns, was used for analysis. German terms were translated to English for clarity. Using PySpark for data processing and various machine learning models, the study provides insights to optimize pricing strategies in the used car market.
### Data Loading
PySpark, a Python-based API for Apache Spark, facilitates processing large datasets efficiently using parallel computing. Written in Scala, Spark integrates with Python, Java, SQL, Scala, and R. Py4j library enables PySpark to operate seamlessly with these languages, offering benefits like resilient distributed datasets, high-speed processing, and caching. This project primarily uses Spark SQL for computations and employs Tableau, Pandas, Seaborn, and Matplotlib for data visualizations.
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/35c23d8e-a014-4a44-993a-6c9ac7916f84)

o	Duplicates are dropped
o	Missing and null values are fetched and replaced with most frequently occuring values in respective column
o	Outlier removal:
Outliers are extreme values that can skew analysis.
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/061ac300-9e9a-4952-81c0-f9a71ec4c723)
### Exploratory Data Analysis using Tableau
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/a8c1840d-91be-4b6f-b05d-c7817cbe88ac)
Approximately 40 distinct branded cars are present in dataset which are available for Used Car Sales
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/2f625651-d72a-49fb-94ea-fa197b5c13e8)
The correlation values provided reveal how different variables in the dataset are related to 
each other and to the target variable "price." Positive correlations indicate that when one 
variable increases, the other tends to increase as well, while negative correlations suggest 
that one variable increases as the other decreases.
From the given correlations:
-	Higher "yearOfRegistration" values are positively correlated with higher "price,"
Indicating that newer cars generally have higher prices.
-	Cars with more "powerPS" tend to have higher "price" values, as shown by their 
positive correlation.
-	"kilometer" has a negative correlation with "price," meaning that cars which ran 
more kms usually have lower prices.
These correlation insights offer a concise way to understand how various factors influence 
the pricing of used cars in the dataset.
### Building pipeline
First , it is essential to transform the data into a suitable format for machine learning.
StringIndexer encodes categorical string variables into numerical indices making it possible 
to include these features in Machine Learning pipeline and also assembled along with 
numerical variables using  VectorAssembler() 
(DataFrame-based MLlib documentation has been used to create pipeline)
The data has been preprocessed by converting categorical columns into numerical indices 
using StringIndexer.It then combines all relevant features including numeric and indexed 
categorical ones, into a single feature vector using VectorAssembler.Finally it divides the 
prepared data into training and testing  sets for model training and evaluation.
### Results
GBTRegressor performed better than other models .
Results without hyperparameter tuning are summarized in the below 
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/1efec5b6-ca61-4801-ba90-ba9f302219aa)

Results with hyperparameter tuning using random combination :
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/f2f6bfdc-bf20-4792-b642-0ac08dea6784)

![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/2fcfe785-14b4-466e-8307-9752878332ec)

Actual Vs Predicted Price for different models
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/7b02989c-b98c-43b3-8902-a38f8225ecf0)
### Conclusion
This project investigates the factors influencing used car prices in Germany using a dataset from eBay. The raw data, comprising 371,539 rows, underwent extensive cleaning to remove non-essential columns, outliers, and translate German terms to English for better comprehension. 
Key insights from the exploratory data analysis (EDA) included:
- Cars without or with repaired damage are priced higher.
- Newer cars and those with higher power tend to have better prices.
- Higher mileage generally decreases prices, except for luxury brands like Porsche.
- Automatic transmission cars usually fetch slightly higher prices.
- Brand rankings show Porsche, Land Rover, and Audi as the most expensive used car brands.

Correlation analysis showed that newer registration years and higher power are positively correlated with higher prices, while higher mileage negatively impacts prices.
The study evaluated four machine learning models: Linear Regression, Decision Tree, Random Forest, and Gradient Boosting Trees (GBT). The GBT model demonstrated superior performance with lower RMSE, higher r-squared, and lower MAE. Hyperparameter tuning notably improved the Decision Tree and Random Forest models' performance. Overall, the GBT model consistently provided the best predictions.
## Ethical aspect and Social Impact
- Positive Social Impact and Ethical Considerations:The analysis of used car sales has the potential for several positive social impacts. Firstly, it encourages responsible choices and environmental sustainability by extending the lifespan of cars, reducing the need for new vehicle production, and minimizing carbon emissions. Additionally, by providing insights into fair pricing and accurate information, the analysis promotes transparency and empowers consumers to make informed decisions. This can lead to increased trust in the market and fair treatment of buyers and sellers, fostering a healthier business environment.
- Negative Social Impact and Ethical Considerations:However, there are ethical concerns and potential negative social impacts that need to be addressed. If the analysis is not conducted with integrity, it may lead to manipulation of prices, misrepresentation of vehicle conditions, and exploitation of consumers. Unethical practices could erode trust in the used car market, leading to a decline in consumer confidence and harming both buyers and sellers. Moreover, if the analysis is used to discriminate against certain groups or perpetuate biased pricing, it could exacerbate social inequalities and perpetuate injustice.

In conclusion, while the analysis of used car sales can bring positive social impacts through responsible choices and transparency, ethical considerations are vital to prevent potential negative consequences that may harm individuals and the society. Striking the right balance between promoting fair practices and preventing unethical behavior is essential for maximizing the benefits of this analysis while minimizing its drawbacks.






