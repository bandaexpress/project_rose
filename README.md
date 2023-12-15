# project_rose
Project 1 from Columbia University Data Analytics Bootcamp

# Libraries
- [Pandas](https://pandas.pydata.org/) - Data analysis and manipulation.
- [Matplotlib](https://matplotlib.org/) - Creates data visualizations.
- [SciPy](https://scipy.org/) - Used for scientific and technical computing.
- [NumPy](https://numpy.org/) - Provides numerical computations.
- [Requests](https://pypi.org/project/requests/) - Used for making HTTP requests in Python.
- [JSON](https://www.json.org/json-en.html) - Used to encode Python objects into JSON format.

# Data
1. The data is available from the [National Center for Health Statistics](https://www.cdc.gov/nchs/data_access/vitalstatsonline.htm) for the year 2021.
2. The compressed files are over 200+ mb (uncompressed 4.6 GB) and are in text file format.
3. The txt files were examined in Excel's power query editor to extract a sample file size small enough to upload to GitHub (50 mb).
4. The output is a csv file with 100,000 rows. Each row contains Birth Rate Data for a single birth within the 2021 timeframe.
5. Once the data has been read into the jupyter notebook there is additional data cleaning to rename column and row variables per inputs based on [NCHS documenation](https://ftp.cdc.gov/pub/Health_Statistics/NCHS/Dataset_Documentation/DVS/natality/UserGuide2021.pdf) and convert metric values to imperial for readability.

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
TBD

# Contributors
[Anthony Banda](https://github.com/bandaexpress), [Emily Sims](https://github.com/emilys28), [Daniel Kenet](https://github.com/dkenet), [Jarret Baum](https://github.com/jarretbaum)
