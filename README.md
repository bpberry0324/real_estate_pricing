# On Home and Real Estate Sales in Ames, Iowa

This survey examines and evaluates potential factors for the improvement of property value by home and real estate owners intending to sell.

### Table of Contents:

- Part I: Summary of Findings
- Part II: File Directory
- Part III: On the Data Used
- Part IV: Conclusion

## Part I: Summary of Findings

Home sellers often find themselves overwhelmed by the prospect of property appraisal. When are they moving, and to where? How much is their home worth and how much time is there to realize this potential? And (perhaps most importantly during the final year) what can be done in the time remaining to improve property value and receive the highest possible selling price? Relevant factors consist of things an owner might alter in what time remains before the sale date to turn the highest profit.

A serviceable linear regression model was formulated during the course of this study to provide an accurate base number from which to begin focusing on more malleable traits. Many features were engineered and considered, and interactions received attention as well. Heatmaps and pairplots that examine key relationships and demonstrate important findings (correlation, linearity, etc.) are provided in the main summary notebook. Unsurprisingly, factors such as size and total space encompassed by a property weigh considerably in a its perceived value, as does age and location.

Among changeable variables--that is, those that an owner might improve within a reasonable amount of time--overall condition proved to be significant. The quality and condition of the kitchen and of any fireplaces where they exist proved most significant, with the condition of other areas less so.

## Part II: File Directory

|File or Folder|Description|
|---|---|
|appendices/|folder including notebooks with in-depth treatment of more extensive phases of this study (i.e. cleaning and EDA)|
|cleaning/|folder including readouts of summary statistics for the training and test datasets pre-cleaning and post-cleaning|
|datasets/|folder including all .csv tables used|
|images/|folder including supplementary images|
|main.ipynb|primary project notebook outlining the modeling process and conclusions|
|presentation.pdf|PDF version of final slide presentation|
|README.md|brief summary of the aims, findings, and conclusions of this project|
|visualizations/|folder including pairplots, heatmaps, and scatterplots to illustrate the most relevant findings|

## Part III: On the Data Used

##### Initial Datasets

- [`test.csv`](./datasets/test.csv): test dataset as initially provided by Kaggle
- [`train.csv`](./datasets/train.csv): training dataset as initially provided by Kaggle

##### Additional (Derived) Datasets

- [`base_submit.csv`](./datasets/base_submit.csv): final .csv file of selling price estimates for the test dataset from Kaggle
- [`final_train.csv`](./datasets/final_train.csv): datset used in the main summary notebook demonstration of this study's final regression model
- [`main_test.csv`](./datasets/main_test.csv): test dataset (post-cleaning) whose features were then engineered for the Kaggle submission
- [`main_train.csv`](./datasets/main_train.csv): training dataset (post-cleaning) from which features were derived and the regression model developed

Below is a list of features included in this study's final regression model for each property, as named in `final_train.csv`:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|1st_flr_sf|int|final_train.csv|first floor square footage|
|2nd_flr_sf|int|final_train.csv|second floor square footage|
|bsmt_code|int|final_train.csv|basement condition encoded numerically|
|ex_kitch|int|final_train.csv|binary variable demonstrating whether or not kitchen quality is listed as excellent|
|garage_area|float|final_train.csv|garage square footage|
|gr_liv_area|int|final_train.csv|total square footage of above-ground living areas|
|grg_code|int|final_train.csv|garage condition encoded numerically|
|is_new|int|final_train.csv|binary variable demonstrating whether or not a property was built after the year 2000|
|is_new_rem|int|final_train.csv|binary variable demonstrating whether or not a property had remodels/additions after the year 2000|
|mas_vnr_area|float|final_train.csv|masonry veneer square footage|
|nbhd_rank_idx_1|int|final_train.csv|binary variable indexing (1 through 6) a property's neighborhood, from most to least desirable|
|nbhd_rank_idx_2|int|final_train.csv|binary variable indexing (1 through 6) a property's neighborhood, from most to least desirable|
|nbhd_rank_idx_3|int|final_train.csv|binary variable indexing (1 through 6) a property's neighborhood, from most to least desirable|
|nbhd_rank_idx_4|int|final_train.csv|binary variable indexing (1 through 6) a property's neighborhood, from most to least desirable|
|nbhd_rank_idx_5|int|final_train.csv|binary variable indexing (1 through 6) a property's neighborhood, from most to least desirable|
|nbhd_rank_idx_6|int|final_train.csv|binary variable indexing (1 through 6) a property's neighborhood, from most to least desirable|
|overall_qual|int|final_train.csv|overall construction quality|
|pos_a/n|int|final_train.csv|binary variable demonstrating whether or not a property is located near desirable amenities|
|sale_code|int|final_train.csv|numeric encoding of sale type|
|total_bsmt_sf|float|final_train.csv|square footage of basement area|
|total_bath|int|final_train.csv|number of serviceable bathrooms|

## Part IV: Conclusion

Further study might allow for the development of an even more accurate model, in which case, the relative significance of each variable could at least potentially change.

In the meantime, to reiterate, home owners considering or intent on selling would do well to focus first on improving kitchen areas, and then on improving fireplaces to maximize profit when time is limited.
