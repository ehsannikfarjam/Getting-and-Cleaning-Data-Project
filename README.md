# Getting and Cleaning Data - Course Project

This repository contains the R script and documentation for the Coursera "Getting and Cleaning Data" course project.

## Project Goal
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.

## Dataset
-   **Source Profile**: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
-   **Dataset**: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## Files
-   `run_analysis.R`: The R script that performs the data preparation and cleaning steps as defined in the course project instructions (see "Script Execution" below).
-   `CodeBook.md`: A code book that modifies and updates the available codebooks with the data to indicate all the variables and summaries calculated, along with units, and any other relevant information.
-   `tidy_data.txt`: The exported final dataset created by the script (submitted separately for grading).
-   `README.md`: Explains how all of the scripts work and how they are connected.

## Script Execution (`run_analysis.R`)
The `run_analysis.R` script performs the following core steps:

1.  **Preparation**: Make sure the `UCI HAR Dataset` exists in your working directory. The script uses the `dplyr` package.
2.  **Reads Data**: It reads in the features, activity labels, training and test datasets (`X`, `y`, and `subject` files).
3.  **Merges the training and the test sets to create one data set**: It concatenates the training and test data tables vertically. Then it binds the subject, activity, and feature measurements horizontally into one dataframe (`Merged_Data`).
4.  **Extracts only the measurements on the mean and standard deviation for each measurement**: It subsets the dataset, keeping only the Subject ID, Activity ID Columns, and features that contain "mean" or "std" in their names (`TidyData`).
5.  **Uses descriptive activity names to name the activities in the data set**: It replaces the numeric Activity IDs in the dataset with the descriptive names provided in `activity_labels.txt` (e.g., WALKING, SITTING).
6.  **Appropriately labels the data set with descriptive variable names**: Features names are cleaned up using regular expressions (e.g., replacing "t" with "Time", removing parentheses, expanding abbreviations like "Acc" to "Accelerometer").
7.  **Creates a second, independent tidy data set with the average of each variable for each activity and each subject**: It groups the data by `subject` and `activity` and calculates the mean for every feature.
8.  **Output**: The resulting independent dataset is written to a text file named `tidy_data.txt` in the working directory.

## Instructions for Running the Script
1.  Open an R console or terminal.
2.  Set your working directory to the root directory where the `UCI HAR Dataset` folder is located.
3.  Run the script using `source("run_analysis.R")` or from the command line using `Rscript run_analysis.R`.
4.  The output file `tidy_data.txt` will be generated in your working directory.
