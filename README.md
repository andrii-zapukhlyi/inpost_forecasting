# Inpost forecasting - ML regression project

#### Data description: 
- DimDates - CSV file - Database with date information (Year, Month, Day, Weekday, Weekend, Holiday, etc.)
- PostingVolume - Parquet file - Database with daily transmissions (From January 1, 2021 to August 31, 2023). The data is grouped per day by two services APM and COURIER along with a separated customer X. This customer provides us with its order forecast every month at the end of the previous month
- Customers_Orders - EXCEL file - Data provided by customer (X) since the beginning of 2023. The data for the upcoming month is sent at the end of the previous month. The file contains the number of orders expected by the customer each day
- Task_Data_Temperature - Folder with CSV Files - The folder contains CSV files, where each file (for each month - between January 2021 and August 2023) stores data on temperatures (maximum, average, minimum temperature) and precipitation (rain and snow). The data is collected for two cities: Warszaw and Krakow


#### Project objective:
Import, preprocess, analyze the provided datasets and develop predictive models to forecast the number of transmissions for a specific day in the upcoming week or month

## Achievements

After analyzing and merging the datasets, I built machine learning models to predict the number of transmissions. The XGBoost model achieved the best performance with the following results:

- **R² Score:** 0.97
- **Mean Squared Error (MSE):** 0.03
- **Mean Absolute Error (MAE):** 0.12

These results demonstrate that the model accurately predicts transmissions, explaining about 97% of the variance with minimal error. Additionally, cross-validation and performance metrics indicate no signs of overfitting. 

##### Suggestions for further improving the model:
- Feature Engineering
- Enhanced GPU Utilization
- Advanced Data preprocessing techniques

Overall, the **XGBoost model** provides a robust and reliable solution for forecasting future transmissions. 
