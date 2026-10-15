# Assignment_3
Healthcare_ DataAnalysis_and_Insights
1)	Check for the number of missing values marked with '?' in each column of the “Medical Examinations” Table and "Hospitalization Details" Table. 
The number of missing values was found using a Countifs function; =countifs(criteria range).

2)	Fill in the missing values of ‘month’ with Sep and ‘year’ with its average rounded to the nearest integer. 
The missing values of ‘month’ with Sep using  excel find & replace function.
The missing values of ‘Year’ with Average of cell using formula”=Average(number range)”; and then replaced the value by excel find & replace function.

4) Determine the most frequently occurring values in the ‘smoker’, 'Hospital tier' and 'City tier' columns, and fill in the missing values accordingly. 
The most frequently occurring values in the ‘smoker’ found by =COUNTIFS(criteria range,"Yes")  and then compared using conditional formatting tool Data Bar. The greater one where replaced by replace function.

the most frequently occurring values 'Hospital tier' and 'City tier' columns, found by =COUNTIFS(criteria range,"tier - 1")  and then compared using conditional formatting tool Data Bar. The greater one where replaced by replace function.

4) If any 'State ID' values are missing, consider filling them with 'Unknown' or using another appropriate strategy. 
The missing values of State ID with Unknown using  excel find & replace function.
-------------------------------------------------------------------------------------------------------
Data Transformation: (8 marks) 
1) Split the ‘names’ column in the “Customer Names” Table into 3 meaningful columns: ‘Title’, ‘First Name’, and ‘Last Name’. 
The name columns splited into 3 columns using excel- Data- Text to Column function- delimitor option and then =TRIM(SUBSTITUTE(D2,".","")) used for removing the inconsistency in last name column.
2) Convert the "NumberOfMajorSurgeries" column in the “Medical Examinations” Table to numerical data by replacing non-numeric characters with meaningful numerical values. 
In "NumberOfMajorSurgeries" the non-numeric characters were replaced 'No major surgery' with “0” using excel find & replace function;  retained numeric counts 1, 2, and 3 as numbers.

3) Check for inconsistencies in the 'Heart Issues' and 'smoker' columns and propose corrective actions if necessary. 
inconsistencies in the 'Heart Issues' and 'smoker' columns were capitalized using “=PROPER(cell range)” and then replaced with “Unknown”using excel find & replace function.

4) Create a new column named “Weight Status” that categorizes BMI into different categories as below: BMI Weight Status Below 18.5 Underweight 18.5 – 24.9 Normal Weight 25.0 – 29.9 Overweight 30.0 and Above Obesity .
Create a new column named “Weight Status” by inserting new column option in excel & then used ‘=IF(B3<=18.5,"Under Weight",IF(B3<=24.9,"Normal Weight",IF(B3<=29.9,"Over Weight","Obesity")))” formula to categoring.

5) Create a new column named “Diabetes Status” and fill it as per the information given below: HbA1C Diabetes Status Below 5.7 Normal 5.7 – 6.4 Prediabetes 6.5 and Above Diabetes 
Create a new column named “Diabetes Status” by inserting new column option in excel & then used =IF(E4<=5.7,"Normal",IF(E4<=6.4,"Prediabetes","Diabetes"))” formula to categoring.

6) Merge ‘year’, ‘month’ and ‘date’ columns in the “Hospitalization Details” Table into one column named ‘Date of Birth’ and format it in ‘DD-MMM-YYYY’ custom format. 
For merging  ‘year’, ‘month’ and ‘date’ columns used =D2&"-"&C2&"-"&B2 formula in excel.
7) Calculate the ‘Age’ of each customer based on their ‘Date of Birth’ and the date of collection of the dataset, which is 8 th June 2023. 
Age of customer based on DoB and 8 th June 2023 by setting formula “(=DATEDIF(E3,DATE(2023,6,8),"y")&" "&"Years")”.
8) Format ‘charges’ column as currency ($). 
currency ($) imputed in charge column by applying  excel custom currency function.
----------------------------------------------------------------------------------------------------------------

Data Exploration, Analysis & Visualization: (12 marks)
 ➢ Create a new sheet named “Healthcare", combine all three tables into one, using Customer ID as the common column, utilizing VLOOKUP. . 
➢ Retain the following necessary columns: Customer ID, First Name, BMI, HBA1C, Heart Issues, Any Transplants, Cancer history, NumberOfMajorSurgeries, smoker, Weight Status, Diabetes Status, Date of Birth, charges, Hospital tier, City tier, State ID, Age. 
Step 1: Created new sheet by clickind new tab and then renamed as Healthcare.
Step 2: Created all necessary column name for vlookup the data from 3 sheets.
Step 3: Applied the function =VLOOKUP(lookup_value, table_array, col_index_num, 0) to each rows accordingly from source data ranges.

Create pivot tables if required to do the following analysis, then visualize through charts: Analysis using Pie/Donut Chart:
➢ What is the distribution of cancer history among smokers and non-smokers?
Opened Healthcare.xlsx workbook. Select Insert → PivotTable → New Worksheet → OK for pivot the table and plotted all the values in Value Field Settings field. Then selected the pivot table and selected Pie chart option from Insert tab to comparing.

 ➢ How does the total number of major surgeries and average HbA1C differ between patients with and without a history of transplants?
Select Insert → PivotTable → Same Healthcare worksheet→ OK for pivot the table and plotted all the values in Value Field Settings field. Then selected the pivot table and selected Donut chart option from Insert tab to comparing.

 Analysis using Column/Bar Chart:
 ➢ How do healthcare charges vary based on different weight statuses and diabetes statuses? 
Select Insert → PivotTable → Same Healthcare worksheet → OK for pivot the table and plotted all the values in Value Field Settings field. Then selected the pivot table and selected Column chart option from Insert tab to comparing.

➢ Can you compare the average charges for each hospital tier within different states? 
Select Insert → PivotTable → Same Healthcare worksheet → OK for pivot the table and plotted all the values in Value Field Settings field. Then selected the pivot table and selected Bar chart option from Insert tab to comparing.

Analysis using Line/Scatter Plot: 
➢ Is there any correlation between age and both BMI and HbA1C in the dataset? 
Select Insert → PivotTable → Same Healthcare worksheet → OK for pivot the table and plotted all the values in Value Field Settings field. Then selected the pivot table and selected Line chart option from Insert tab to comparing.

➢ Explore the relationship between age and healthcare charges. 
Select Insert → PivotTable → Same Healthcare worksheet → OK for pivot the table and plotted all the values in Value Field Settings field. Then selected the pivot table and selected Scatter Plot chart option from Insert tab to comparing.

Dashboard Creation: 
➢ Build an interactive dashboard that consolidates all key insights using the above visualizations. Ensure visual clarity and ease of interpretation for all chart types. 

Step 1: Create a dashboard worksheet by adding a new worksheet and rename it as Dashboard.
Step 2: Typed the heading Healthcare Dashboard.
Step 3: Used a blue coloured background for selected background., 
Step 4: Created KPIs using text column and shapes options and imputed all the necessary values from pivot table.
Step 5: Also moved all charts onto this worksheet from pivot table.

➢ Add slicers for the fields “Weight Status” and “Diabetes Status” to enable filtering across all visualizations, supporting comparison of health outcomes and charges based on body weight and diabetes condition.
Step 1: Selected one chart and then to Insert Slicer from PivotTable Analyze and check weight satus/diabetes status and then ok
Step 2: Right click the Slicer and then selected Report Connections and then  tick the check box of all charts.

