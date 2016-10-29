# Introduction

We have just one R file - run_analysys.R. It performs 5 steps from assignment.

* As if was described in README.md of http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones , there are two groups: 70%(training dataset) and 30%(test), thats why we need to merge them together. There wasn't any problem with that, I had X,Y and subject files. X represent all the measurements, Y represent activity, that subject was doing, and subject represent the subject. It's worth saying, that X,Y and subject files have the same row length.
* Next, we need to get only average and standart deviation. This is the hardest part, on my opinion. Here's what I figure out, and what helped me: number of rows in features.txt is equal to number of columns in X_test.txt and X_train.txt.
* We need to convert digital activity id's into some string representation, which is located in activity_labels.txt
* Correcting column names
* Creating a new dataset, grouped by subject and activity. (30 subjects * 6 activities = 180 rows). The output file is called `grouped_data.txt`, and uploaded to this repository.

# Variables

* `XTrain`, `YTrain`, `XTest`, `YTest`, `SubjectTrain` and `SubjectTest` have the data from training and test  datasets.
* `X`, `Y` and `Subject` is a result of merging test and train datasets together.
* `features` is a dataframe from features.txt file.
* `meanAndStdFeatures` - is a new dataset, which has only average and standart deviation
* `activities` contains 6 types of activity: WALKING, WALKING_UPSTAIRS,WALKING_DOWNSTAIRS, SITTING, STANDING,LAYING, and we need to map them to `Y`
* `finalData` merges `X`, `Y` and `Subject` in one complex dataset.
* `groupedBySubjectAndAcitivity` contains average data, grouped by subject and activity. I used dplyr package to calculate that.
