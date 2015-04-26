# - run_analysis.R code cleans the data using the following steps:
# - X_train.txt, y_train.txt and subject_train.txt is read from the data folder stored in the directory.
# - X_test.txt, y_test.txt and subject_test.txt are read from the data folder stored in the directory.
# - Combine testData with trainData to generate a data frame joinData; combine testLabel to trainLabel to create data fram joinLabel
#   and combine testSubject to trainSubject to create data frame joinSubject
# - Read features.txt file from the directory and store data in varaible called features. Only the mean and standard deviation measurements
#   are extracted.  Results in a 66 indices list.  Obtain a subset of joinData with the 66 corresponding columns.
# - Names of the columns in the subset are cleaned.  Remove the "()" and "-" symbols, and make the first letter of "mean" and "std"
#   a capital letter "M" and "S" respectively.
# - activity_labels.txt file is read from the directory stored and stored in a variable called activity.
# - Activity names are cleaned in the second column of activity. Make names to lower cases. If there is an underscore, it is removed,
#   and capitalize the letter right afte the underscore.
# - Transform the values of joinLabel according to the activity data frame.
# - Combine joinSubject, joinLabel and joinData by column to get a new data fram cleanedData.  Name the 
#   first two columns, "subject" and "activity". "Subject" contains integers ranging from 1 to 30 inclusive; "activity" contains 6
#   kinds of activity names; the last 66 columns contain measurement randing from -1 to 1 exclusive.
# - Write cleanedData out to "merged_data.txt" file in currect working directory.
# - Generate a second independent tidy data set with average of each measurement for each activity and each subject.  There are 
#   30 unique subjects 6 unique activites, giving a total of 180 combinations.  For each combination, the mean is calculated for 
#    each measurement.  After initialzing the result data frame and performing two for-loops, 180x68 data frame is obtained.
# - The result is written to "data_with_means.txt" file in working directory.

# 
