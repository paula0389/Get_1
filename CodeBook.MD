+## Getting and Cleaning Data Project  
 2  +  
 3  +Heather Wade  
 4  +  
 5  +### Description  
 6  +Additional information about the variables, data and transformations used in the course project for the Johns Hopkins Getting and Cleaning Data course.  
 7  +  
 8  +### Source Data  
 9  +A full description of the data used in this project can be found at [The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)  
 10  +  
 11  +[The source data for this project can be found here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)  
 12  +  
 13  +### Data Set Information  
 14  +The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.   
 15  +  
 16  +The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.  
 17  +  
 18  +### Attribute Information  
 19  +For each record in the dataset it is provided:   
 20  +- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.   
 21  +- Triaxial Angular velocity from the gyroscope.   
 22  +- A 561-feature vector with time and frequency domain variables.   
 23  +- Its activity label.   
 24  +- An identifier of the subject who carried out the experiment.  
 25  +  
 26  +### Section 1. Merge the training and the test sets to create one data set.  
 27  +After setting the source directory for the files, read into tables the data located in  
 28  +- features.txt  
 29  +- activity_labels.txt  
 30  +- subject_train.txt  
 31  +- x_train.txt  
 32  +- y_train.txt  
 33  +- subject_test.txt  
 34  +- x_test.txt  
 35  +- y_test.txt  
 36  +  
 37  +Assign column names and merge to create one data set.  
 38  +  
 39  +## Section 2. Extract only the measurements on the mean and standard deviation for each measurement.   
 40  +Create a logcal vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others.  
 41  +Subset this data to keep only the necessary columns.  
 42  +  
 43  +## Section 3. Use descriptive activity names to name the activities in the data set  
 44  +Merge data subset with the activityType table to cinlude the descriptive activity names  
 45  +  
 46  +## Section 4. Appropriately label the data set with descriptive activity names.  
 47  +Use gsub function for pattern replacement to clean up the data labels.  
 48  +  
 49  +## Section 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject.   
 50  +Per the project instructions, we need to produce only a data set with the average of each veriable for each activity and subject  
