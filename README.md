<<<<<<< HEAD
**Vehicle Classification Project**

__Project Overview__
This project was developed to classify three types of vehicles—bus, van, and car—using their silhouette features. The data used for the classification is based on geometric features extracted from the silhouette of vehicles viewed at different angles. The goal of the project was to apply both supervised and unsupervised learning techniques to classify the vehicles, comparing their performance.

__Problem Statement__
"Prospect Auto," a chain of car repair shops, asked us to build a model capable of classifying three types of vehicles based on their silhouette features. The dataset contains geometric measurements (e.g., compactness, circularity, skewness, etc.) extracted from the silhouettes of three vehicles:

A bus (double-decker)
A van (Chevrolet van)
A car (either Saab 9000 or Opel Manta)
The objective was to create a classification model that can reliably predict the type of vehicle given its silhouette features.

__Data Overview__
The dataset consists of the following features:

compactness
circularity
distance_circularity
radius_ratio
pr.axis_aspect_ratio
max.length_aspect_ratio
scatter_ratio
elongatedness
pr.axis_rectangularity
max.length_rectangularity
scaled_variance
scaled_variance.1
scaled_radius_of_gyration
scaled_radius_of_gyration.1
skewness_about
skewness_about.1
skewness_about.2
hollows_ratio
class (target variable: bus, van, car)
The dataset contains 846 rows and 19 columns, with 18 feature columns and a class column indicating the vehicle type.

__Approach & Methodology__
Step 1: Data Preprocessing
The first task was to clean the data:

Missing Data Handling: Missing values were handled by filling them with the mean of the respective column.
Standardization & Normalization: The features were scaled using StandardScaler to normalize the data, ensuring that all features had a mean of 0 and a standard deviation of 1.
__Step 2: Exploratory Data Analysis (EDA)__
A thorough exploratory data analysis was performed to understand the distribution of the data. Visualizations such as histograms, box plots, and correlation matrices were used to check for relationships between features and detect potential outliers.

__Step 3: Dimensionality Reduction (PCA)__
To reduce the complexity of the data, Principal Component Analysis (PCA) was applied to reduce the number of features from 18 to 6 while retaining a significant portion of the variance (96.9%). This helped in visualizing the data and also improved the performance of certain algorithms.

__Step 4: Supervised Learning (Random Forest Classifier)__
A Random Forest Classifier was trained using the preprocessed dataset. The data was split into training and test sets (70% train, 30% test). The model was evaluated using:

Accuracy: 97.24%
Confusion Matrix
Classification Report: Precision, recall, and F1-score for each vehicle class.
__Step 5: Unsupervised Learning (KMeans Clustering)__
In the unsupervised learning approach, KMeans clustering was applied on the scaled data to group the vehicles into clusters. PCA was used to reduce the data to 2D for visualization. The Adjusted Rand Index (ARI) was used to evaluate the clustering performance, resulting in an ARI of 0.07, indicating a poor match with the true vehicle classes.

__Step 6: Model Comparison__
The performance of both the supervised and unsupervised approaches was compared:

Supervised Approach: Provided high accuracy and reliable classification metrics.
Unsupervised Approach: Showed a lower ARI, as expected from unsupervised methods that do not have access to labeled data.
__Final Conclusion__
The supervised learning approach (Random Forest Classifier) significantly outperformed the unsupervised clustering method (KMeans) with an accuracy of 97.24%. The clustering approach, while useful for cases without labeled data, resulted in a much lower ARI due to the lack of label information.

In conclusion, the supervised approach proved to be the more effective method for this classification task, achieving better performance metrics and reliability.

__Repository Structure__
The project folder contains the following files:

vehicle_classification.ipynb: Jupyter notebook containing the entire workflow (data cleaning, analysis, model training, and evaluation).
vehicle.csv: The dataset containing vehicle silhouette features.
requirements.txt: A list of Python packages required to run the project.
venv/: Virtual environment folder.

=======
# machine-learning-vehicle-classification
This project classifies vehicles (bus, car, van) using machine learning. It applies both supervised (Random Forest) and unsupervised (KMeans clustering) approaches. Key steps include data preprocessing, feature scaling, dimensionality reduction (PCA), and evaluating performance with metrics like accuracy and ARI.
>>>>>>> ebc6094de9235c30f116f33106b9ea038ef12921
