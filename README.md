# Empirical Validation of Size Effects in Sub-sized Tensile Specimens for Nuclear Structural Materials

[![Scientific Reports](https://img.shields.io/badge/Scientific_Reports-DOI%3A_10.1038%2Fs41598--024--61189--x-brightgreen.svg)](https://doi.org/10.1038/s41598-025-98849-5)  

Authors: Longze Li, John W. Merickel, Yalei Tang, Rongjie Song, Joshua E. Rittenhouse, Aleksandar Vakanski, Fei Xu

Advancing the understanding of material behavior and phenomena related to size effects in small-scale components is critical for settings where limited quantities of material samples can be tested. Established guidelines for sub-sized specimen testing encompass best practices for specimen preparation, testing equipment, test procedures, and data analysis methods. However, prior investigations of specimen size effects in the literature typically involved a relatively small number of tests performed and analyzed. To address this limitation, our team created a large database of tensile test records for nuclear structural materials collected from peer-reviewed articles. 

In this study, we introduce a machine learning-based approach for predicting key tensile properties such as yield strength, ultimate tensile strength, and elongation for sub-sized specimens of Stainless Steel 316, and we develop methods for uncertainty quantification of predicted properties. Furthermore, we conduct an experimental validation of the reported critical values for the dimensions and geometry of sub-sized specimens, and we validated existing analytical models for correlating total elongation between sub-sized and standard-sized specimens. Our findings demonstrate the potential of machine learning techniques to enhance understanding of specimen size-dependent material behavior and highlight the need for coordinated efforts in developing large, open-source databases of mechanical testing data to support future research.

## 📂 Repository Organization
- [**Figures**](Figures/): This directory contains code for reproducing the figures in the article. The article includes 21 figures, and the notebook titles in this directory correspond to the respective figure numbers. <br>
- [**Tables**](Tables/): This directory contains code related to the results presented in Tables 3 to 6 of the article. The notebook titles correspond to those specific tables. <br>

## 📊 Data
 - [**Tensile Properties Dataset**](Tensile_Properties_Data.xlsx): The used dataset in this study is based on the dataset of tensile properties created by our team ([link1](https://www.nature.com/articles/s41597-024-04329-2), [link2](https://doi.org/10.24435/materialscloud:ws-8j)), comprising 1,050 tensile test records of sub-sized Stainless Steel 316 specimens collected from the published literature. Each record includes 55 features covering material type, specimen geometry, heat treatment, testing conditions, and measured mechanical properties. In this work, we expanded the dataset by adding tensile test records for full-sized Stainless Steel 316 specimens, bringing the total number to 1,473 records.

## 🧠 Machine Learning Methods
We developed machine learning models to predict tensile properties of Stainless Steel 316 specimens, including yield strength, ultimate tensile strength, uniform elongation, and total elongation. In addition to single-point predictions, we implemented uncertainty-aware models to estimate confidence intervals, enabling a more robust understanding of prediction reliability. The following table summarizes the model types and specific algorithms used in this study.

| Model Type                 | Task                                | Models Used                                                                 |
|---------------------------|-------------------------------------|------------------------------------------------------------------------------|
| Property prediction       | Single-point estimates             | k-Nearest Neighbors (kNN), Support Vector Machine (SVM), Decision Trees, Random Forest, Extreme Gradient Boosting (XGBoost), Gaussian Process Regression (GPR), Artificial Neural Networks (ANN) |
| Uncertainty quantification| Confidence interval predictions  | Quantile Regression, Natural Gradient Boosting (NGBoost), Gaussian Process Regression (GPR), Deep Ensemble, Monte Carlo Dropout (MC Dropout), Bayesian Neural Networks - Variational Inference, Bayesian Neural Networks - Markov Chain Monte Carlo |


## 🔨 Requirements

keras  2.6.0  
tensorflow 2.6.0  
pyro-ppl 1.8.5  
torchbnn 1.2  
torch 2.0.1  
pandas 1.5.3  
numpy 1.23.5  
scikit-learn 1.2.2  

## ▶️ Use
The codes are provided as Jupyter Notebook files. To reproduce the results, run the .ipynb files. 

## 📜 Citation

If you use the codes or the methods in your work, please cite the following <a href="https://doi.org/10.1038/s41598-025-98849-5">article</a>:   

    @article{li2025,
      TITLE= {Empirical validation of size effects in sub-sized tensile specimens for nuclear structural materials},
      AUTHOR= {Li, Longze and Merickel, John W. and Tang, Yalei and Song, Rongjie and Rittenhouse, Joshua E. and Vakanski, Aleksandar and Xu, Fei},
      JOURNAL = {Scientific Reports},
      YEAR = {2025},
      VOLUME = {15},
      ISSUE = {1},
      ARTICLE-NUMBER = {13846},
      URL = {https://doi.org/10.1038/s41598-025-98849-5},
      ISSN = {2045-2322},
      DOI = {10.1038/s41598-025-98849-5}}


## 🚩 License
<a href="LICENSE.txt">MIT License</a>

## 👏 Acknowledgments
This work was supported through the INL Laboratory Directed Research& Development (LDRD) Program under DOE Idaho Operations Office Contract DE-AC07-05ID14517 (project tracking number 24A1081-149). Accordingly, the publisher, by accepting the article for publication, acknowledges that the U.S. Government retains a nonexclusive, paid-up, irrevocable, worldwide license to publish or reproduce the published form of this manuscript or allow others to do so, for U.S. Government purposes.

## ✉️ Contact or Questions
<a href="https://www.webpages.uidaho.edu/vakanski/">A. Vakanski</a>, e-mail: vakanski at uidaho.edu
