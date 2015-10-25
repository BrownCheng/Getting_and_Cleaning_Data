# Description

The script `run_analysis.R`performs the 5 steps described in the course project's definition.

* 1), data is merged using the `rbind()` function. 
* 2), only those columns with the mean and standard deviation measures are taken from the whole dataset. And, they are given the correct names from `features.txt`.
* 3)  take the activity names and IDs from `activity_labels.txt` and they are substituted in the dataset.
* 4) On the whole dataset, column names are corrected with more descriptive manner, ex like “activity” and “subject”.
* 5) generate a new dataset with all the average measures for each subject and activity type. The output file is called `averages.txt.

# Variables

* `x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` are the name for the respective the data from the downloaded files.
* then, `x_data`, `y_data` and `subject_data` are modified by merging the datasets.
* `features` contains the correct names for the `x_data` dataset, which are applied to the column names stored in `mean_and_std_features`.
* activity names are modified to the `activities` variable.
* `all_d` merges `x_data`, `y_data` and `subject_data` in a big dataset.
* Finally, `averages` contains the relevant averages which will be later stored in a `.txt` file. 
* `ddply()` from the plyr package is used to apply `colMeans()`.
