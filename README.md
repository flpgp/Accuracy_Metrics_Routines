# Accuracy_Metrics_Routines
Using routines in R and Python to forecast accuracy metrics.

To calculate \( R^2 \) (R-squared), MAPE (Mean Absolute Percentage Error), and RMSE (Root Mean Square Error) using the data from the "AlimentacaoDomicilio" sheet in the provided Excel file, we can follow these steps:

1. Read the data from the "AlimentacaoDomicilio" sheet.
2. Extract the "Focus" and "Observado" columns.
3. Calculate the \( R^2 \), MAPE, and RMSE values based on the formulas:

   - \( R^2 = 1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2} \)
   - \( \text{MAPE} = \frac{1}{n} \sum \left| \frac{y_i - \hat{y}_i}{y_i} \right| \times 100 \)
   - \( \text{RMSE} = \sqrt{\frac{\sum (y_i - \hat{y}_i)^2}{n}} \)

where:
- \( y_i \) are the actual values ("Observado").
- \( \hat{y}_i \) are the predicted values ("Focus").
- \( \bar{y} \) is the mean of the actual values.
- \( n \) is the number of observations.

Let's start by reading the data and calculating the required metrics.

It seems like the data in the Excel sheet doesn't have a header row, and the actual headers are located in the first row of the data. Additionally, it looks like there are some missing values in the "Focus" and "Observado" columns.

To proceed, I will:
1. Read the data again, specifying the first row as the header.
2. Clean the data by removing rows with missing values in the "Focus" or "Observado" columns.
3. Calculate the \( R^2 \), MAPE, and RMSE values using the cleaned data.

Let's go ahead and do this.

It seems like there was an issue because the columns "Focus" and "Observado" couldn't be found in the dataframe. This might be due to the fact that the actual column names might be different, or they might contain extra spaces or different capitalizations.

To address this, I will take a closer look at the column names in the dataframe and then proceed accordingly.

The columns in the dataframe are unnamed, which is why we encountered a KeyError earlier. 

To resolve this issue, I will use the first row of the dataframe as the header. This will help us identify and use the correct column names for further analysis.

Let's proceed with this approach.

Now that we have successfully cleaned the data and extracted the "Focus" and "Observado" columns, we can proceed to calculate the \( R^2 \), MAPE, and RMSE values.

Let's go ahead and perform these calculations.

Here are the calculated values based on the "Focus" and "Observado" columns from the "AlimentacaoDomicilio" sheet:

- \( R^2 \) (R-squared): \( 0.9042 \)
- RMSE (Root Mean Square Error): \( 0.3287 \)

However, the MAPE (Mean Absolute Percentage Error) value resulted in infinity. This issue typically arises when there are actual values (denominator in the MAPE formula) that are very close to zero, leading to a division by zero or a very large value. 

To address this, we could:
1. Exclude the rows where the actual values are zero or very close to zero before calculating MAPE.
2. Use a modified version of MAPE that avoids division by zero.

Would you like to proceed with one of these options or do you have another preference?
