# School Performance Analysis Using Pandas

In a fictional universe, I am the new Chief Data Scientist for my city's school district. In this capacity, I will be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.

For my first project, I have been asked to analyze the district-wide standardized test results of 15 local schools. I have be given access to every student's math and reading scores on a recent competency assessment, as well as various information on the schools they attend. These data were given to me in two csv files. The first file ('starter-students-complete.csv') is a dataset that contains the names of every student, their ids, gender, grade, school they attended, reading score, and their math score. The second ('starter-schools-complete.csv') provides information on each school—the name of the school, school id, the school type (i.e., district or charter), size, and budget. My task is to aggregate the data to showcase obvious trends in school performance.

## Dataset Manipulation
First, the two csv files were imported and merged into one pandas dataframe.
![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/91994bad-ccba-4d10-b0a9-5401013378ce)

**Figure 1.** *The process of merging the dataframes using pandas.*

___
Next, we obtained metrics that summarized the district's performance in math and reading including the overall percentage of students passing math and reading. After gathering these metrics, we put it into a single pandas dataframe to give a snapshot of district performance.
![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/c1bf4a61-66c7-4b03-a308-888b0661fbad)

**Figure 2.** *A snapshot of math and reading performance in the school district.*

___
Third, we calculated each of the individual school's average scores and passing rates (defined as a score of 70 or higher) in the district to examine each school's performance more closely. After these data were calculated, they were put into a pandas dataframe to get side-by-side comparison of each school.
![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/1f97e48d-9147-450a-a91d-652e1d29e7f9)

**Figure 3.** *A comparison of each school's average math score, reading score, math pass rate, reading pass rate, and overall pass rate.*

___
We also wanted to list the top and bottom performers for the district. To do this, we created a new pandas dataframe and sorted the values so that the top performing schools would be at the top, and the schools with the lowest pass rate would be at the bottom. We did the same for the schools with the lowest passing rate.
![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/08601aeb-f03a-45f1-b532-7cbf4728eb19)

**Figure 4.** *Sorted dataframe displaying the top 5 and bottom 5 schools in the district.*
