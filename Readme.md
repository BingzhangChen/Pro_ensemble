# Modelling Prochlorococcus boundary README

This file accompanies the paper entitled " Salinity-Driven Boundary of Prochlorococcus in the Northwest Pacific Revealed by Ensemble Machine Learning" submitted to Journal of Geophysical Research: Machine Learning and Computation.

## Authors

Wenhui Liu, Bingzhang Chen, Baoguang Cong, Tong Jiang, Zihang Zhang, Min Wang, Hongbin Liu, Cui Guo

## Contact email

[bingzhang.chen\@strath.ac.uk](mailto:bingzhang.chen@strath.ac.uk)

## Brief summary of the study

This study uses an ensemble machine learning model to model the distribution boundary of *Prochlorococcus* in the China seas.

## Contributor

Bingzhang Chen is responsible for writing the R code.

## LICENSE

All the codes and data are covered by the MIT license. Please see the **LICENSE** file for details.

*************Metadata for essential files*************************

****Data files*****
pro_data.csv: Original data of in situ Prochlorococcus abundance collected during ten cruises in the South China Sea (2006-2012, 2018, 2021, and 2023) and seven cruises in the East China Sea (2009-2011, 2021, 2022). This data file also contains simultaneously measured temperature (Temp; unit: ºC), Salinity (Sal), nitrate + nitrite concentration (NO3; unit: µg/L), phosphate concentration (PO4; unit: µg/L). Chl: in situ Chl a concentration (µg/L). Pro: Prochlorococcus abundance (cells/mL).  lon: Longitude (ºE). lat: Latitude (ºN). Depth: sampling depth (m). DOY: Date of the year starting from 1 January. SSChl: in situ surface Chl a concentration (µg/L) corresponding to the Chl a concentration at 0 m. Year: sampling year.

Multi-decade averaged environmental data (Temp, Sal, NO3 and PO4) obtained from World Ocean Atlas and SSChl data obtained from SeaWIFS are not included due to their large size. These data can be downloaded from https://www.ncei.noaa.gov/access/world-ocean-atlas-2023/ and http://oceancolor.gsfc.nasa.gov.
****End of Data files*****


****R scripts*****
Ensemble_Pro_classification.Rmd: R script for the preprocessing of Prochlorococcus observation data (pro_data.csv) and the development of an ensemble model through training and stacking of the five machine learning algorithms. The classification task employs five machine learning algorithms: logistic Linear Regression, Artificial Neural Network, Support Vector Machine, Random Forest, and Boosted Regression Trees. The performance of the ensemble classification model is tested and compared to the single best model. The ensemble model is then used to output the weights of predictors on Prochlorococcus presence and the accumulated local effects of predictors on the probability of the presence of Prochlorococcus.

Ensemble_Pro_regression.Rmd: R script for the preprocessing of Prochlorococcus observation data (pro_data.csv) and the development of an ensemble model through training and stacking of the five machine learning algorithms. The regression task employs five machine learning algorithms: logistic Linear Regression, Artificial Neural Network, Support Vector Machine, Random Forest, and Boosted Regression Trees. The performance of the ensemble regression model is tested and compared to the ensemble classification model. The ensemble model is then used to output the weights of predictors on Prochlorococcus abundance. 
****End of R scripts*****
