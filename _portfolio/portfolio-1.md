---
title: "Credit Risk Scoring: A Stacking Generalization Approach"
excerpt: "Model Combination Approach to Credit Scoring<br/><img src='/images/CreditCard.png'>"
collection: portfolio
---

Presented in World CIST Conference, 2023

**Paper Overview**
---
<div style="text-align: justify;">
<p>This study delves into the critical role of credit markets in financial crises and subsequent regulatory changes, highlighting the significance of credit scoring in loan assessment. It traces the evolution of credit scoring techniques from traditional methods to contemporary machine learning approaches and introduces ensemble-based modelling, particularly stacking generalization.</p>
</div>
<div style="text-align: justify;">
<p>Conducted on a publicly available bank loan dataset, the empirical study focuses on banking loan default. Through ensemble-based techniques, specifically stacking generalization, the research aims to enhance model robustness and predictive power. The findings underscore the effectiveness of combining diverse models, offering substantial flexibility to credit scoring frameworks.</p>
</div>
<div style="text-align: justify;">
<p>Representing the culmination of the author's master's thesis in statistics and information management, this research contributes empirical insights and methodological advancements to the field.</p>
</div>

**Introduction**
----
<div style="text-align: justify;">
<p>Credit risk regulation has received tremendous attention, especially in the aftermath of the latest global financial crisis. Under the Basel guidelines and the Internal Rating Based approach, banks are permitted to use internal risk measures as key drivers to assess the viability of granting a loan to an applicant. Credit scoring, a statistical approach used for evaluating potential loan applications in financial and banking institutions, plays a crucial role in this process. When applying for a loan, an applicant must provide details such as income, marital status, and loan purpose, which contribute to a credit scoring model. This model produces a score used to determine the appropriateness of granting a loan, thereby enabling faster and more consistent credit approvals and reducing bad debt. Traditionally, machine learning and statistical approaches like logistic regression and tree-based algorithms have been employed individually for credit scoring models. However, newer contemporary machine learning techniques, which combine multiple models, can outperform these classic methods.</p>
</div>
<div style="text-align: justify;">
<p>The most well known ensemble based approaches bagging and boosting, who use homogeneuons based learners, have been widely used in the credit risk literatture. The novel approach of this study is to apply stacking, who considers heterogeneuos learners, in credit scoring. The architecture of a stacking ensemble involves two or more base models, often referred to as level-0 models with different weight combinations, and a meta-model that combines the predictions of these level-0 models to make a complete final prediction The proposed ensemble method, based on stacking generalization, extends various preceding studies that used different techniques to improve model predictive capabilities. Bellow we present a general structure of a stacked based ensemble:</p>
</div>

<div style="text-align: center;">
    <img src="/images/stacking.png" alt="Stacked Ensemble Model Structure">
    <br><br>
</div>

<div style="text-align: justify;">

<p>In conclusion, the adoption of stacking generalization, an ensemble method employing heterogeneous learners, represents a novel approach in credit scoring. By combining diverse base models and leveraging their predictions through a meta-model, this study aims to advance model predictive capabilities beyond traditional methods like bagging and boosting.</p>
</div>


**Key Findings**
---
<div style="text-align: justify;">

1) **Dataset Overview and Preprocessing and Initial Evaluation:**

<p>The study utilized a comprehensive dataset containing 2.26 million rows and 151 features. Appropriate exploratory data analysis (EDA) and feature engineering techniques were applied to ensure the data's suitability for modeling. In addition to these preparatory steps, k-fold cross-validation and hyperparameter tuning were employed to further enhance the predictive capabilities of individual models. Below, we present the results from these individual models:</p>
</div>

<table style="width:100%; border-collapse: collapse; border: 1px solid black;">
    <tr>
        <th style="border: 2px solid black;">Model</th>
        <th style="border: 2px solid black;">Accuracy</th>
        <th style="border: 2px solid black;">Precision</th>
        <th style="border: 2px solid black;">Recall</th>
        <th style="border: 2px solid black;">F1-score</th>
        <th style="border: 2px solid black;">AUC Score</th>
    </tr>
    <tr>
        <td style="border: 2px solid black;">LR</td>
        <td style="border: 2px solid black;">0.7489</td>
        <td style="border: 2px solid black;">0.4276</td>
        <td style="border: 2px solid black;">0.7607</td>
        <td style="border: 2px solid black;">0.5474</td>
        <td style="border: 2px solid black;">0.8329</td>
    </tr>
    <tr>
        <td style="border: 2px solid black;">SVM</td>
        <td style="border: 2px solid black;">0.7454</td>
        <td style="border: 2px solid black;">0.4238</td>
        <td style="border: 2px solid black;">0.7667</td>
        <td style="border: 2px solid black;">0.5459</td>
        <td style="border: 2px solid black;">0.7564</td>
    </tr>
    <tr>
        <td style="border: 2px solid black;">KNN</td>
        <td style="border: 2px solid black;">0.8396</td>
        <td style="border: 2px solid black;">0.6372</td>
        <td style="border: 2px solid black;">0.4566</td>
        <td style="border: 2px solid black;">0.5320</td>
        <td style="border: 2px solid black;">0.8453</td>
    </tr>
    <tr>
        <td style="border: 2px solid black;">DT</td>
        <td style="border: 2px solid black;">0.9258</td>
        <td style="border: 2px solid black;">0.7492</td>
        <td style="border: 2px solid black;">0.9433</td>
        <td style="border: 2px solid black;">0.8351</td>
        <td style="border: 2px solid black;">0.9764</td>
    </tr>
</table>

2) **Application of Sampling Techniques**
<div style="text-align: justify;">
<p>The dataset was found to be highly imbalanced. To address this issue, a strategy that combines both undersampling and oversampling was implemented to reduce the risk of overfitting. We present the results of each individual model considering this strategy.</p>
</div>

<table style="width:100%; border-collapse: collapse; border: 1px solid black;">
    <tr>
        <th style="border: 2px solid black;">Model</th>
        <th style="border: 2px solid black;">Accuracy</th>
        <th style="border: 2px solid black;">Precision</th>
        <th style="border: 2px solid black;">Recall</th>
        <th style="border: 2px solid black;">F1-score</th>
        <th style="border: 2px solid black;">AUC Score</th>
    </tr>
    <tr>
        <td style="border: 2px solid black;">LR</td>
        <td style="border: 2px solid black;">0.7489</td>
        <td style="border: 2px solid black;">0.4276</td>
        <td style="border: 2px solid black;">0.7607</td>
        <td style="border: 2px solid black;">0.5474</td>
        <td style="border: 2px solid black;">0.8329</td>
    </tr>
    <tr>
        <td style="border: 2px solid black;">SVM</td>
        <td style="border: 2px solid black;">0.7454</td>
        <td style="border: 2px solid black;">0.4238</td>
        <td style="border: 2px solid black;">0.7667</td>
        <td style="border: 2px solid black;">0.5459</td>
        <td style="border: 2px solid black;">0.7564</td>
    </tr>
    <tr>
        <td style="border: 2px solid black;">KNN</td>
        <td style="border: 2px solid black;">0.8396</td>
        <td style="border: 2px solid black;">0.6372</td>
        <td style="border: 2px solid black;">0.4566</td>
        <td style="border: 2px solid black;">0.5320</td>
        <td style="border: 2px solid black;">0.8453</td>
    </tr>
    <tr>
        <td style="border: 2px solid black;">DT</td>
        <td style="border: 2px solid black;">0.9258</td>
        <td style="border: 2px solid black;">0.7492</td>
        <td style="border: 2px solid black;">0.9433</td>
        <td style="border: 2px solid black;">0.8351</td>
        <td style="border: 2px solid black;">0.9764</td>
    </tr>
</table>

























It's noteworthy that the Decision Tree Model showed minimal improvement from this sampling strategy, highlighting its robustness and the importance of proper tuning.










**Notebooks**
---
* [Exploratory Data Analysis](https://github.com/BernardoRaimundo/Credit-Risk-Stacking-Ensemble/blob/main/Python%20Code%20For%20Deployment/1.%20Lending%20Club%20(EDA).ipynb).
* [Feature Engineering + Logistic Regression](https://github.com/BernardoRaimundo/Credit-Risk-Stacking-Ensemble/blob/main/Python%20Code%20For%20Deployment/2.%20Lending%20Club%20(Feature%20Engineering%20%2B%20LR).ipynb).
* [Feature Engineering + Decision Tree](https://github.com/BernardoRaimundo/Credit-Risk-Stacking-Ensemble/blob/main/Python%20Code%20For%20Deployment/3.%20Lending%20Club%20(Feature%20Engineering%20%2B%20DT).ipynb).
* [Feature Engineering + Support Vector Machine](https://github.com/BernardoRaimundo/Credit-Risk-Stacking-Ensemble/blob/main/Python%20Code%20For%20Deployment/4.%20Lending%20Club%20(Feature%20Engineering%20%2B%20SVM).ipynb)
* [Feature Engineering + K Nearest Neighbors](https://github.com/BernardoRaimundo/Credit-Risk-Stacking-Ensemble/blob/main/Python%20Code%20For%20Deployment/5.%20Lending%20Club%20(Feature%20Engineering%20%2B%20KNN).ipynb)
* [Final Model Combination](https://github.com/BernardoRaimundo/Credit-Risk-Stacking-Ensemble/blob/main/Python%20Code%20For%20Deployment/6.%20Lending%20Club%20(Stacking).ipynb)



**Publication:** Raimundo, B., Bravo, J.M. (2024). Credit Risk Scoring: A Stacking Generalization Approach. In: Rocha, A., Adeli, H., Dzemyda, G., Moreira, F., Colla, V. (eds) Information Systems and Technologies. WorldCIST 2023. Lecture Notes in Networks and Systems, vol 799. Springer, Cham. Available [here](https://doi.org/10.1007/978-3-031-45642-8_38)