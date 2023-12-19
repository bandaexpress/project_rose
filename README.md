# project_rose
Project 1 from Columbia University Data Analytics Bootcamp

# Research Statement

The goal of our project is to examine 2021 US birth rate data for patterns in healthcare outcomes based on payment sources at delivery.

# Hypothesis

There is a positive correlation between birth rate data and payment sources at delivery in regards to various healthcare outcomes. 

# Research Questions
1. Does the use of private insurance typically leads to better care and/or resources?
2. How do the different payment sources influence birth outcomes, like the health of the baby born?
3. How common is each source of payment used when Infertility Treatment is necessary?

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
## Resources Analysis: 
First, our group our created Figure 1: Bar Graph of WIC Counts for Each Payment Source to count all Women, Infant, and Children (WIC) per Payment Source to examine utilization by payment source. The correlation coefficient between Payment Source and WIC is approximately -0.47, indicating a moderate negative correlation. This suggests that as one variable increases, the other tends to decrease.The p-value is very close to zero (0.0), which means that the observed correlation is statistically significant.

![wic_payment_source_bar_graph](https://github.com/bandaexpress/project_rose/assets/146903245/f0e43f80-3b8f-41fd-922c-cd82c35962e4)



We decided to look further into the Attendant at Birth column. We theorized that those with private insurance would be more likley to have a Doctor of Medicne (MD), Doctor of Osteopathy, or Licensed Midwife/  as the attedning physician vs those with Medicare. As Medicare patients may end up with the less certifed physicians. We conducted a Chi Squared test to to examine if there is a significant association between Attendent at Birth and Payment Sources. The p-value was extremely close to zero, signifying these variables are closely correlated. Fig 2 demonstrates that those with private insurance are more likely to have a Doctor of Medicine. 

![attending_payment](https://github.com/bandaexpress/project_rose/assets/146903245/0717361d-a2ce-41eb-adfa-fa02092d6e78)

Another resource we explored was the use of anesthesia- believing that those with private insurance would have a higher access and use of anesthesia vs Medicaid patients. Figure 3: Comparison of Anesthesia and Payment Source illustrates that those with private insurance are in fact more likely to use anesthesia during child birth. The p-value was zero, showing that anesthesia and payment source are also closely correlated. 
![anesthesia_payment](https://github.com/bandaexpress/project_rose/assets/146903245/e90d1217-3fee-44d4-98e8-1c2ef97ac0cf)


## Baby Health Analysis:  
In Fig 4: Mother Age vs Payment we can see that younger mothers come surprisingly from military personnel type of coverage.

![mother_age_vs_payment_source](https://github.com/bandaexpress/project_rose/assets/146903245/f464bf88-6434-402a-8052-a51f9db1844a)

Fig 5: Percentage of Low Weight Babies across Payment Source breaks down and shows how people with government support have higher chances of having a lower than healthy baby.
![percentage_low_weight_pie_chart](https://github.com/bandaexpress/project_rose/assets/146903245/58484b37-a8cf-41de-b35f-1994b097a974)

Fig 6: Percentage of High Weight Babies across Payment Source shows that surprisingly natives have higher rate of overweight babies, with military personnel following.
![percentage_high_weight_pie_chart](https://github.com/bandaexpress/project_rose/assets/146903245/3ae4d0a4-c55c-4f38-96f0-52befdced120)

In Fig 7: Percentage of Low/High Weight Babies based on Number of Living Children breaks down higher and lower weight of babies based on the number of children the mother had, the more risk she has of having an underweight baby, but that is also because the women are older on average by the third child so that has the risks associated accordingly. However, it is worth noting that for the first child there seem to also be a higher rate of low weight births.
![living_children_vs_weight_category_percentage_chart](https://github.com/bandaexpress/project_rose/assets/146903245/3a0477f4-52f9-4392-a9bf-4d67f6852f68)

Additonally, we explored the babies' weight based on the different payment source options. A box plot enables us to visually understand how they compare to one another. Based on Fig 8: Relationship between Payment Source and Birth Weight, we can see that there is a slight increase in weight for babies' born with private insurance vs Medicaid. 
![weight_payment](https://github.com/bandaexpress/project_rose/assets/146903245/ca7f598b-ee3c-495a-aacc-8260991bc071)

## Infertility Treatment Analysis
The primary objective here was to understand the financial avenues chosen by individuals seeking assistance with infertility. Notably, 'Private Insurance' emerges prominently, suggesting a prevalent reliance on this avenue. 
Fig 9: Infertility Treatment by Payment Source
![InfertilityTreatmentbyPaymentSource](https://github.com/bandaexpress/project_rose/assets/146903245/1eba3893-7bd9-4b44-ba93-a78410e44d50)

This insight unveils the substantial role of private insurance in supporting individuals through their infertility journeys. It's not just a financial choice; it reflects the intricate intersection of healthcare and personal paths to parenthood.
Figure 10: Fertility Enhancing Drugs by Payment Source
![FertilityEnhancingDrugsbyPaymentSource](https://github.com/bandaexpress/project_rose/assets/146903245/a08daba9-cc07-4193-b017-c032e771b2bc)

Delving deeper into our data, a trend emerges. While exploring Infertility Treatment options, it's intriguing to note that slightly more individuals leaned towards 'Fertility Enhancing Drugs' compared to 'Assisted Reproductive Technology.'
Figure 11: Asst. Reproductive Technology by Payment Source
![AsstReproductiveTechnologybyPaymentSource](https://github.com/bandaexpress/project_rose/assets/146903245/cd6e0334-50cf-49d1-875d-e33dacbfdd2a)


# Conclusion
Based on our analysis, we can reasonably conclude that there is a positive correlation between birth rate data and payment sources at delivery in regards to various healthcare outcomes. 

While the differences between private insurance and government funded insurance (Medicare) aren't vastly different, there is still a statistically significant enough difference between the health of the babies born, and hospital resources afforded to the mother.  

Private Insurance overwhelmingly serves as the primary payment method for births requiring infertility treatment, highlighting its pivotal role in reproductive healthcare. This emphasizes the need for future studies exploring broader implications and inequalities within the US healthcare system.

We believe our analysis would be a good stepping stone for further studies to explore additional factors such as racial inequalities in healthcare, broader US economic connections, and resource inequalities based on race. 

# Presentation Link
https://docs.google.com/presentation/d/1N1s349-hj3Yi8iv_RMOcmPwwKKIq1DzLiIXdc5KCQ0w/edit?usp=sharing

# References
1. Centers for Disease Control and Prevention. (2022). Birth Data Files. Vital Statistics Online.  https://www.cdc.gov/nchs/data_access/vitalstatsonline.htm
2. WHO: https://www.medicalnewstoday.com/articles/325630#average-weights
3. https://stackoverflow.com/questions/986006/how-do-i-pass-a-variable-by-reference/986145#986145
4. https://stackoverflow.com/questions/7505775/python-remove-rows-based-on-lack-of-character
5. https://stackoverflow.com/questions/14446511/most-efficient-method-to-groupby-on-an-array-of-objects
6. https://stackoverflow.com/questions/14262433/large-data-workflows-using-pandas
7. https://stackoverflow.com/questions/44339824/capture-nested-exceptions-in-python

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
