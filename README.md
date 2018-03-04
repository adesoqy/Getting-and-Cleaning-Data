# Getting-and-Cleaning-Data
Coursera : getting and cleaning data course project

Create one R script called run_analysis.R that does the following:
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


Script download and unpack "UCI HAR Dataset" from internet ( https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip ), create some data aggregation and create a new file - "mean_values.txt" with the average of each variable for each activity and each subject of investigation

Script read.datas from test and train subset from txt ("X_train.txt", "X_test.txt"), and merge them with information about type of activity from files ("y_train.txt", "y_test.txt")

Text labels contains in file "activity_labels.txt" so the first column with numeric marks of activity replace by srting labels

Names of column are in file "features.txt", so column's names have been replaced to names from this files

Now the first column of our dataset is type of activity, and 561 column with different measuresements.

We take only column, that contains in names "-mean()" or "-std()", because we need only information about mean values and standart deviation

We add add for the each row information about subject from ("subject_test.txt", "subject_train.txt")

Now we have dataset with first column - number of subject, second column - name of activity, and 79 columns with measureness

Finally script aggregate data by ezch subject and activity type and receive a mean value by 79 columns with measureness

The new dataset we save as "tidy_data.txt" file to main directory with our zip file
