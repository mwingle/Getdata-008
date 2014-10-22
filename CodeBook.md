#Overview
This document describes the modified data set output by the run_analysis.R script.

A full description of the original dataset can be found in the README.txt file of the UCI HAR Dataset.zip file.  More information about the original dataset can be found in the README.md file in this project.

##Description of transformed data set, modifed from the original description:
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The original dataset had been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. *The run_analysis.R script merges the two datasets together.*

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See the section titled 'Feature Selection' for more details. 

###For each record it is provided:


- An identifier of the subject who carried out the experiment, 1 through 30
- Its activity label (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING)
- 66 columns of time and frequency domain variables. 

###Feature Selection 

From the original README.txt:

>The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

>Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

>Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

>These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.
 
The run_analysis.R script produces tidyAverages.txt, which includes contains the average of each variable, grouped by test subject and activity.

These are the fields of tidyAverages.txt ouput by the run_analysis.R script.

Units:  Fields starting with "t" are time domain values, already normalized.  Fields starting with "f" are frequency domain values, already normalized.

1. subject
2. activity
3. mean-tBodyAcc-mean-X
4. mean-tBodyAcc-mean-Y
5. mean-tBodyAcc-mean-Z
6. mean-tBodyAcc-std-X
7. mean-tBodyAcc-std-Y
8. mean-tBodyAcc-std-Z
9. mean-tGravityAcc-mean-X
10. mean-tGravityAcc-mean-Y
11. mean-tGravityAcc-mean-Z
12. mean-tGravityAcc-std-X
13. mean-tGravityAcc-std-Y
14. mean-tGravityAcc-std-Z
15. mean-tBodyAccJerk-mean-X
16. mean-tBodyAccJerk-mean-Y
17. mean-tBodyAccJerk-mean-Z
18. mean-tBodyAccJerk-std-X
19. mean-tBodyAccJerk-std-Y
20. mean-tBodyAccJerk-std-Z
21. mean-tBodyGyro-mean-X
22. mean-tBodyGyro-mean-Y
23. mean-tBodyGyro-mean-Z
24. mean-tBodyGyro-std-X
25. mean-tBodyGyro-std-Y
26. mean-tBodyGyro-std-Z
27. mean-tBodyGyroJerk-mean-X
28. mean-tBodyGyroJerk-mean-Y
29. mean-tBodyGyroJerk-mean-Z
30. mean-tBodyGyroJerk-std-X
31. mean-tBodyGyroJerk-std-Y
32. mean-tBodyGyroJerk-std-Z
33. mean-tBodyAccMag-mean
34. mean-tBodyAccMag-std
35. mean-tGravityAccMag-mean
36. mean-tGravityAccMag-std
37. mean-tBodyAccJerkMag-mean
38. mean-tBodyAccJerkMag-std
39. mean-tBodyGyroMag-mean
40. mean-tBodyGyroMag-std
41. mean-tBodyGyroJerkMag-mean
42. mean-tBodyGyroJerkMag-std
43. mean-fBodyAcc-mean-X
44. mean-fBodyAcc-mean-Y
45. mean-fBodyAcc-mean-Z
46. mean-fBodyAcc-std-X
47. mean-fBodyAcc-std-Y
48. mean-fBodyAcc-std-Z
49. mean-fBodyAccJerk-mean-X
50. mean-fBodyAccJerk-mean-Y
51. mean-fBodyAccJerk-mean-Z
52. mean-fBodyAccJerk-std-X
53. mean-fBodyAccJerk-std-Y
54. mean-fBodyAccJerk-std-Z
55. mean-fBodyGyro-mean-X
56. mean-fBodyGyro-mean-Y
57. mean-fBodyGyro-mean-Z
58. mean-fBodyGyro-std-X
59. mean-fBodyGyro-std-Y
60. mean-fBodyGyro-std-Z
61. mean-fBodyAccMag-mean
62. mean-fBodyAccMag-std
63. mean-fBodyBodyAccJerkMag-mean
64. mean-fBodyBodyAccJerkMag-std
65. mean-fBodyBodyGyroMag-mean
66. mean-fBodyBodyGyroMag-std
67. mean-fBodyBodyGyroJerkMag-mean
68. mean-fBodyBodyGyroJerkMag-std

Notes: 
======
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.

For more information about this dataset coheantact: activityrecognition@smartlab.ws

License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
