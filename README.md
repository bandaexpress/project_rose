# project_rose
Project 1 from Columbia University Data Analytics Bootcamp

# Research Statement

The goal of our project is to examine 2021 US birth rate data for patterns in healthcare outcomes based on payment sources at delivery.

# Hypothesis

There is a positive correlation between birth rate data and payment sources at delivery in regards to various healthcare outcomes. 

# Research Questions
1. Does the use of private insurance typically leads to better care and/or resources?
2. How do the different payment sources influence birth outcomes, like the health of the baby born?
3. 

# Libraries
- [Pandas](https://pandas.pydata.org/) - Data analysis and manipulation.
- [Matplotlib](https://matplotlib.org/) - Creates data visualizations.
- [SciPy](https://scipy.org/) - Used for scientific and technical computing.
- [NumPy](https://numpy.org/) - Provides numerical computations.
- [Requests](https://pypi.org/project/requests/) - Used for making HTTP requests in Python.
- [JSON](https://www.json.org/json-en.html) - Used to encode Python objects into JSON format.
- [Seaborn](https://seaborn.pydata.org/) - For  statistical graphics. 

# Data
1. The data is available from the [National Center for Health Statistics](https://www.cdc.gov/nchs/data_access/vitalstatsonline.htm) for the year 2021.
2. The compressed files are over 200+ mb (uncompressed 4.6 GB) and are in text file format.
3. The txt files were examined in Excel's power query editor to extract a sample file size small enough to upload to GitHub (50 mb). Depicted in image 1 below. 
4. The output is a csv file with 100,000 rows. Each row contains Birth Rate Data for a single birth within the 2021 timeframe. Depicted in image 2 below. 
5. Once the data has been read into the jupyter notebook, there is additional data cleaning to rename column and row variables per inputs based on [NCHS documenation](https://ftp.cdc.gov/pub/Health_Statistics/NCHS/Dataset_Documentation/DVS/natality/UserGuide2021.pdf), filter out unknown/not stated values, and convert metric values to imperial for readability. Depicted in image 3 below. 

Image 1: Excel output
<img width="1233" alt="Screenshot 2023-12-18 at 4 34 11 PM" src="https://github.com/bandaexpress/project_rose/assets/146903245/25080a9f-744e-465b-a007-02e81d8cdfff">

Image 2: Full dataframe from CSV file 
<img width="992" alt="Screenshot 2023-12-17 at 9 50 24 PM" src="https://github.com/bandaexpress/project_rose/assets/146903245/0d429a5b-30bc-431f-bf6f-0422995a3851">

Image 3: Cleaned dataframe using techniques described above. 
<img width="990" alt="Screenshot 2023-12-18 at 4 31 14 PM" src="https://github.com/bandaexpress/project_rose/assets/146903245/1d4c2bc9-6225-4e59-8084-6786fe810846">


The columns of data extracted from the txt file are:
1. Birth Year
2. Birth Month
3. Birth Place
4. Mother's Age
5. Month Prenatal Care Began (+ grouped)
6. Number of Prenatal Visits (+ grouped)
7. WIC
8. Payment Source
9. Mother's Age
10. Mother's BMI
11. Living Children
12. Deceased Children
13. Used Anesthesia
14. Attendant at Birth
15. Intensive Care Admission
16. NICU Admission
17. Birth Weight (lbs)

# Analysis 
In fig 1: Mother Age vs Payment we can see that younger mothers come surprisingly from military personnel type of coverage.

![mother_age_vs_payment_source](https://github.com/bandaexpress/project_rose/assets/146903245/f464bf88-6434-402a-8052-a51f9db1844a)

Fig 2: Percentage of Low Weight Babies across Payment Source breaks down and shows how people with government support have higher chances of having a lower than healthy baby.
![percentage_low_weight_pie_chart](https://github.com/bandaexpress/project_rose/assets/146903245/58484b37-a8cf-41de-b35f-1994b097a974)

Fig 3: Percentage of High Weight Babies across Payment Source shows that surprisingly natives have higher rate of overweight babies, with military personnel following.
![percentage_high_weight_pie_chart](https://github.com/bandaexpress/project_rose/assets/146903245/3ae4d0a4-c55c-4f38-96f0-52befdced120)

Finally, fig 4: Percentage of Low/High Weight Babies based on Number of Living Children breaks down higher and lower weight of babies based on the number of children the mother had, the more risk she has of having an underweight baby, but that is also because the women are older on average by the third child so that has the risks associated accordingly. However, it is worth noting that for the first child there seem to also be a higher rate of low weight births.
![living_children_vs_weight_category_percentage_chart](https://github.com/bandaexpress/project_rose/assets/146903245/3a0477f4-52f9-4392-a9bf-4d67f6852f68)

# Conclusion
Based on our analysis, we can reasonably conclude that there is a positive correlation between birth rate data and payment sources at delivery in regards to various healthcare outcomes. 

While the differences between private insurance and government funded insurance (Medicare) aren't vastly different, there is still a statistically significant enough difference between the health of the babies born, and hospital resources afforded to the mother.   

We believe our analysis would be a good stepping stone for further studies to explore additonal factors such as racial inequalities in healthcare, and broader US economic connections. 

# Requirements
## Completed Analysis Uploaded to GitHub (20 points)
1. Final data analysis contains ample and complete information in README file (10 points)
2. Final repository is acceptable for professional quality presentation (10 points)

## Visualizations (20 points)
1. 6–8 visualizations of data (at least two per question) (10 points)
2. Clear and accurate labeling of images (5 points)
3. Visualizations supported with ample and precise explanation (5 points)

## Analysis and Conclusion (20 points)
1. Write-up summarizes major findings and implications at a professional level (5 points)
2. Each question in the project proposal is answered with precise descriptions and findings (5 points)
3. Findings are strongly supported with numbers and visualizations (5 points)
4. Each question response is supported with a well-discerned statistical analysis from lessons (e.g., aggregation, correlation, comparison, summary statistics, sentiment analysis, and time series analysis) (5 points)

## Group Presentation (20 points)
1. All group members spoke during the presentation (5 points)
2. Group was well prepared (5 points)
3. Presentation is relevant to material (5 points)
4. Presentation maintains audience interest (5 points)

## Slide Deck (20 points)
1. Slides are visually clean and professional (5 points)
2. Slides are relevant to material (5 points)
3. Slides effectively demonstrate the project (5 points)
4. Slides are clear and maintain audience interest (5 points)

# Contributors
[Anthony Banda](https://github.com/bandaexpress), [Emily Sims](https://github.com/emilys28), [Daniel Kenet](https://github.com/dkenet), [Jarret Baum](https://github.com/jarretbaum)
