# Code Book for Getting and Cleaning Data Course Project

This code book describes the variables, the data, and any transformations or work that was performed to clean up the data.

## The Data Source
- Original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
- Original description of the dataset: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Data Set Information
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

## The Variables
The `tidy_data.txt` data set contains the following variables:

- `subject`: The ID of the test subject (integer from 1 to 30).
- `activity`: The type of activity performed (factor with 6 levels: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING).

The remaining variables are the average of each feature for each activity and each subject. The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals `tAcc-XYZ` and `tGyro-XYZ`. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (`tBodyAcc-XYZ` and `tGravityAcc-XYZ`) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (`tBodyAccJerk-XYZ` and `tBodyGyroJerk-XYZ`). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (`tBodyAccMag`, `tGravityAccMag`, `tBodyAccJerkMag`, `tBodyGyroMag`, `tBodyGyroJerkMag`).

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing `fBodyAcc-XYZ`, `fBodyAccJerk-XYZ`, `fBodyGyro-XYZ`, `fBodyAccJerkMag`, `fBodyGyroMag`, `fBodyGyroJerkMag`. (Note the 'f' to indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for each pattern:
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

We only extracted the measurements on the mean and standard deviation for each measurement.

The list of variables in `tidy_data.txt`:
(Note: these are the descriptive names applied during the cleaning process)
1.  `subject`
2.  `activity`
3.  `TimeBodyAccelerometerMean()-X`
4.  `TimeBodyAccelerometerMean()-Y`
5.  `TimeBodyAccelerometerMean()-Z`
6.  `TimeBodyAccelerometerSTD()-X`
7.  `TimeBodyAccelerometerSTD()-Y`
8.  `TimeBodyAccelerometerSTD()-Z`
9.  `TimeGravityAccelerometerMean()-X`
10. `TimeGravityAccelerometerMean()-Y`
11. `TimeGravityAccelerometerMean()-Z`
12. `TimeGravityAccelerometerSTD()-X`
13. `TimeGravityAccelerometerSTD()-Y`
14. `TimeGravityAccelerometerSTD()-Z`
15. `TimeBodyAccelerometerJerkMean()-X`
16. `TimeBodyAccelerometerJerkMean()-Y`
17. `TimeBodyAccelerometerJerkMean()-Z`
18. `TimeBodyAccelerometerJerkSTD()-X`
19. `TimeBodyAccelerometerJerkSTD()-Y`
20. `TimeBodyAccelerometerJerkSTD()-Z`
21. `TimeBodyGyroscopeMean()-X`
22. `TimeBodyGyroscopeMean()-Y`
23. `TimeBodyGyroscopeMean()-Z`
24. `TimeBodyGyroscopeSTD()-X`
25. `TimeBodyGyroscopeSTD()-Y`
26. `TimeBodyGyroscopeSTD()-Z`
27. `TimeBodyGyroscopeJerkMean()-X`
28. `TimeBodyGyroscopeJerkMean()-Y`
29. `TimeBodyGyroscopeJerkMean()-Z`
30. `TimeBodyGyroscopeJerkSTD()-X`
31. `TimeBodyGyroscopeJerkSTD()-Y`
32. `TimeBodyGyroscopeJerkSTD()-Z`
33. `TimeBodyAccelerometerMagnitudeMean()`
34. `TimeBodyAccelerometerMagnitudeSTD()`
35. `TimeGravityAccelerometerMagnitudeMean()`
36. `TimeGravityAccelerometerMagnitudeSTD()`
37. `TimeBodyAccelerometerJerkMagnitudeMean()`
38. `TimeBodyAccelerometerJerkMagnitudeSTD()`
39. `TimeBodyGyroscopeMagnitudeMean()`
40. `TimeBodyGyroscopeMagnitudeSTD()`
41. `TimeBodyGyroscopeJerkMagnitudeMean()`
42. `TimeBodyGyroscopeJerkMagnitudeSTD()`
43. `FrequencyBodyAccelerometerMean()-X`
44. `FrequencyBodyAccelerometerMean()-Y`
45. `FrequencyBodyAccelerometerMean()-Z`
46. `FrequencyBodyAccelerometerSTD()-X`
47. `FrequencyBodyAccelerometerSTD()-Y`
48. `FrequencyBodyAccelerometerSTD()-Z`
49. `FrequencyBodyAccelerometerMeanFreq()-X`
50. `FrequencyBodyAccelerometerMeanFreq()-Y`
51. `FrequencyBodyAccelerometerMeanFreq()-Z`
52. `FrequencyBodyAccelerometerJerkMean()-X`
53. `FrequencyBodyAccelerometerJerkMean()-Y`
54. `FrequencyBodyAccelerometerJerkMean()-Z`
55. `FrequencyBodyAccelerometerJerkSTD()-X`
56. `FrequencyBodyAccelerometerJerkSTD()-Y`
57. `FrequencyBodyAccelerometerJerkSTD()-Z`
58. `FrequencyBodyAccelerometerJerkMeanFreq()-X`
59. `FrequencyBodyAccelerometerJerkMeanFreq()-Y`
60. `FrequencyBodyAccelerometerJerkMeanFreq()-Z`
61. `FrequencyBodyGyroscopeMean()-X`
62. `FrequencyBodyGyroscopeMean()-Y`
63. `FrequencyBodyGyroscopeMean()-Z`
64. `FrequencyBodyGyroscopeSTD()-X`
65. `FrequencyBodyGyroscopeSTD()-Y`
66. `FrequencyBodyGyroscopeSTD()-Z`
67. `FrequencyBodyGyroscopeMeanFreq()-X`
68. `FrequencyBodyGyroscopeMeanFreq()-Y`
69. `FrequencyBodyGyroscopeMeanFreq()-Z`
70. `FrequencyBodyAccelerometerMagnitudeMean()`
71. `FrequencyBodyAccelerometerMagnitudeSTD()`
72. `FrequencyBodyAccelerometerMagnitudeMeanFreq()`
73. `FrequencyBodyAccelerometerJerkMagnitudeMean()`
74. `FrequencyBodyAccelerometerJerkMagnitudeSTD()`
75. `FrequencyBodyAccelerometerJerkMagnitudeMeanFreq()`
76. `FrequencyBodyGyroscopeMagnitudeMean()`
77. `FrequencyBodyGyroscopeMagnitudeSTD()`
78. `FrequencyBodyGyroscopeMagnitudeMeanFreq()`
79. `FrequencyBodyGyroscopeJerkMagnitudeMean()`
80. `FrequencyBodyGyroscopeJerkMagnitudeSTD()`
81. `FrequencyBodyGyroscopeJerkMagnitudeMeanFreq()`
82. `Angle(TimeBodyAccelerometerMean,Gravity)`
83. `Angle(TimeBodyAccelerometerJerkMean),GravityMean)`
84. `Angle(TimeBodyGyroscopeMean,GravityMean)`
85. `Angle(TimeBodyGyroscopeJerkMean,GravityMean)`
86. `Angle(X,GravityMean)`
87. `Angle(Y,GravityMean)`
88. `Angle(Z,GravityMean)`

## Data Transformations
The following steps were performed by `run_analysis.R` to clean the data:
1.  **Merges the training and the test sets to create one data set.**
    -   `X_train.txt`, `y_train.txt` and `subject_train.txt` from the `./UCI HAR Dataset/train` folder were read.
    -   `X_test.txt`, `y_test.txt` and `subject_test.txt` from the `./UCI HAR Dataset/test` folder were read.
    -   `rbind()` was used to combine the training and test datasets.
    -   `cbind()` was used to combine the features, subjects and activities into one dataset.
2.  **Extracts only the measurements on the mean and standard deviation for each measurement.**
    -   `dplyr::select()` along with `contains("mean")` and `contains("std")` was used to subset the columns.
3.  **Uses descriptive activity names to name the activities in the data set.**
    -   The `activity_labels.txt` file was read and used to replace the numeric activity IDs (1-6) with their corresponding labels (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING).
4.  **Appropriately labels the data set with descriptive variable names.**
    -   The `features.txt` file was used for the initial column names.
    -   `gsub()` was used to modify the variable names to be more descriptive:
        -   `Acc` replaced with `Accelerometer`
        -   `Gyro` replaced with `Gyroscope`
        -   `BodyBody` replaced with `Body`
        -   `Mag` replaced with `Magnitude`
        -   Starting with `t` replaced with `Time`
        -   Starting with `f` replaced with `Frequency`
        -   `tBody` replaced with `TimeBody`
        -   `-mean()` replaced with `Mean`
        -   `-std()` replaced with `STD`
        -   `-freq()` replaced with `Frequency`
        -   `angle` replaced with `Angle`
        -   `gravity` replaced with `Gravity`
5.  **From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.**
    -   The dataset was grouped by `subject` and `activity` using `dplyr::group_by()`.
    -   The average of each variable for each group was calculated using `dplyr::summarise_all()`.
    -   The resulting tidy dataset was written to `tidy_data.txt` using `write.table()` with `row.name=FALSE`.
