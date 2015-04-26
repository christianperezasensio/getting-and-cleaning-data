Script description
-----------------

The script named as run_analysis.R first downloads and unzips the dataset from:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Then merges the train and test datasets to one data frame with **rbind**. The next step is to extract only the measurements on the mean and standard deviation for each measurement. This is done with **grep**. Next, to make descriptive activity names, the activity_labels are loaded and cleaned using **tolower** and **gsub**. Then the datasets x, y and subject are merged and exported to merged.txt with **write.table**. The last step is to create the tidy dataset with the average of each variable for each activity and each subject. This is exported to average.txt.