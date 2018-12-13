# Getting and Cleaning Data-Course Project 

This project was completed as required for Coursera's Getting and Cleaning Data's course project. The data used was obtained from the "Human Activity Recognition Using Smartphones Dataset". 

The dataset includes data acquired from 30 subjects, with 21 of those subjects selected for the training condition, and the remaining 8 subjects selected for the test condition. Participants in both conditions wore a Samsung Galaxy S II on their waist while performing 6 activities: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING. The records within y_train.txt and y_test.txt contain the values of the activities conducted, with activity_label denoting which value corresponds to what action. 

The records within x_test & x_train include the values acquired from the sensor signals. From the dataset's readme, it specifically contains the following: 
	"Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
	Triaxial Angular velocity from the gyroscope. 
	A 561-feature vector with time and frequency domain variables."
The fields within x_test & x_train correspond to the measurements outlined in features_info.txt. They are: 
*"tBodyAcc-XYZ 
*tGravityAcc-XYZ
*tBodyAccJerk-XYZ
*tBodyGyro-XYZ
*tBodyGyroJerk-XYZ
*tBodyAccMag
	tGravityAccMag
	tBodyAccJerkMag
	tBodyGyroMag
	tBodyGyroJerkMag
	fBodyAcc-XYZ
	fBodyAccJerk-XYZ
	fBodyGyro-XYZ
	fBodyAccMag
	fBodyAccJerkMag
	fBodyGyroMag
	fBodyGyroJerkMag
	gravityMean
	tBodyAccMean
	tBodyAccJerkMean
	tBodyGyroMean
	tBodyGyroJerkMean"
each with the following submeasurements: 
	"mean(): Mean value
	std(): Standard deviation
	mad(): Median absolute deviation 
	max(): Largest value in array
	min(): Smallest value in array
	sma(): Signal magnitude area
	energy(): Energy measure. Sum of the squares divided by the number of values. 
	iqr(): Interquartile range 
	entropy(): Signal entropy
	arCoeff(): Autorregresion coefficients with Burg order equal to 4
	correlation(): correlation coefficient between two signals
	maxInds(): index of the frequency component with largest magnitude
	meanFreq(): Weighted average of the frequency components to obtain a mean frequency
	skewness(): skewness of the frequency domain signal 
	kurtosis(): kurtosis of the frequency domain signal 
	bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
	angle(): Angle between to vectors."

Subject_train & subject_test contains the participant number that did the action for both sets. 

The overall purpose of this project was to produce a tidy dataset that included one activity per subject, along with the mean and standards deviations of their measurements. In order to do so, all the aforementioned files were combined into one dataframe, then narrowed down to include the measurements that only contained the mean and standard deviations, then further grouped by subjects and activity labels, to produce a final table with 180 observations of 89 variables. 


