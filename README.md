# project_rose
Project 1 from Columbia University Data Analytics Bootcamp

# Research Statement

The goal of our project is to examine 2021 US birth rate data for patterns in healthcare outcomes based on payment sources at delivery.

# Hypothesis

There is a positive correlation between birth rate data and payment sources at delivery in regards to various healthcare outcomes. 

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

# Requirements
## Completed Analysis Uploaded to GitHub (20 points)
Final data analysis contains ample and complete information in README file (10 points)
Final repository is acceptable for professional quality presentation (10 points)

## Visualizations (20 points)
6–8 visualizations of data (at least two per question) (10 points)
Clear and accurate labeling of images (5 points)
Visualizations supported with ample and precise explanation (5 points)

## Analysis and Conclusion (20 points)
Write-up summarizes major findings and implications at a professional level (5 points)
Each question in the project proposal is answered with precise descriptions and findings (5 points)
Findings are strongly supported with numbers and visualizations (5 points)
Each question response is supported with a well-discerned statistical analysis from lessons (e.g., aggregation, correlation, comparison, summary statistics, sentiment analysis, and time series analysis) (5 points)

## Group Presentation (20 points)
All group members spoke during the presentation (5 points)
Group was well prepared (5 points)
Presentation is relevant to material (5 points)
Presentation maintains audience interest (5 points)

## Slide Deck (20 points)
Slides are visually clean and professional (5 points)
Slides are relevant to material (5 points)
Slides effectively demonstrate the project (5 points)
Slides are clear and maintain audience interest (5 points)

# Contributors
[Anthony Banda](https://github.com/bandaexpress), [Emily Sims](https://github.com/emilys28), [Daniel Kenet](https://github.com/dkenet), [Jarret Baum](https://github.com/jarretbaum)
