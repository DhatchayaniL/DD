__Regression:__

1. **Avocado price prediction - Decision tree regressor**
    1. *Data cleaning*
        * No null values
        * No duplicates
    2. *Data visualization*
        * Each and every columns are correlated
        * There is a positive relation between 'total volume' and all the other columns.
        * All the other columns are also positively correlated with all the columns except the target column.
        * Total volume can go above 3 if the average price is in between 0.5 to 2
        * Average price of 1.0 to 1.6 are high in frequency
    3. *Model Building*
        * Decision tree regressor
    4. *Model Benckmarking*
        * sklearn accuracy - 72.1%
        * Custom code accuracy - 70.3%

2. **Car price prediction - Random forest regressor**
    1. *Data cleaning*
        * Had null values
        * Numerical columns - Imputed using Iterative Imputer
        * Categorical columns - Imputed using Mode
        * Dropped all duplicates
    2. *Data visualization*
        * Selling price is maximum in 50,000 to 3Lakhs
        * Fuel efficiency is maximum at 20 km/L
        * Dropped LPG and CNG from fuel type as it is very less.
    3. *Model Building*
        * Random forest regressor
    4. *Model Benckmarking*
        * sklearn accuracy - 81.4%
        * Custom code accuracy - 80.4%

3. **Taxi price prediction - Linear regression**
    1. *Data cleaning*
        * No null values
        * Dropped all duplicates
    2. *Data visualization*
   ![pairplot](https://github.com/DhatchayaniL/DD/assets/88893048/6bca7e3b-4574-4e81-9d9c-e31fd174d461)
        * Dropped distance_traveled and num_of_passengers as they are less correlated with other columns.
        * Total fare and fare are highly correlated
        * miscellaneous fees and surge_applied are highly correlated in correlation matrix.
   ![taxi_cor](https://github.com/DhatchayaniL/DD/assets/88893048/0df62a66-1ebc-4548-8bcd-ff9bf7a27ab6) 
           
    4. *Model Building*
        * Linear regression
    5. *Model Benckmarking*
        * sklearn accuracy - 99%
        * Custom code accuracy - 99%
          

    ![lin](https://github.com/DhatchayaniL/DD/assets/88893048/481afef5-3b10-42f8-abe3-b2eb3b75b9b4)

__Classification__

4. **Credit card payment classification - KNN**
    1. *Data cleaning*
        * No null values
        * Dropped all duplicates
    2. *Data visualization*
        * There is no relation between v1 to v28 columns
   ![correlation](https://github.com/DhatchayaniL/DD/assets/88893048/aebe3e2a-9f7c-4e5c-9ef4-9860fb504ea4)
        * Did principal component analysis and reduces its dimentionality which increases correlation between v1 to v28 columns
   ![correlation after PCA](https://github.com/DhatchayaniL/DD/assets/88893048/b4c524d4-28f3-4bdc-a757-48f90689f93c)
        * Transaction amount is higher in 0 to 2000
        * Used robust scalar for normalization
   ![distribution plot](https://github.com/DhatchayaniL/DD/assets/88893048/4c4eeb04-4641-49c5-8724-09c8c1e58df9)
    3. *Model Building*
        * K-Nearest Neightbour
    4. *Model Benckmarking*
        * sklearn accuracy - 94.3%
        * Custom code accuracy - 94.3%
    ![confusion matrix heatmap](https://github.com/DhatchayaniL/DD/assets/88893048/41acd77b-13a7-4823-9291-d21a0949f51a)

5. **Rain in australia - Logistic regression**
    1. *Data cleaning*
        * Had null values
        * Used KNN - imputer to fill null values
        * Dropped all duplicates
    2. *Data visualization*
   ![Rain Tomorrow vs. Rain Today](https://github.com/DhatchayaniL/DD/assets/88893048/9432afb3-3bd3-41e5-ad23-e497e47ac088)
        * Imbalanced dataset
        * Did over sampling
      
          
   ![after sampling](https://github.com/DhatchayaniL/DD/assets/88893048/9f8a2c30-0459-44b7-b483-15b9a3d03a77)

        * Min Temp and Max Temp are positively correlated 
        * Temp3pm and Temp9am are positively correlated
    4. *Model Building*
        * Logistic regression
    5. *Model Benckmarking*
        * sklearn accuracy - 1.0%
        * Custom code accuracy - 1.0%

7. **Email spam classification - Multinomial naive bayes**
    1. *Data cleaning*
        * No null values
        * Dropped all duplicates
    2. *Data visualization*
        * Add 2 necessary columns
        * All columns are positively correlated
        * Did stemming and lemmetization
        * Call is the most repeted work in spam messages
        * U is the most repeted work in ham messages
    3. *Model Building*
        * Multinomial naive bayes
    4. *Model Benckmarking*
        * sklearn accuracy - 96.9%
        * Custom code accuracy - 95.9%

8. **Salary prediction - Ada boost classifier**
    1. *Data cleaning*
        * No null values
        * Dropped all duplicates
    2. *Data visualization*
        * Imbalanced dataset
        * Did oversampling using Random sampler
        * Work class of self-emp-inc is higher
        * Doctorate people are higher in the dataset
        * In marital status married-civ-spouse is higher
        * U is the most repeted work in ham messages
    3. *Model Building*
        * Ada boost classifier
    4. *Model Benckmarking*
        * sklearn accuracy - 80%
        * Custom code accuracy - 74%

9. **Salary prediction - Ada boost classifier**
    1. *Data cleaning*
        * Had null values
        * Did iterative imputer
        * Dropped all duplicates
    2. *Data visualization*
        * Movies with drama genre are higher
        * Most number of movies are released in 2007
        * Most number of movies are release on friday
        * May is the highset average gross month
        * French movies are highest in number
    3. *Model Building*
        * XG boost classifier
    4. *Model Benckmarking*
        * sklearn accuracy - 81.7%
        * Custom code accuracy - 81.7%
