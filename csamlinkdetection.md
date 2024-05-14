# CSAM Link Detection App using Machine Learning Techniques
## ABSTRACT
The project's main objective is to develop a comprehensive solution to combat CSAM links, by leveraging the power of advanced machine learning and cloud-based technologies. Central CSAM Intelligence System a cloud-based algorithms to detect and disrupt CSAM links and report them to relevant authorities and link shortening service providers.
## INTRODUCTION
![F0dSHJaWIA0uSBn](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/8a3fd44b-456e-45ba-8e81-feec57954e5b)

Child Sexual Abuse Material (CSAM) remains a significant issue on the internet, posing a grave threat to society's most vulnerable members. As technology advances, perpetrators continuously find new ways to obfuscate CSAM links to evade detection and dissemination. To combat this, leveraging advanced Machine Learning (ML) techniques is a promising approach. This literature review aims to explore existing research on the detection and prevention of CSAM links using ML, focusing on key methodologies, features, and advancements.
The proliferation of child sexual abuse material (CSAM) on the internet is a significant global problem that requires immediate attention. The increase in the number of reports of suspected CSAM highlights the need for effective and efficient measures to detect and prevent its spread. According to the National Centre for Missing and Exploited Children (NCMEC), the number of reports of suspected CSAM increased from 983,734 in2019 to 21.7 million in 2020, a staggering 2,100% increase. According to a report from the International Centre for Missing and Exploited Children (ICMEC), there were over 17 million reports of CSAM globally in 2020.The majority of CSAM is shared through file-sharing networks and peer-to-peer sharing, with websites accounting for a smaller percentage of distribution.
The market opportunity for a comprehensive solution that can detect and prevent CSAM links is significant, as parents, households, and law enforcement agencies are actively seeking tools to protect themselves and their communities from this growing problem.
## DATA COLLECTION
The dataset utilized in this project serves as a critical foundation for developing and training models aimed at combatting Child Sexual Abuse Material (CSAM) online. Initially, due to challenges in acquiring real-world CSAM URLs promptly, a synthetic dataset was crafted. This synthetic dataset provided a valuable resource for early model development, allowing researchers to begin their work despite delays in obtaining authentic data. To ensure the dataset's relevance and accuracy, interviews were conducted with domain experts from organizations such as INTERPOL, Internet Watch Foundation (IWF), and the Child Exploitation and Online Protection Command (C3P). These interviews, conducted through structured questionnaires, aimed to extract insights into the distribution tactics of CSAM. Furthermore, a crucial partnership was established with the IWF, facilitating access to authentic CSAM URLs datasets. This collaboration greatly enhanced the model's accuracy and effectiveness by incorporating real-world data, thereby strengthening its ability to detect and combat CSAM online.

![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/c5f9dbf2-d4e1-42e9-a4d5-03e802f754d3)
## DATA PREPROCESSING
Developed Scripts for feature extraction such as to extract geo-location of the URLs, Special characters, URL Type, server response time, number of subdomains, url length etc. Features were extracted mainly on the basis of URL Characteristics, such as length, redirection, non-standard protocols, link shortening services, link creation time, click lag difference, Domain Analysis such as Domain Reputation, Domain Age, Domain Registrar Country, Domain Creation Time, Content Analysis such as Linguistic Analysis, Metadata Analysis, Hosting Analysis such as Hosting Provider and Hosting Location.
Handling missing values: Null or missing values within a dataset can have a detrimental impact on the performance of a machine learning model. One effective approach taken to tackle these missing values was to replace with appropriate values. For categorical data, the mode strategy was employed (filling missing values with most frequently occurring value) while for numerical data mean method was used to fill out the missing values.
By handling missing values, it was ensured that the data has been prepared for further processing and model training result in more accurate predictions. 
Merging and consolidating of dataset for enhanced analysis, the dataset preprocessed was consolidated and merged with URLs having CSAM and benign along with features for enhanced analysis.
Categorical data encoding has been performed to convert categorical columns to numerical which are suitable for Machine Learning purpose. One hot encoding converts categorical columns to binary format. URLs present in dataset were effectively encoded using TFIDF Vectorizer which converted textual data into TF-IDF vectors.
## DATA VISUALIZATION
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/c0942d24-0512-480c-acfb-bdbebcd0341a)


Correlation heatmap and TF-IDF technique were employed to analyse the feature importance aligning with the URL classification. As per the map length, special characters, keywords contribute more towards url being CSAM /Benign.TF-IDF scores help identify the most relevant terms in a document by considering both their frequency within the document and their rarity across the entire document collection. They are often used for tasks such as document classification, information retrieval, and keyword extraction. For building robust results we have considered all features extracted and allowed ML model to retrieve results based on feature importance.
## VALIDATION TECHNIQUE UTILIZED
- Cross Validation
- Percentage Split Mechanism
- TF-IDF Vectorization
## RESULTS AND FINDINGS
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/c4cc8c18-d7d2-4b5a-b23e-f14f7e403b59)
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/1b5c6e00-85c4-48de-aecb-4f57765f6671)

•	Decision trees and ensemble methods RF demonstrate the highest accuracy and agreement for CSAM detection.
•	Bayesian methods offer competitive performance with lower computational cost.
•	SMO exhibit lower accuracy and agreement but may have other advantages.
•	Further model analysis and application development are made using trained Random Forest Classifier
 Plot showing accuracy comparison of different models
 
 ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/f3f9206e-faec-4a40-9e5f-d2a5086f0fca)
 ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/67c830ad-d6af-4d6d-8a52-bf190c11f446)
 
 ROC Curve and Confusion Matrix for best performing model Random Forest Classifier
 ROC Curve=1, RF model has achieved perfect discrimination between two classes.
 ## CONCLUSION
 The analysis of the CSAMGuard system’s performance using techniques like cross validation, percentage split, TF-IDF vectorization approaches with different Machine Learning models provided useful insights in drawing relevant conclusions.
High Effectiveness: The CSAMGuard system, employing the various approach with Random Forest model showed highest accuracy of 97% indicates strong ability to correctly classify instances.
Balanced Performance: The model exhibits a balanced performance, as reflected in high precision, recall, and F1-scores for both the ‘Benign’ and ‘CSAM’ classes. This suggests that the model is reliable in correctly identifying instances of both classes without trade-off between precision and recall.
Generalization: The model’s consistent accuracy across different evaluation methods such as percentage split and cross-validation, suggests good generalization to new and unseen data. This is a positive indicator of the model’s robustness.
Class-Specific Performance: The model performs well for both classes, achieving high precision and recall. The ability to identify ‘CSAM’ instances with 99% precision is particularly crucial for the system’s intended purpose.
## Integration of Machine Learning Model to Web Application!
Streamlit, a Python library, seamlessly converts machine learning models into interactive web applications.
User can input urls or upload bulk urls and check the prediction results

![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/40da785a-cb2a-4a39-8fad-b5e0ad7121ab)
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/4e754129-9704-477b-a4d4-96e988bc7658)
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/9c407fc6-d935-4c81-9f32-51bdd102e6a1)
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/2276be90-a1a2-40cd-899d-8e9694d8bde3)
## Tested model with various 10 top url shortener provider services
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/99457163-aa6b-45b6-8736-72c99ce6f4fe)
## CCIS API Validation
In this section, the practical application of the API developed are presented, outlining its design, key components, and the testing process.
API Design and Functionality: The API is structured to receive POST requests containing JSON data with a designated URL field. Subsequently, it utilizes a pre-trained machine learning model based on the Random Forest algorithm to classify the input, providing the prediction result in JSON format.
 ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/a6da7888-32e8-4053-91ac-b6decb98849b)

Key Components Used
•	Flask: A web application framework utilized for building the API.
•	Pandas: A data manipulation library for Python, aiding in data processing.
•	Pickle: Python's built-in module for object serialization and deserialization.
•	Requests: An HTTP library for Python, facilitating communication between the API and external entities.
Machine Learning Model: The machine learning model implemented within the API employs the Random Forest algorithm, which has undergone thorough training to achieve optimal accuracy. This model serves as the backbone for predicting the classification of URLs.
Testing Methodology: Extensive testing was conducted using Postman, a widely recognized API development tool. The objective was to ensure the correct functionality and reliability of the API under various scenarios. These scenarios encompassed both valid and invalid JSON requests to assess the API's robustness.
 ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/16ea3e38-48c5-4a23-9b74-c0300d07c332)

Postman Usage: To initiate testing, the URL to be evaluated was provided in JSON format within the Postman tool. Parameters were configured according to the specifications of the developed model. This comprehensive testing approach allowed for a meticulous examination of the API's responsiveness.
 ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/c956ead3-b8a4-4167-bcd0-df396eb5f4b3)
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/33ecb11e-6fd5-4645-bda3-07a4282fcae9)

 
Command Prompt Testing: Additionally, testing was performed through the command prompt using the curl tool. A POST request was made to a locally hosted server at http://127.0.0.1:5000/predict, demonstrating the API's functionality in a command-line environment.
 ![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/4c2201d6-b71e-4dc0-9fe9-c6a141478a25)

In summary, the local API has undergone rigorous testing using industry-standard tools and methodologies, ensuring its reliability, accuracy, and seamless integration into various environments. The incorporation of machine learning, coupled with a well-defined API structure, positions this solution as a robust and effective tool for URL classification.


## Future Research Considerations
- Intelligence Extraction from CSAM Content (CSAMGuard+)
Collaboration with organizations like the Internet Watch Foundation (IWF) and short link service providers to leverage their expertise and data reservoirs.
Implement advanced techniques to extract metadata from CSAM content, utilizing it as a pivotal feature for predictive models. Ethical data handling and adherence to privacy regulations remain paramount.
![image](https://github.com/nawalrabia/nawalportfolio.github.io/assets/120711618/92ca5fbf-a95e-460b-b1e4-a2f8084ae75f)

- Develop a comprehensive CSAM detection framework by Integrating existing solutions, including:
GATE-like systems to refine search criteria and streamline webpage retrieval.
- Sentiment analysis models to discern contextual cues.
Image forensic analysis for identifying illicit content using AI algorithm for image comparison and similarity detection.





















