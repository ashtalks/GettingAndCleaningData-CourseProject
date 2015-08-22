#Introduction
The script run_analysis.R performs the 5 steps described in the course project's definition.

1) All the similar data is merged using the rbind() function. We look at files having the same number of columns and that refer to the same entities.
2) Only columns with mean and standard deviation measures are taken from the entire dataset. 
3) Correct Names are assigned after extracting the columns taken from features.txt.
4) We take the activity names and IDs from activity_labels.txt and substitute it in the dataset.
5) On the entire dataset, columns with vague names are corrected.
6) A new dataset is generated with all the average measures for each subject and activity type.
7) The output file is called averages_data.txt, and uploaded to this repository.

Variables
x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
x_data, y_data and combine_data merge the previous datasets to further analysis.
features contain the correct names for the x_data dataset. It is applied to the column names stored in mean_and_std_features.
all_data merges x_data, y_data and subject_data in a big dataset.
averages_data contains the relevant averages which will be later stored in a .txt file. 
ddply() from the plyr package is used to apply colMeans().
