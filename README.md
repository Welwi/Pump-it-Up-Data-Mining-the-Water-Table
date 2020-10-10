# Pump it Up: Data Mining the Water Table

![alt text](https://water.org/media/images/Waterorg_Our-Impact_Tanzania_Img-2.original.jpg)

## Team Members

Sam Videlock, Edna Fernandes and Anup Sebastian


## Project Intro/Objective

This project was part of a competition hosted by drivendata. The goal of the competition was to use data from Taarifa and the Tanzanian Ministry of Water and predict which pumps were functional, which needed repair and which were non functional. Results obtained helped optimize Tanzanian maintenance operations and ensure that clean, potable water is available to communities across Tanzania.

## Methods Used
   * **Modeling approach 1**: combined the targets "functional" and "functional needs repair" into one. Due to the small amount of "functional needs repair" target, the simplification was still able to get relatively good  results (79% accuracy).
   
   * **Modeling approach 2**: SMOTE, xgboost. Used the three different targets. The model had an 80% accuracy.
   
   * **Data Visuazliation**: PowerBI.


## Technologies
   * **Programming language**: Python.
   * **Libraries**: numpy, pandas, sklearn, imblearn
   
   
## Dataset Description  

The original training dataset is found on 'train_set_values.csv', 'train_set_labels.csv'. The test set can be found on 'test_set_values.csv'. As part of the cleaning step, the 'train_set_values.csv' and 'train_set_labels.csv' were merged, the null values were replaced with the mode and duplicate values were dropped. Categorical features have been transformed using target encoding. 

### Key Insights
  * Most wells have good water quality but about 17,000 with good water quality are non-functional.
  



In our analysis we were able to identify a smaller subset of non functioning wells that could be prioritized for restoration based on the insights. The analysis can be found on the Power BI file "Data_Analysis.pbix".

The final presentation can be found in the file 'Final_Presentation.pdf' or from this link: https://www.canva.com/design/DADxqPE0Yxg/Hurc4uIQFubGl3QY-9lOyA/view?utm_content=DADxqPE0Yxg&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton



## README Summary

In this README we will discuss our process for data cleaning, our insights in the dataset and our modeling process.



### Data Cleaning

The original training dataset is found on 'train_set_values.csv', 'train_set_labels.csv'. The test set can be found on 'test_set_values.csv'. The data comes from the drivendata.org for the competition Pump it Up: Data Mining the Water Table (https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/).

For our cleanup, we created a preprocessor file (preprocessor.py). In the preprocessor we have the following steps:
    - Merged the 'train_set_values.csv', 'train_set_labels.csv'.
    - Replaced all the null values with the mode.
    - Dropped some columns that seemed repretitive.
    - Target encoded our features
    

### Models

Binary Model
  - Can be found in the file "Binary_Simplified_Model.ipynb".
  - Combined the targets "functional" and "functional needs repair" into one.
  - Due to the small amount of "functional needs repair" target, the simplification was still able to get relatively good       results (79% accuracy).


Final Model
  - Can be found in the file 'XGBoost_with_SMOTE'
  - Had the three different targets ("functional", "functional needs repair" and "non functional").
  - We got an accuracy score of 80.59% (top 15% of competition) 
