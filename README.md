# COVID-19-EDA-ML
Explanatory Data Analysis and Machine Learning project about Covid-19 data released by Mexican Government

<img src="https://ec.europa.eu/eurostat/documents/10760954/10762597/COVID_overview_image.jpg/" />



<div align="justify">
<p>
Coronavirus disease (<strong>COVID-19</strong>) is an infectious disease caused by a newly discovered coronavirus. Most people infected with COVID-19 virus will experience mild to moderate respiratory illness and recover without requiring special treatment. Older people, and those with underlying medical problems like cardiovascular disease, diabetes, chronic respiratory disease, and cancer are more likely to develop serious illness.
</p>
<p>
During the entire course of the pandemic, one of the main problems that healthcare providers have faced is the shortage of medical resources and a proper plan to efficiently distribute them. In these tough times, being able to predict what kind of resource an individual might require at the time of being tested positive or even before that will be of immense help to the authorities as they would be able to procure and arrange for the resources necessary to save the life of that patient.
</p>
<p>
The main goal of this project is to build a machine learning model that, given a Covid-19 patient's current symptom, status, and medical history, will predict whether the patient is in <strong>high risk</strong> or not.
</p>
</div>
<div align="justify">
<p>
The dataset was provided by the Mexican government (<a href="https://datos.gob.mx/busca/dataset/informacion-referente-a-casos-covid-19-en-mexico" target="_blank">link</a>). This <a href="https://www.kaggle.com/datasets/meirnizri/covid19-dataset" target="_blank">dataset</a> contains an enormous number of anonymized patient-related information including pre-conditions. The raw dataset consists of 21 unique features and 1,048,576 unique patients. In the Boolean features, 1 means "yes" and 2 means "no". values as 97 and 99 are missing data.
</p>
<br><br>
<ul>
  <li><strong>sex</strong>: 1 for female and 2 for male.</li>
  <li><strong>age</strong>: of the patient.</li>
  <li><strong>classification</strong>: covid test findings. Values 1-3 mean that the patient was diagnosed with covid in different degrees. 4 or higher means that the patient is not a carrier of covid or that the test is inconclusive.</li>
  <li><strong>patient type</strong>: type of care the patient received in the unit. 1 for returned home and 2 for hospitalization.</li>
  <li><strong>pneumonia</strong>: whether the patient already have air sacs inflammation or not.</li>
  <li><strong>pregnancy</strong>: whether the patient is pregnant or not.</li>
  <li><strong>diabetes</strong>: whether the patient has diabetes or not.</li>
  <li><strong>copd</strong>: Indicates whether the patient has Chronic obstructive pulmonary disease or not.</li>
  <li><strong>asthma</strong>: whether the patient has asthma or not.</li>
  <li><strong>inmsupr</strong>: whether the patient is immunosuppressed or not.</li>
  <li><strong>hypertension</strong>: whether the patient has hypertension or not.</li>
  <li><strong>cardiovascular</strong>: whether the patient has heart or blood vessels related disease.</li>
  <li><strong>renal chronic</strong>: whether the patient has chronic renal disease or not.</li>
  <li><strong>other disease</strong>: whether the patient has other disease or not.</li>
  <li><strong>obesity</strong>: whether the patient is obese or not.</li>
  <li><strong>tobacco</strong>: whether the patient is a tobacco user.</li>
  <li><strong>usmr</strong>: Indicates whether the patient treated medical units of the first, second or third level.</li>
  <li><strong>medical unit</strong>: type of institution of the National Health System that provided the care.</li>
  <li><strong>intubed</strong>: whether the patient was connected to the ventilator.</li>
  <li><strong>icu</strong>: Indicates whether the patient had been admitted to an Intensive Care Unit.</li>
  <li><strong>date died</strong>: If the patient died indicate the date of death, and 9999-99-99 otherwise.</li>    
    
</ul>
</div>

----

<html>
<body>
  <h1>Explanatory Data Analysis (EDA)</h1>
  <p>Explanatory Data Analysis (EDA) is an important step in any data science project. It involves exploring and analyzing the data to better understand its properties and characteristics.</p>
  <h2>Why is EDA important?</h2>
  <ul>
    <li>Identifying patterns and trends: EDA helps you identify patterns and trends in the data that can give you insights into the relationships between different variables. This can help you build better models and make more accurate predictions.</li>
    <li>Detecting anomalies and outliers: EDA can help you detect anomalies and outliers in the data, which can indicate errors or potential problems. By identifying and addressing these issues, you can improve the quality and reliability of your analysis.</li>
    <li>Data cleaning and preparation: EDA helps you identify missing or incorrect values in the data, and gives you the opportunity to clean and prepare the data for further analysis.</li>
    <li>Communicating results: EDA can help you generate plots and visualizations that effectively communicate your results to others. These visualizations can be an important part of presenting your findings to stakeholders or decision-makers.</li>
  </ul>
  <p>Overall, EDA is an essential step in any data science project, as it helps you understand the characteristics and patterns in your data, identify potential issues, and prepare the data for further analysis.</p>
</body>
</html>

----

<html>
<body>
    <div align="justify">
  <h1>Correlation Matrix</h1>
    <br>
A correlation matrix is a table or matrix that shows the statistical relationship between a set of variables. It is a useful tool for understanding the relationships between variables and for identifying patterns in data.
    <br><br>
  <h2>Why is Correlation Matrix important?</h2>
        <br>
In a correlation matrix, each variable is listed on both the rows and columns of the table, and the cells of the table show the correlation between the variables. A correlation coefficient (a value between -1 and 1) is used to indicate the strength and direction of the relationship between the variables. A coefficient of 1 indicates a strong positive correlation, a coefficient of -1 indicates a strong negative correlation, and a coefficient of 0 indicates no correlation.<br><br>
Correlation matrices are used in a variety of fields, including statistics, finance, and psychology, to help understand and analyze data. They can be particularly useful in identifying relationships between variables that may not be immediately obvious and in identifying patterns in data that may be useful in predicting future outcomes.<br><br>
Overall, correlation matrices are an important tool for understanding and analyzing data and for identifying patterns and relationships in data.
        </div>
</body>
</html>

----

<html>
<body>
    <div align="justify">
  <h1>The baseline model</h1>
    <br>
A baseline model is a model that is used as a reference point against which other models can be compared. It is a simple model that is built using minimal effort and resources, and it is used as a benchmark to see how much improvement can be achieved through more advanced modeling techniques.
    <br><br>
  <h2>Why is the baseline model important?</h2>
        <br>
Baseline models are often used in machine learning and other areas to establish a baseline performance for a given problem. For example, in a classification problem, a baseline model might be a simple model that always predicts the most common class. This model would serve as a baseline, and any other model that performs better than this baseline model would be considered an improvement.<br><br>
Baseline models can be useful for identifying the minimum performance that is acceptable for a given problem and for identifying areas where more advanced modeling techniques may be needed. They can also help to establish a baseline performance that can be used to compare the performance of different models and evaluate which model is the most effective.<br><br>
        
  <h2>Binary classification</h2>
        <br>
Binary classification is a type of classification in which there are only two classes. For example, a binary classification problem might involve predicting whether a patient has a disease or not, or whether an email is spam or not spam.<br><br>
In the context of predicting the <strong>survival</strong> of people who had covid, binary classification could be used to predict whether a person with covid will survive or not survive. The model would be trained on a dataset of people who had covid and the outcome (survival or not), and it would use features such as age, gender, underlying health conditions, and other relevant factors to make predictions.<br><br>
      
  <h2>Split data into training/test</h2>
        <br>
<strong>train_test_split</strong> is a function in scikit-learn that can be used to split a dataset into two subsets: a training set and a test set. The training set is used to train a machine learning model, while the test set is used to evaluate the performance of the model.<br><br>
The reason why it is important to use train_test_split is that it helps to avoid overfitting. Overfitting occurs when a model is trained too well on the training data and performs poorly on new, unseen data. By splitting the data into a training set and a test set, we can ensure that the model is not overfitting by evaluating its performance on the test set, which is unseen during the training process.<br><br>
        
</div>
</body>
</html>

-------

<html>
<body>
    <div align="justify">
  <h1>The model evaluation</h1>
    <br>
Model evaluation is an important step in the machine learning process, especially in the context of binary classification. Binary classification involves predicting one of two classes, and it is commonly used in a variety of applications, such as predicting whether a patient has a disease or not, or whether an email is spam or not spam. When evaluating the performance of a binary classifier, several metrics can be used to measure how well the model is able to predict the two classes.
    <br><br>
  <h2>Accuracy</h2>
        <br>
Accuracy is the most basic and intuitive metric for evaluating the performance of a binary classifier. It is defined as the number of correct predictions made by the model divided by the total number of predictions. For example, if a model makes 100 predictions and 75 of them are correct, the accuracy of the model is 75%.<br><br>
<p style="text-align: center;">Accuracy = $\frac{\text{number of correct predictions}}{\text{total number of predictions}} = \frac{TP+TN}{TP+TN+FP+FN}$</p>
        
  <h2>Precision</h2>
        <br>
Precision is a metric that measures the proportion of true positive predictions made by the model. In other words, it is the number of true positive predictions made by the model divided by the total number of positive predictions made by the model. Precision is often used as a metric in imbalanced classification problems, where one class is more common than the other. For example, in a problem where the negative class is much more common than the positive class, a model with high precision would be able to correctly identify the positive class most of the time, even if it also wrongly identifies some negative instances as positive.<br><br>
<p style="text-align: center;">Precision = $\frac{TP}{TP+FP}$</p>
        
  <h2>Recall</h2>
        <br>
Recall is a metric that measures the proportion of true positive predictions made by the model compared to the total number of positive instances in the data. It is defined as the number of true positive predictions made by the model divided by the total number of positive instances in the data. Recall is often used as a metric in imbalanced classification problems, where it is important to identify as many instances of the minority class as possible. For example, in a problem where the negative class is much more common than the positive class, a model with high recall would be able to identify most of the positive instances in the data, even if it also wrongly identifies some negative instances as positive.<br><br> 
<p style="text-align: center;">Recall = $\frac{TP}{TP+FN}$</p>
        
  <h2>F1 Score</h2>
        <br>
The F1 score is a metric that combines precision and recall into a single score. It is defined as the harmonic mean of precision and recall, and is calculated as follows:<br><br>
<p style="text-align: center;">F1 Score = $\frac{2\times\text{Precision}\times\text{Recall}}{\text{Precision}+\text{Recall}} = \frac{2\times TP}{2\times TP+FP+FN}$</p><br><br>
The F1 score is a useful metric for evaluating the performance of a binary classifier, especially in imbalanced classification problems. It takes into account both the precision and recall of the model, and is more sensitive to changes in either of these metrics than either metric alone. A model with a high F1 score is able to make both accurate and precise predictions, and is generally considered to be a good model.<br><br>     
      
</div>
</body>
</html>


--------


<html>
<body>
    <div align="justify">
<h2>The Confusion Matrix</h2>
        <br>
A confusion matrix is a table that is often used to describe the performance of a classification algorithm, particularly in binary classification problems. A confusion matrix will have four entries, corresponding to the number of true positives, true negatives, false positives, and false negatives. These four entries will have the following meanings:<br><br>

<li><strong>True positives (TP)</strong>: The number of instances that are positive (i.e., belong to the positive class) and are correctly classified as positive.</li>
<li><strong>True negatives (TN)</strong>: The number of instances that are negative (i.e., belong to the negative class) and are correctly classified as negative.</li><li><strong>False positives (FP)</strong>: The number of instances that are negative but are incorrectly classified as positive. Also known as Type I error or false alarm.</li><li><strong>False negatives (FN)</strong>: The number of instances that are positive but are incorrectly classified as negative. Also known as Type II error or miss.</li><br>
The confusion matrix is important because it gives you an idea of how well your classification algorithm is performing. You can use the entries in the matrix to compute various performance metrics, such as accuracy, precision, recall, and F1-score.<br><br> 
Additionally, the confusion matrix is also useful for identifying which types of mistakes the model is making and where it needs improvement. For example, if your model has a high number of false negatives, it means that it's missing a lot of positive examples, whereas a high number of false positives indicates that it's flagging too many negative examples as positive. By understanding the patterns in the confusion matrix, you can adjust your model's settings or feature engineering to improve its performance.<br><br>
In summary, the confusion matrix is a powerful tool for evaluating the performance of a binary classifier, as it allows you to compute a variety of performance metrics, which are important to understand the performance of a model and help in identifying the areas of improvement.<br><br>

</div>
</body>
</html>

--------



