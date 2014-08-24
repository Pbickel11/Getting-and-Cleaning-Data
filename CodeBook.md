Getting and Cleaning Data Project Code Book
============================================
This file describes the variables, data, and work that I have performed to clean the data.  
The site where the data was obtained:  
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones      
The data for the project:  
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  

The run_analysis.R script performs the following steps:   
 1. Read X_train.txt, y_train.txt and subject_train.txt from the "./data/train" folder and store them as trainData, trainLabel and trainSubject.       
 2. Read X_test.txt, y_test.txt and subject_test.txt from the "./data/test" folder and store them as testData, testLabel and testsubject.  
 3. Concatenate testData and trainData to generate a 10299x561 data frame named joinData. Concatenate testLabel and trainLabel to generate a 10299x1 data frame named joinLabel. Concatenate testSubject and trainSubject to generate a 10299x1 data frame named joinSubject.  
 4. Read the features.txt file from the "/data" folder and store the data as features. We only extract the measurements on the mean and standard deviation. This results in a 66 indices list. We get a subset of joinData with 66 columns.  
 5. Clean the column names of the subset. We remove the "()" and "-" symbols in the names, and capitalize "mean" and "std".
 6. Read the activity_labels.txt file from the "./data"" folder and store the data as activity.  
 7. Clean the activity names in the second column of activity. Make all names to lower cases. Remove the underscore and capitalize the letter immediately after the underscore.  
 8. Transform the values of joinLabel according to the activity data frame.  
 9. Combine the joinSubject, joinLabel and joinData by column to get a new cleaned 10299x68 data frame named cleanedData. Name the first two columns subject and activity. 
 10. Write the cleanedData out to merged_data.txt in the working directory.  
 11. Create a second tidy data set with the average of each measurement for each activity and subject. 30 subjects and 6 activities results in a 180 combinations. For each combination, calculate the mean of each measurement with the corresponding combination. After initializing the result data frame and performing the two for-loops, we get a 180x68 dataframe.
 12. Write the result out to data_with_means.txt in the working directory. 
