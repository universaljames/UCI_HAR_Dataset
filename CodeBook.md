The following steps which required by the course will be done with run_analysis.R

1. Merges the training and the test sets to create one data set.
After download the dataset, it will be extracted under UCI_HAR_Dataset. each data will be assign to the variable with the same name.
x_train and x_test will be merged by the function rbind() to x, as same as y and Subject.
X, y, Subject will be merged to Merged_Data by cbind().

2. Extracts only the measurements on the mean and standard deviation for each measurement.
Collumn subject, code, mean and std will be selected from Merged_data to create TidyData.

3. Uses descriptive activity names to name the activities in the data set
In TidyData, the code column will be taken from the second column of the activities.

4. Appropriately labels the data set with descriptive variable names.
Replace code to activities.
Replace Acc to Accelerometer.
Replace Gyro to Gyroscope.
Replace BodyBody to Body
Replace Mag to Magnitude.
Replace f* to Frequency.
Replace t* to Time.

5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
FinalData will be created from TidyData with the average of each variable for each activity and each subject. And also output a txtfile with the name FinalData.txt from FinalData.
