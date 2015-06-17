#Getting and Cleaning Data Course Project CodeBook

This file describes Describes the variables, the data, and any transformations or work that was performed to clean up the data.

#Data source
The site where the data was obtained:  
    http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones      
The data for the project:  
    https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 


# run_analysis.R 

This script performs the following steps to clean the data:   

1. Read and merge data files by using the `rbind()` function. Those files should have the same number of columns and referring to the same entities.
2. Retrieve columns with the mean and standard deviation measures from the dataset, and then assign the columns with correct names, taken from `features.txt`.
3. As activity data is addressed with values,take the activity names and IDs from `activity_labels.txt` and they are substituted in the dataset.
4. Correct the columns with vague column names.
5. Generate a tidy dataset with all the average measures for each subject and activity type.

# Variables

1. Source Data: `x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` 2. Merged Data: * `x_data`, `y_data` and `subject_data` 
3. Data with correct names and numeric vector data: `features`,`activities` `mean_and_std_features`.
4. `all_data` merges `x_data`, `y_data` and `subject_data` in a big dataset.
5. Final tidy data:  `TidyData` 
6. Function needed: `ddply()` from the plyr package is used to apply `colMeans()` and ease the development.
