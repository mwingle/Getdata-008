#Getdata-008#

The purpose of ths project is to clean and tidy the smartphone activity dataset obtained from the URL below to help facilitate further exploration and analysis.

One of the most exciting areas in all of data science right now is wearable computing - see for example <a href="http://www.insideactivitytracking.com/data-science-activity-tracking-and-the-battle-for-the-worlds-top-sports-brand/">this article</a> . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

To run the cleaning script (run_analysis.R), you must download the zip file yourself into the current working directory that the script will be run from. It should be named "UCI HAR Dataset.zip".

The data can be found at:  https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

The script performs the following tasks:

  1.  Merges the training and the test sets to create one data set.
  2.  Extracts only the measurements on the mean and standard deviation for each measurement. 
  3.  Uses descriptive activity names to name the activities in the data set
  4.  Appropriately labels the data set with descriptive variable names.  I used the existing variable names, and just removed the parenthesis to make the data more user-friendly.
  5.  From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
  
  Please read the supplied CodeBook.md file for more detailed information about the data set.

This script was created using R 3.1.1 and R-Studio 0.98.99 on Mac OSX V10.9.5.