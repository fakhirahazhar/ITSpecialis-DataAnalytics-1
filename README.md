# IT Specialis-DataAnalytics-1
IT Specialist in Data Analytics focuses on analyzing and interpreting data to support decision-making. They require expertise in statistics, programming Python and data visualization. 

# World Cup Matches Data Cleansing
The dataset comprises information about FIFA World Cup matches, containing details such as the year of the tournament, date and time of the match, stage of the tournament, stadium and city where the match took place, home and away team names, goals scored by each team, attendance, halftime scores, referee details, round ID, match ID, and initials of the home and away teams.

This dataset serves as the basis for analyzing FIFA World Cup matches, allowing for insights into various aspects of the tournament, such as team performances, match outcomes, and attendance trends. Before conducting any analysis, it's essential to perform data cleaning and preprocessing to ensure the dataset's quality and integrity.

## Python Libraries Import
<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/78bc434b-ace9-4c0c-accc-f6cc18302132" /></div>

## Load Data Set

Display the data set that has been loaded
<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/1476409b-23c9-45f2-81ed-a43d07a0cc31" /></div>

## Data Cleansing
Data cleansing is the process of identifying and correcting errors, inconsistencies, and inaccuracies in a dataset to improve its quality and reliability for analysis. It involves various tasks aimed at ensuring that the data is accurate, complete, and consistent.

### Check Data Condition
<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/a5a88496-01d7-4f53-9adf-dcc9800186f5" /></div>

From the description, we can see that some columns have fewer non-null values than the total entries, indicating the presence of null or empty values in the DataFrame. Additionally, we can also observe the data types of each column, where there are columns whose data types are not yet appropriate.

## Check and remove duplicate rows from theData Frame
### keep
- {‘first’, ‘last’, False}, default ‘first’
- Determines which duplicates (if any) to mark.
- first : Mark duplicates as True except for the first occurrence.

  <div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/7e54184c-666b-4c7c-b269-c31d2fb32977" /></div>

- last : Mark duplicates as True except for the last occurrence.

  <div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/15d83cbb-4fa1-4c35-9d53-f930f393f870" /></div>
  
- False : Mark all duplicates as True.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/d08aff44-cc69-4198-a344-2ccd21f0a960" /></div>

Due to the presence of numerous NaN values, our first step will be to drop rows containing NaN values.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/c4e8bd85-0a76-43e5-85cd-8a5a578a1ecb" /></div>

### Check Duplicate 

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/b9eb90fd-2ae4-42fc-85d6-4811ab764767" /></div>

 <div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/15d83cbb-4fa1-4c35-9d53-f930f393f870" /></div>

 <div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/15d83cbb-4fa1-4c35-9d53-f930f393f870" /></div>

  <div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/d08aff44-cc69-4198-a344-2ccd21f0a960" /></div>

Once we have confirmed that the duplicated data is indeed redundant, we can proceed to delete the duplicates.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/088c0335-b557-4f75-bab5-ef62d41bd795" /></div>

## Convert Dtype
"Convert Dtype" refers to the process of converting the data type of a column in a dataset. This process is often necessary to ensure that the data is in the appropriate format for analysis or visualization.

For example, if a column contains numerical data but is stored as a string, it may be necessary to convert it to a numerical data type (e.g., int or float) to perform mathematical operations or statistical analysis.

Similarly, if a column contains dates or times but is stored as a string or integer, it may be necessary to convert it to a datetime data type to perform date-based analysis or visualization.

In summary, converting data types ensures that the data is in the correct format for analysis and allows for more efficient and accurate data processing.

### Year 

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/ab5817c3-d530-4223-8f31-dc793dbb6753" /></div>

### Datetime

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/91df3230-4da1-49a5-9c69-b0abf90852c6" /></div>


### Home Team Goals, Away Team Goals, Attendance, Half-time Home Goals, Half-time Away Goals, RoundID, MatchID

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/811d52f0-6a18-4fdb-bbc3-fea239df1f4e" /></div>

## Check Percentage Missing Values
"Check Percentage Missing Values" refers to the process of calculating and determining the percentage of missing values in each column of a dataset. This step is essential in data preprocessing and quality assurance, as missing values can impact the accuracy and reliability of analytical results.

To perform this task, the dataset is inspected column by column, and the number of missing values in each column is counted. Then, the percentage of missing values is calculated by dividing the number of missing values by the total number of observations in the dataset and multiplying by 100.

Understanding the percentage of missing values in each column helps data analysts or scientists develop appropriate strategies for handling missing data. Depending on the nature of the missing values and their impact on the analysis, strategies such as imputation (replacing missing values with estimated ones), deletion of rows or columns with missing values, or specialized modeling techniques may be employed to address missing data issues effectively.

In summary, checking the percentage of missing values provides valuable insights into the data quality and guides decision-making regarding data preprocessing and analysis strategies.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/99f0ee0a-2b4a-4e51-bfab-2768855f9dd9" /></div>

It turns out that only the 'Datetime' column has missing values. Although the number of missing values is not significant, considering that 'Datetime' is a crucial column for analysis, we have decided to retain the missing values in the 'Datetime' column.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/5e17354d-cfe7-46d5-b0a3-6c00a8c0b8b9" /></div>

#### Insights and Considerations
- All columns have missing values, with 'Attendance' having the highest number of missing values, totaling 3722.
- Assuming we want to analyze "team performance in matches," some unimportant columns can be dropped.
##### Extremely Important Columns
- Year: The year of the match.
- Home Team Name: The name of the home team.
- Away Team Name: The name of the away team.
- Home Team Goals: The score of the match and the performance of the home team in scoring goals.
- Away Team Goals: The score of the match and the performance of the away team in scoring goals.
- Attendance: The number of spectators in the match.
- Datetime: The date and time of the match. (to be manipulated later)
##### Possibly Important Columns
- Half-time Home Goals: The number of goals scored by the home team in the first half.
- Half-time Away Goals: The number of goals scored by the away team in the first half.
- City: The city where the match took place.
- Stadium: The name of the stadium where the match took place.
- Stage: The stage or phase of the tournament.
- RoundID: The ID of the tournament round.
- MatchID: The ID of the match.
- Win conditions: The conditions for winning the match.
##### Unimportant Columns
- Referee: The name of the match referee.
- Assistant 1: The name of the first assistant referee.
- Assistant 2: The name of the second assistant referee.
- Home Team Initials: The initials of the home team.
- Away Team Initials: The initials of the away team.

## Data Manipulation
Data manipulation involves making changes to the dataset to prepare it for analysis or to extract valuable insights. This process includes tasks such as cleaning the data, transforming its structure, creating new features, and aggregating information.
### Drop Non-Essential Columns
This step involves removing columns from the dataset that are deemed non-essential for the analysis. Non-essential columns are those that do not contribute significantly to the analysis or do not align with the research objectives. By dropping these columns, we can streamline the dataset and focus only on the most relevant features.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/54ed1f6f-9d52-4596-9018-907d81602807" /></div>

We drop columns such as 'Referee', 'Assistant 1', 'Assistant 2', 'Home Team Initials', and 'Away Team Initials' as they are not critical for the analysis at hand.

Show dataset info to see if the date and country columns are missing.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/cd4ff5e4-0b49-4ed3-978a-6a8094a97de5" /></div>

### Make Column Draw, Date, and Time
We will perform data manipulation here. Manipulation here does not involve altering data values but rather restructuring the data to make it easier for machines to read.
To determine whether a match ended in a draw or not, we can use the "Home Team Goals" and "Away Team Goals" columns.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/fd27eec7-eae7-4c4c-836f-2bb535f738f7" /></div>

Split Datetime into 'Date' and 'Time'

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/e433c318-edc8-4899-a3f2-68c14183a5ca" /></div>


## Visualization
### Home Team Goals vs Away Team Goals 
Analyze the relationship between the number of goals scored by the home team and the number of goals scored by the away team.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/d4c7f830-062f-461c-a156-247be50df4b3" /></div>

Using value_counts() to count how many times each value of home team goals appears in the data, only in matches where the away team scored a goal.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/54a63b5f-28b3-4c97-ae9b-911387d7ecac" /></div>

### Win Conditions vs Home Team Goals
Looking at how victory conditions are based on home team goals

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/f6dcbf68-2959-49e0-a8b3-9997ea0af71e" /></div>

There are 48 entries in the DataFrame that have 5 or more goals scored by the home team but do not have any information in the 'win conditions' column.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/5785d72d-eedd-46ba-a46e-54592b22017f" /></div>

### Number of Matches by Year
- The groupby() function is used to group the rows of data based on the same value in the column used as the grouping criterion, in this case, the 'Year' column.
- The size() method counts the number of rows in each group. In this context, each year group will have the same number of rows as the number of matches in that year.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/2ea13c50-c0f0-4cf4-9c46-fb42ea47214f" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/194a3c83-da0d-49cb-8a84-24ec9192f9a5" /></div>

### Year vs Draw
Count of matches that ended in a draw for matches from the year 2000 onwards.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/4fd680f2-7ec7-436c-a23e-d4bdaabf07d8" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/9b6a5d5b-62be-4ddb-b824-2b1e88e0be5a" /></div>

## Pivot
Pivoting is a process used to reorganize and reshape data, typically for the purpose of analysis or visualization. In pandas, the `pivot_table()` function is commonly used to create a spreadsheet-style pivot table as a DataFrame. This function allows us to specify the index, columns, and values to aggregate, providing flexibility in how the data is arranged.

By pivoting data, we can transform rows into columns and vice versa, aggregating values based on specified criteria. This can help in summarizing and analyzing data in a more structured and intuitive format, facilitating further exploration and interpretation.

### Make_pivot
The `make_pivot` function is a custom utility developed to pivot the data in our dataset. Pivoting is a technique used to reshape data from long to wide format, making it easier to analyze and visualize. This function takes certain parameters such as index, columns, and aggregation functions to create a pivot table from the original dataset.

<div align="center"><img src="hhttps://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/e16b3a7a-f61e-45a4-b28a-3d5ac8e760d5" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/3c2efbfa-3a24-4284-930e-7b320911c160" /></div>

After observing the bar chart, it seems that visualizing Year vs Draw would be more appropriate using a line graph.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/0f375151-708a-4ada-a419-21214df1ac6d" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/0251636c-abe6-4db7-a2bc-acb6c1a5be00" /></div>

### Slice_pivot
The `slice_pivot` variable is a pivot table generated from a sliced portion of the original dataset. This pivot table provides insights into specific aspects of the data by grouping and aggregating values based on specified index and column criteria.
#### Description:
- `Purpose`: To analyze a subset of the dataset and visualize relationships between different variables.
- `Generated From`: The df_slice DataFrame, which is a subset of the original dataset containing selected columns.
- `Parameters`: The pivot table is created using the pivot_table function, with parameters specifying index, columns, and aggregation functions.

#### How many `Draws` based on the `Year`

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/94ad44ea-5d42-48b9-86d8-1b0343b1c55c" /></div>

#### How many `Draws` occur in each stage of the matches based on the `Year`

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/44f0e357-bc31-4d6f-8165-b16f86918833" /></div>

## Groupby
The `groupby` operation in pandas is a powerful tool for splitting the data into groups based on some criteria, applying a function to each group independently, and then combining the results into a DataFrame or other data structure.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/1e008baa-6867-4d06-b41f-fde50f618c15" /></div>


## Crosstab
The `crosstab` function in pandas is used to compute a cross-tabulation of two or more factors, also known as contingency tables. It computes a simple cross-tabulation of two (or more) factors, which can be either categorical or discrete variables.

By default, it calculates the frequency.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/0bf20d0d-9644-4733-a09f-56fb49412b03" /></div>

## Get Dummies
The `get_dummies` function in pandas is used to convert categorical variables into dummy/indicator variables, also known as one-hot encoding. It creates a new DataFrame with binary indicator variables for each category present in the original categorical variable.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/9567648a-5fca-43bc-b526-a7e128465a13" /></div>

## Sort
Sorting data in pandas allows you to rearrange the rows of a DataFrame or Series based on the values of one or more columns. The `sort_values` method is commonly used for this purpose.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/8445b6da-c69e-4fc4-a81c-6aec8de99be7" /></div>

## Rename
Renaming columns in pandas allows you to change the names of one or more columns in a DataFrame to make them more descriptive or suitable for analysis. The `rename` method is commonly used for this purpose.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/080a0afb-f5d9-44c5-9a1b-4fd7c1e9448f" /></div>

## Concat
Concatenating DataFrames in pandas involves combining multiple DataFrames along rows or columns. The `concat` function is used for this purpose.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/b6eeb7fd-8e7c-4a40-b87a-9ded16a37c90" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/cb469cb4-4fe7-41d1-ac48-982699714632" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/8f7c23a3-5742-4aa2-b230-d12739cc12c3" /></div>

## Merge
Merging DataFrames in pandas involves combining data from different sources based on common columns or indices. The `merge` function is used for this purpose.

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/b2b51adf-4fdf-4059-8e9e-8c9e162524ea" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/2d4e5a2e-bf60-4e08-8040-9d0edf5753ff" /></div>

<div align="center"><img src="https://github.com/fakhirahazhar/ITSpecialis-DataAnalytics-1/assets/165735471/98a68991-c5df-4aa2-9425-a816297d3062" /></div>












