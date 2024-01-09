## Overview
The goal of this project was to examine fitness tracker data to draw  conclusions about the trackers and the physical characteristics and activity of the participants. The datasets were found on kaggle.com  (see 'References section'). The Fitbit and Apple Watch dataset was a record of 49 participants by fitness tracker type, heart rate, activity level, etc. over a 65 minute period. The data was collected and stored in .csv files. The data that was only Fitbit data was collected from 30 people over two months and includes a variety of features including, BMI, sleep, calories burned, etc. in the form of .csv files. For this project, we focused on the files that covered participants' heartrate, intensity of activity, amount of sleep, BMI (body mass index), and activity level. 

## The questions that we wanted to answer based on the data that we had available to us were:
1.) How do Apple watches vs. Fitbits compare when taking heart rate data?
2.) How does the activity level correlate to average heart rate?
3.) How does the amount of sleep affect Body Mass Index (BMI)
4.) How does the activity level affect number of calories burned?

## Data Analysis & Conclusions:
### How do Apple watches vs. Fitbits compare when taking heart rate data?

The devices used in the Apple Watch – Fit data were the Fitbit Charge HR 2 and the Apple Watch Series 2. <br>
#### Terminology <br>
METs – Metabolic Equivalents, are a simple way to measure the energy cost of physical activities. For example, sitting only uses 1 MET. <br>
Resting heart rate - your heart rate when your body is at rest. <br>
Normal heart rate - number of times your heart beats per minute <br>
Activities used for this project were Running 3, 5, 7 METS and self paced walking <br>
New question: <br>
Were there significant differences in the measurement of resting heart rates based on activity and device. <br>
Hypothesis: The Apple Watch records a higher resting heart rate than the Fitbit device. <br>
Statistical test: T-Test(independent) <br>
Results: <br>
Here are the p-values results between the two devices on resting heart rate: <br>
Activity p-value <br>
   Self-Pace walking: 0.00013644418747026964 <br>
   Running 7METs: 3.473589188909155e-08 <br>
   Running 5METs: 0.0008572713151761626 <br>
   Running 3 METs: 0.09087616379978523 <br>
  
Conclusions:
There were no significant differences with the between the Apple Watch and Fitbit in recording the resting heart rate.

### How does the activity level correlate to average heart rate?

To compare how the participants' average heart rate compares to their overall activity level we used the files 'heartrate_seconds_merged.csv' and 'dailyIntensities_merged.csv' and merged them by the participant ID. A summary table was then created using the data to show the average heart rate and number of minutes at each activity level over the course of data collection for each individual participant. This means that each participant has a single entry for average heart rate and each activity level. 

Plotting all of the activity data together was not the most helpful as there was too much going on in the graph to draw any conclusions. We can tell from the pie chart that is included with this portion of the project that participants on average spent 81.6% of their time sedentary. Since being sedentary was the most prolific activity people engaged in, we graphed the sedentary minutes vs. the heart rate in a scatter plot and added a linear regression line to see if there are any trends.

From the linear regression and a Pearson's r test resulting in a value of approximately 0.40, we can see that there is a moderate positive correlation between amount of time spent sedentary and the participant's average heartrate. 

The conclusion for this question was that the more minutes an individual spends sedentary, the higher their average heartrate is. It is important to note that this is a small pool of participants, so a larger dataset/datasets would be necessary to draw more complete conclusions. 

### How does the amount of sleep affect Body Mass Index (BMI)?

To compare how BMI is affected by the amount of sleep a person gets, we used the files 'sleepDay_merged.csv' and 'weightLogInfo_merged.csv'. From these .csv files, we focused on the columns BMI and HoursSleep and merged them on the participant ID column that was present in each .csv file. The average BMI and amount of sleep per participant over the entire length of data collection was then calculated.

The average BMI was then plotted against the average amound of sleep in hours in a scatter plot, and a linear regression was generated from the points. The Pearson's r for the points was approximately 0.814 which indicates a strong correlation between BMI and amount of sleep. 

It is important to note that the dataset used to answer this question is very limited; there were only 7 participants in the data who contributed both BMI and sleep data. With so little data, it is hard to determine potential outliers, and the conclusion for the data cannot be conclusive. 

The conclusion that we can draw from this dataset is that people who get more sleep tend to have a higher BMI, but analysis of a larger dataset/datasets would be necessary to prove/disprove this conclusion. 

### How does the activity level affect number of calories burned?


## References:
Link to Fitbit & Apple Watch data:
https://www.kaggle.com/datasets/aleespinosa/apple-watch-and-fitbit-data/discussion/370036

Link to Fitbit data:
https://www.kaggle.com/datasets/arashnic/fitbit?resource=download