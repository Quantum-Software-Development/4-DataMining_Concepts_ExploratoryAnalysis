
<br>

**\[[🇧🇷 Português](README.pt_BR.md)\] \[**[🇺🇸 English](README.md)**\]**


<br><br>

# 4- [Data Mining]()  / [Concepts and Exploratory Analysis]()



<!-- ======================================= Start DEFAULT HEADER ===========================================  -->

<br><br>


[**Institution:**]() Pontifical Catholic University of São Paulo (PUC-SP)  
[**School:**]() Faculty of Interdisciplinary Studies  
[**Program:**]() Humanistic AI and Data Science
[**Semester:**]() 2nd Semester 2025  
Professor:  [***Professor Doctor in Mathematics Daniel Rodrigues da Silva***](https://www.linkedin.com/in/daniel-rodrigues-048654a5/)

<br><br>

#### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)


<br><br>

<!--Confidentiality statement -->

#

<br><br><br>

> [!IMPORTANT]
> 
> ⚠️ Heads Up
>
> * Projects and deliverables may be made [publicly available]() whenever possible.
> * The course emphasizes [**practical, hands-on experience**]() with real datasets to simulate professional consulting scenarios in the fields of **Data Analysis and Data Mining** for partner organizations and institutions affiliated with the university.
> * All activities comply with the [**academic and ethical guidelines of PUC-SP**]().
> * Any content not authorized for public disclosure will remain [**confidential**]() and securely stored in [private repositories]().  
>


<br><br>

#

<!--END-->




<br><br><br><br>



<!-- PUC HEADER GIF
<p align="center">
  <img src="https://github.com/user-attachments/assets/0d6324da-9468-455e-b8d1-2cce8bb63b06" />
-->


<!-- video presentation -->


##### 🎶 Prelude Suite no.1 (J. S. Bach) - [Sound Design Remix]()

https://github.com/user-attachments/assets/4ccd316b-74a1-4bae-9bc7-1c705be80498

####  📺 For better resolution, watch the video on [YouTube.](https://youtu.be/_ytC6S4oDbM)


<br><br>


> [!TIP]
> 
>  This repository is a review of the Statistics course from the undergraduate program Humanities, AI and Data Science at PUC-SP.
>
> Access Data Mining [Main Repository](https://github.com/Quantum-Software-Development/1-Main_DataMining_Repository)
> 
>  If you’d like to explore the full materials from the 1st year (not only the review), you can visit the complete repository [here](https://github.com/FabianaCampanari/PracticalStats-PUCSP-2024).
>
>



<!-- =======================================END DEFAULT HEADER ===========================================  -->





# Table of Contents

- [Project Overview](#project-overview)
- [AI Project Workflow](#ai-project-workflow)
- [Installation and Requirements](#installation-and-requirements)
- [Usage Examples](#usage-examples)
- [Knowledge Discovery in Databases (KDD)](#knowledge-discovery-in-databases-kdd)
- [Mathematical Concepts](#mathematical-concepts)
- [Discrete vs Continuous Values](#discrete-vs-continuous-values)
- [Primary Libraries and Tools](#primary-libraries-and-tools)
- [Supervised vs Unsupervised Learning](#supervised-vs-unsupervised-learning)
- [Clustering and Distance Calculations](#clustering-and-distance-calculations)
- [Credit Analysis: Classification Example](#credit-analysis-classification-example)
- [Fruit Clustering Example](#fruit-clustering-example)
- [Anomaly Detection and Association Rules](#anomaly-detection-and-association-rules)
- [Applications](#applications)
- [Repository Structure and Documentation](#repository-structure-and-documentation)
- [Contributing and License](#contributing-and-license)
- [References](#references)


<br>


## [Project Overview]()

This project provides a comprehensive introduction to **Data Mining and AI**, based on the workbook from PUC-SP by Prof. Dr. Daniel Rodrigues da Silva. It covers:

- Foundations of data mining and KDD
- Relation between data, information, and knowledge concepts
- Mathematical foundations (inflection points, maxima, minima)
- Overview of supervised and unsupervised learning
- Practical coding examples in Python and R
- Real-world cases such as credit classification, fruit clustering, anomaly detection, and industrial applications


<br><br>

## [AI/ML Project Workflow]()

<br>

Machine learning project development follows an iterative, structured process:

<br>


```
+-----------------+      +---------------------+      +----------------------+
|   Dataset/Data  | ---> |   Preprocessing     | ---> |   Cluster Training   |
+-----------------+      +---------------------+      +----------------------+
                                |                          |
                                v                          v
                      +---------------------+      +----------------------+
                      |  Cleaned/Labeled    |      |   Parallel Training  |
                      |      Data           |      +----------------------+
                      +---------------------+                |
                                        |                    v
                                        v          +----------------------+
                                  +---------------------+ | Validation &   |
                                  |     Validation      | |   Tuning       |
                                  +---------------------+ +----------------+
                                        |
                                        v
                               +---------------------+
                               |   Trained Model     |
                               +---------------------+
                                        |
                                        v
                             +------------------------+
                             | Inference in Production|
                             +------------------------+
                                        |
                                        v
                             +------------------------+
                             | Feedback (New Data)    |
                             +------------------------+
```


<br><br>


## [Detailed AI Project Workflow Explanation]()

<br>

1. [**Data Collection (Dataset)**]()
Everything starts with collecting the dataset used for training.
*Example:* 1 million images for a facial recognition model.

<br>

2. [**Preprocessing**]()
Clean, standardize, and organize data.
*Example:* Resize images, remove noise, label properly. Simple machines or servers suffice.

<br>

3. [**Sending to the Cluster**]()
Data is sent to clusters (dozens or hundreds of GPUs/CPUs) for parallel processing.
*Example:* Upload to AWS, Google Cloud, or private clusters.

<br>

4. [**Training on the Cluster**]()
Workload is split across multiple machines for faster training.
*Example:* GPUs process parts of batches; results combined for final model.

<br>

5. [**Validation and Tuning**]()
Test on validation subset to check accuracy; tune hyperparameters until objectives met.

<br>

6. [**Inference in Production**]()
Deploy trained model on servers/clusters for real-time predictions.
*Example:* User uploads photo; model recognizes face in seconds.

<br>

7. [**Feedback and Update**]()
Collect new data to retrain and improve the model continually.
*Example:* User data expands dataset for next training cycle.


<br><br>


## Installation and Requirements

### [Python Setup]()

```python
pip install pandas numpy scikit-learn seaborn
```

<br>

### Include `requirements.txt` for ease:

<br>

```python
pandas
numpy
scikit-learn
seaborn
```

<br>


### R Setup

```R
install.packages(c("tidyverse", "caret", "cluster"))
```

<br><br>

## [Usage Examples]()

### [Python]() Clustering Example

<br>

```python
import pandas as pd
from sklearn.cluster import KMeans

data = pd.DataFrame({'shape': [5, 4, 1, 2], 'color': [7, 8, 2, 1]})
kmeans = KMeans(n_clusters=2, random_state=0).fit(data)
data['cluster'] = kmeans.labels_
print(data)
```

<br>

### [Python]() Classification Example

```python
from sklearn.linear_model import LogisticRegression
import pandas as pd

df = pd.DataFrame({
    'income': [2300, 4000, 1200, 6000],
    'score': [600, 700, 550, 800],
    'approved': [0, 1, 0, 1]
})
X = df[['income', 'score']]
y = df['approved']
model = LogisticRegression().fit(X, y)
print(model.predict([[3000, 650]]))
```

<br>

### [R]() Clustering Example

```R
fruit <- data.frame(shape=c(5,4,1,2), color=c(7,8,2,1))
km <- kmeans(fruit, centers=2)
print(km$cluster)
```

<br>

### [R]() Classification Example

```R
data <- data.frame(income=c(2300,4000,1200,6000), score=c(600,700,550,800), approved=c(0,1,0,1))
model <- glm(approved ~ income + score, data, family=binomial)
predict(model, newdata=data.frame(income=3000, score=650), type="response")
```


<br><br>


##[ Knowledge Discovery in Databases (KDD)]()

KDD spans data selection, preprocessing, mining, and validation steps ensuring extracted knowledge is meaningful and valuable.







































<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>
<br><br><br><br>


<!-- ========================== [Bibliographr ====================  -->

<br><br>


## [Bibliography]()


[1](). **Castro, L. N. & Ferrari, D. G.** (2016). *Introdução à mineração de dados: conceitos básicos, algoritmos e aplicações*. Saraiva.

[2](). **Ferreira, A. C. P. L. et al.** (2024). *Inteligência Artificial - Uma Abordagem de Aprendizado de Máquina*. 2nd Ed. LTC.

[3](). **Larson & Farber** (2015). *Estatística Aplicada*. Pearson.


<br><br>


<!-- ======================================= Start Footer ===========================================  -->


<br><br>


## 💌 [Let the data flow... Ping Me !](mailto:fabicampanari@proton.me)

<br><br>



#### <p align="center">  🛸๋ My Contacts [Hub](https://linktr.ee/fabianacampanari)


<br>

### <p align="center"> <img src="https://github.com/user-attachments/assets/517fc573-7607-4c5d-82a7-38383cc0537d" />




<br><br><br>

<p align="center">  ────────────── 🔭⋆ ──────────────


<p align="center"> ➣➢➤ <a href="#top">Back to Top </a>

<!--
<p align="center">  ────────────── ✦ ──────────────
-->



<!-- Programmers and artists are the only professionals whose hobby is their profession."

" I love people who are committed to transforming the world "

" I'm big fan of those who are making waves in the world! "

##### <p align="center">( Rafael Lain ) </p>   -->

#

###### <p align="center"> Copyright 2025 Quantum Software Development. Code released under the [MIT License license.](https://github.com/Quantum-Software-Development/Math/blob/3bf8270ca09d3848f2bf22f9ac89368e52a2fb66/LICENSE)










