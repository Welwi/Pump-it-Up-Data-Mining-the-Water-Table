# Pump it Up: Data Mining the Water Table

![alt text](https://water.org/media/images/Waterorg_Our-Impact_Tanzania_Img-2.original.jpg)

## Team Members

Sam Videlock, Edna Fernandes and Anup Sebastian


## Project Intro/Objective

This project was part of a competition hosted by drivendata. The goal of the competition was to use data from Taarifa and the Tanzanian Ministry of Water and predict which pumps were functional, which needed repair and which were non functional. Results obtained helped optimize Tanzanian maintenance operations and ensure that clean, potable water is available to communities across Tanzania.

## Methods Used
   * **Modeling approach 1**: combined the targets "functional" and "functional needs repair" into one. Due to the small amount of "functional needs repair" target, the simplification was still able to get relatively good  results (79% accuracy).
   
   * **Modeling approach 2**: SMOTE, xgboost. Used the three different targets. The model had an 80% accuracy (top 15% of competition).
   
   * **Data Visuazliation**: PowerBI.


## Technologies
   * **Programming language**: Python.
   * **Libraries**: numpy, pandas, sklearn, imblearn
   
   
## Dataset Description  

The original training dataset is found on 'train_set_values.csv', 'train_set_labels.csv'. The test set can be found on 'test_set_values.csv'. As part of the cleaning step, the 'train_set_values.csv' and 'train_set_labels.csv' were merged, the null values were replaced with the mode and duplicate values were dropped. Categorical features have been transformed using target encoding. 

### Key Insights
  * There were a total of 23,000 non-functional wells.
  * Most wells have good water quality but about 17,000 with good water quality are non-functional.
  * Both submersible, and motorpumps tend to fal at higher rate than gravity and handpump wells. This is porbably due to the increase in maintenance necessary.
  * About 9,000 wells that are currently non-functional have adequate water availability. However, they can not be accessed.
  * Well restauration should be prioritzed to the ones that have good and high water quality and with gravity or handpump as their lifting system.
  
  
![some image](https://github.com/Welwi/Pump-it-Up-Data-Mining-the-Water-Table/blob/master/all_images.PNG)


## Final Presentation
The final presentation can be found in the file 'Final_Presentation.pdf' or from this link: https://www.canva.com/design/DADxqPE0Yxg/Hurc4uIQFubGl3QY-9lOyA/view?utm_content=DADxqPE0Yxg&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton

