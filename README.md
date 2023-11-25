# School Performance Analysis Using Pandas

In a fictional universe, I am the new Chief Data Scientist for my city's school district. In this capacity, I will be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.

For my first project, I have been asked to analyze the district-wide standardized test results of 15 local schools. I have be given access to every student's math and reading scores on a recent competency assessment, as well as various information on the schools they attend. These data were given to me in two csv files. The first file ('starter-students-complete.csv') is a dataset that contains the names of every student, their ids, gender, grade, school they attended, reading score, and their math score. The second ('starter-schools-complete.csv') provides information on each school—the name of the school, school id, the school type (i.e., district or charter), size, and budget. My task is to aggregate the data to showcase obvious trends in school performance.

## Dataframe Merging
First, the two csv files were imported and merged into one pandas dataframe. We will use a 'left' merge because we want to match the values of the right dataframe (school_data) to the keys in the left dataframe (student_data).

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/91994bad-ccba-4d10-b0a9-5401013378ce)

**Figure 1.** *The process of merging the dataframes using pandas.*

___
## Basline Metrics
Next, we obtained metrics that summarized the district's performance in math and reading including the overall percentage of students passing math and reading. After gathering these metrics, we put it into a single pandas dataframe to give a snapshot of district performance.

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/c1bf4a61-66c7-4b03-a308-888b0661fbad)

**Figure 2.** *A snapshot of math and reading performance in the school district.*

___
## Individual School Performance
Third, we calculated each of the individual school's average scores and passing rates (defined as a score of 70 or higher) in the district to examine each school's performance more closely. After these data were calculated, they were put into a pandas dataframe to get side-by-side comparison of each school.

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/1f97e48d-9147-450a-a91d-652e1d29e7f9)

**Figure 3.** *A comparison of each school's average math score, reading score, math pass rate, reading pass rate, and overall pass rate.*

___
## Top and Bottom Performers
We also wanted to list the top and bottom performers for the district. To do this, we created a new pandas dataframe and sorted the values so that the top performing schools would be at the top, and the schools with the lowest pass rate would be at the bottom. We did the same for the schools with the lowest passing rate.

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/08601aeb-f03a-45f1-b532-7cbf4728eb19)

**Figure 4.** *Sorted dataframe displaying the top 5 and bottom 5 schools in the district.*

___
## Highest Subject Grades per School
To determine each school's highest performing grade and subject, we created a new pandas dataframe that grouped the average reading and math test scores by each grade (9th grade - 12th grade) for each school.

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/7a84d6ff-16a8-4f5f-8b90-63bb974cbb82)

**Figure 5.** *A breakdown of math performance for each grade per school.*

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/d1533e38-b2b5-4229-8c2f-4b7cdbeada1b)

**Figure 6.** *A breakdown of reading performance for each grade per school.*
___
## School Funding and Test Scores
School funding is also an important factor in test competency. We hypothesized that schools with the most funding would achieve higher test scores. We defined funding as the amount of money given to the schools to spend per student. This was determined by taking the amount of funding given to a school divided by their student count. For instance, Bailey High School has 4,976 students and an overall budget of $3,124,928, so their per student budget would be $628. To test our hypothesis, we created four separate bins to categorize each school based off of funding per student. Each school was categorized into one of the following bins: <$585 per student, $585-630 per student, $630-645 per student, $645-680 per student. We designed a side-by-side comparison of the average reading and math scores per budget category.

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/8c8cb700-d6a2-411b-8214-d852d3a1fe72)

**Figure 7.** *The bins used to determine funding categorization.*

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/f215b810-5cfb-46e9-b6af-043a6e013a13)

**Figure 8.** *A side-by-side comparison of the funding categories and performance.*

___
## School Size and Test Scores
We also wanted to examine school size and its effect on school performance. Similar to school funding, we binned the schools based on their size. The bins were as follows: Small (<1000 students), Medium (1000-2000 students), Large (2000-5000 students). We created a dataframe to examine the relationship between school size and test performance. 

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/f48fd38e-49c6-4e1b-986e-67496ee7c045)

**Figure 9.** *The bins used to determine size categorization.*

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/0a807d2a-8123-4def-9dd2-52e8f2c29266)

**Figure 10.** *Dataframe comparing the size categories and performance.*

___
## District and Charter School Performance
Lastly, to evaluate the difference between test scores and school type (i.e., distric or charter), we made another pandas dataframe that showed the average test performance grouped by school type. 

![image](https://github.com/nicholaishaw/pandas-challenge/assets/135463220/def57f34-2ec4-476c-aa16-71522b609681)

**Figure 11.** *Dataframe the type of school and performance.*

## Analysis
The data revealed that the top five highest performing schools were Cabrera High School, Thomas High School, Griffin High School, Wilson High School, and Pena High School with overall passing rates of 90.5% or higher. The five lowest performing schools were Rodriguez High School, Figueroa High School, Huang High School, Hernandez High School, Johnson High School.

Comparisons between test performance and size, funding, and school type revealed that schools with the lowest funding performed better on the standardized testing for math and reading. After data were grouped into separate bins based on size, we discovered that schools with the medium sizes possessed the best test results, followed by the smallest schools, and then finally the large schools with an overall passing rate of 58.2%. Finally, the results also showed that charter schools had the highest average scores with a passing rate of 90.4%.
