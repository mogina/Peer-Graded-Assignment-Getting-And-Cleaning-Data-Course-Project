Getting and Cleaning Data - Course Project
==========================================

This repository hosts the R code and documentation files for the Data Science's track course "Getting and Cleaning data", available in coursera.

The dataset being used is: [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

## Files

`CodeBook.md` a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data

`run_analysis.R` contains all 5 steps, which were described in Peer-graded Assignment:
* Merges the training and the test sets to create one data set.
* Extracts only the measurements on the mean and standard deviation for each measurement.
* Uses descriptive activity names to name the activities in the data set
* Appropriately labels the data set with descriptive variable names.
* From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

The result of 1-4 steps is *1-4stepsdata.txt* file, the result of this 5 step is *5stepdata.txt* file, which has tidy
