# Earthquake-Prediction-using-Machine-Learning
## Introduction
In this project past seismic events data is used to predict future earthquakes in the Hindu Kush Mountain region. The dataset contains 22 columns and 14698 rows. 

## Data Preparation
For the preparation of data it is important to choose which columns need to be focused on. For this dataset the columns used are mag, place, depth, nst, gap and rms. These columns were chosen because these columns contribute the most and are necessary. The other columns were removed for varied reasons like contributing similar information, having more than 50% rows as null values, The information in the column is not important for the models and having id information which is used for serial numbering of the data.

Some of the chosen columns have null values which need to be substituted with other values. For substituting, the mean, median and mode can be used. But to choose which method to use it is necessary to first look at the columns and then derive the best method to choose from them. A boxplot for them is created and is shown below.

### Distribution of Important Dataset Parameters
#### Depth 
![Depth](https://github.com/Vighnesh95/Earthquake-Forecasting-using-Machine-Learning/assets/135556257/8e79ba4d-73e1-4f49-a620-c1430e27b780)

#### Number of Seismis Station (NST)
![nst](https://github.com/Vighnesh95/Earthquake-Forecasting-using-Machine-Learning/assets/135556257/cdc52fbb-1d8a-488a-9b38-72daefe70958)

#### RMS
![rms](https://github.com/Vighnesh95/Earthquake-Forecasting-using-Machine-Learning/assets/135556257/4f12879f-af1c-449d-8b05-56d49406c057)

#### Gap
![gap](https://github.com/Vighnesh95/Earthquake-Forecasting-using-Machine-Learning/assets/135556257/c41f5a7e-f613-4d97-b79a-c483b301df32)
As we can see from all the above distribution we need to use mode to replace null values to keep the distribution the same for replaced values as well.

## Models Used
- Random Forest Regression
- Light GBM Regression
- XG Boost Regression
- Gradient Boost Regression

Among these models the best model was Light GBM and the residual scatter plot of this model is shown below to check heteroskedasticity
![scatter](https://github.com/Vighnesh95/Earthquake-Forecasting-using-Machine-Learning/assets/135556257/bf2053fc-7bec-41eb-9311-e3ecc672ec2f)

## True Value vs Predicted Value
![lgbm_fit](https://github.com/Vighnesh95/Earthquake-Forecasting-using-Machine-Learning/assets/135556257/90dbadee-380e-48fb-824e-7faae1ccac3f)

