# COVID-19-EDA-ML
Explanatory Data Analysis and Machine Learning project about Covid-19 data released by Mexican Government


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



