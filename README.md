Getting-and-Cleaning-Data
=========================

+ Steps for run_analysis.R in Getting and Cleaning Data Coursera Project:
1. Download and unzip files to your working directory from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
2. Rename folder name from "getdata-projectfiles-UCI HAR Dataset" to "data"
3. Source("run_analysis.R")
4. run_analysis() will create two text files in the working directory. 
<br>  merged_data.txt
<br>  data_with_means.txt
5. Use read.table function to read data into R 
<br>    data <- read.table("data_with_means.txt") 
<br>    Data has averages for each of the 6 activites and 30 subjects.
