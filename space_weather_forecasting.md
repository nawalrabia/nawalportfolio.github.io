#### Enhancing Real Time Space Weather Using Complex Deep Learning Techniques
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/75eef2b6-11e4-4e9d-abfb-e360575e4ab0)


Geomagnetic fields play a pivotal role in various applications, from navigation systems to scientific research and space weather monitoring. Accurate modeling is essential for their reliable use. This project presents a benchmark study addressing the need for precise geomagnetic field modeling. The primary objective is to establish a standardized model for evaluating and advancing geomagnetic field models, utilizing real-time solar wind data to improve predictive performance.
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/c0023d3c-b28c-47d6-9fb1-ab00cd97c0b6)

##### Data Sources
- **NASA Advanced Composition Explorer (ACE)**
- **NOAA Deep Space Climate Observatory (DSCOVR)**

These satellites provide real-time solar wind data crucial for the project.

##### Tools
- **Programming Languages:** Python
- **Libraries and Frameworks:** TensorFlow, Keras, Scikit-learn
- **Data Visualization:** Matplotlib, Seaborn
- **Data Processing:** Pandas, NumPy
- **Deep Learning Techniques:** Long Short-Term Memory (LSTM), Gated Recurrent Unit (GRU), Recurrent Neural Network (RNN)

##### Data Cleaning/Preprocessing
- **Data Collection:** Gathered real-time solar wind data from ACE and DSCOVR satellites.
- **Data Cleaning:** Removed any anomalies or missing values in the dataset.
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/c8d21855-6d74-4e30-ab4b-0da9d0b7de94)
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/4ceba292-d5a2-4b26-8b78-fbdea802e50d)
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/cefb95fc-e2c2-433a-bc57-de648cc58fdb)



- **Normalization:** Scaled the data to ensure that it is within a specific range, suitable for neural network models.
- **Feature Engineering:** Created new features based on the raw data to improve model accuracy.

##### Exploratory Data Analysis
- **Data Visualization:** Few of solar wind parameters over time to identify patterns and anomalies.
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/beee1d34-d23e-47c4-9d0c-7000e5e50df6)
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/f59a97bc-5c17-4b52-97b6-8fd4b9833388)


- **Statistical Analysis:** Compute summary statistics to understand data distributions.
 
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/d12bca85-1c3b-49cc-9610-c8a001a19d99)
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/4cafc9b9-96b0-4977-9015-fca28a034b50)
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/6742edcd-0ff5-4d89-865e-ab63e50eec21)
  




- **Correlation Analysis:** Examined the relationships between different solar wind parameters and the DST index.
   ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/e800dfeb-b3c4-4d48-b07c-fcd6b5614b9a)

##### Data Analysis
- **Model Selection:** Evaluated different deep learning models including LSTM, GRU, and RNN.
   Selected best algorithm for the project with improved accuracy and lowest RMSE
   ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/736582b4-9d1f-4cdc-ad32-6bbb1f69e379)

  -
- **Training and Validation:** Split the dataset into training and validation sets, and train the models.
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/41661887-d335-41f8-a19f-3982e4a3d087)
 
- **Hyperparameter Tuning:** Optimize the model parameters for better performance.
   ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/9ecdbd4b-d236-46d7-ae61-91a56fcf774e)
   ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/a763274c-bd4d-46be-a6bd-c89ee8a4b427)
   ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/0cae9570-33d8-4f55-b813-0cf67bd0f654)
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/bfec8f57-61ca-4938-83fb-2446d382bcab)
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/69bcf38e-5049-49a9-896b-e5651cd5f57b)
   ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/45eddff4-e711-48fc-a825-41ab556d8f76)
   ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/cca77769-0599-43a1-8ada-5cee6a1e5a52)






  
  
 
- **Model Comparison:** Compared the performance of different models using standardized evaluation metrics.
- ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/14781110-5035-460f-87ce-c63437e2a263)


##### Results and Findings
- **Improved Predictive Performance:** The project demonstrated significant improvements in the accuracy of DST forecasting using advanced deep learning models.
  ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/97f8985f-bae8-4a5d-b2f9-09f95ebc26a8)
- Inference from Bi-LSTM +Bi-GRU Learning Curve
From epochs 1-5, both training and validation losses are high initially, indicating that the model is not performing well on the dataset. This could be due to the model learning the patterns and improving its performance. Epochs 6-10, the losses start to decrease, which is a positive sign. The model seems to be learning and generalizing better. Epochs 11-15, the losses continue to decrease, suggesting that the model is making progress The rate of improvement might slow down compared to earlier epochs. Epochs 16-20, there is a significant drop in both losses, indicating substantial improvement in the model’s performance. Epochs 21-30, the losses continue to decrease, but at a slower rate. Final epochs, the learning rate is reduced and both losses are relatively stable. The model might be approaching convergence.
 
The Learning Curve shows a typical pattern of a model learning from the data. The decrease in loss values indicates that the model is becoming more accurate in predicting the target values. The validation loss is close to the training loss, suggesting that the model is generalizing well to unseen data. The choice of the learning rate schedule, dropout rate and other hyper-parameters seems to be effective for this model.

![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/04827ca7-1ba8-4ee6-a0e0-62d4ed33d5da)
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/b602195d-2182-405e-a559-eccb5dee879b)
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/437bb636-fb3e-4c81-b125-c09ebbdcc48d)




- **Model Benchmarking:** Established a benchmark dataset and evaluation metrics for geomagnetic field modeling.

 ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/dbfb1166-17d3-4b6d-97b6-434e002ade4b)


- **Operational Viability:** The developed models showed high operational viability for real-time forecasting.
- **Impact:** Accurate DST forecasts are crucial for satellite operators, power grid operators, and users of magnetic navigation systems, enhancing reliability amidst geomagnetic disturbances.

### Overall Conclusion
•	The Bi-LSTM + Bi-GRU model stands out as the best-performing model, balancing complexity and predictive accuracy.
•	Learning curves provide insights into the training process, showcasing model adaptation and potential convergence.
•	Ensemble approaches demonstrate the strength of combining different model architectures for improved predictions.
•	Systematic hyperparameter tuning ensures optimal model configurations across experiments.
•	Early stopping contributes to training efficiency and prevents over-fitting, promoting a more reliable and robust model.

