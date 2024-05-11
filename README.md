# CSC245-lab3

![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/f2217bbe-b77d-47ab-a952-e0d62e6303bc)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/f4bf0f43-2ddd-4f6e-845e-6f680bbdb85f)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/9034b1ed-05c2-434b-b1f3-66b2385b0e8c)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/63c6a64b-d1c5-42de-9550-36d880af86a7)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/5f3a99c1-c5d5-41e1-bd69-fc11d4176bbf)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/996adeef-3e45-43e1-a668-a82fdb477594)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/e516e42a-cebb-466c-bcac-297207477922)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/7e915b89-bca7-49fd-938c-e47998518a92)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/4c886379-bc1c-4a90-8d8d-840c26255c6e)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/52cd889d-1486-4048-8cac-bc3a54bd73aa)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/711011b0-94b5-4fe3-8fd5-a445708635ce)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/661f31d0-c2db-4040-8f3a-9dfa81f9cdda)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/fe69263f-4c0f-4b44-80ca-f2a9511205d6)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/b4a5faa9-3806-49f8-89e0-3bb1c7f7c23a)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab3/assets/166454688/2b5ce4a7-9c52-4bd3-8735-6a18cf2bc00e)



# 1. Write a Pandas program to join the two given dataframes along rows and assign all data.
import pandas as pd
student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

student_data2 = pd.DataFrame({
    'student_id': ['S4', 'S5', 'S6', 'S7', 'S8'],
    'name': ['Scarlette Fisher', 'Carla Williamson', 'Dante Morse', 'Kaiser William', 'Madeeha Preston'],
    'marks': [201, 200, 198, 219, 201]
})

print("Original DataFrames:")
print(student_data1)
print()
print(student_data2)

result_data = pd.concat([student_data1, student_data2])

print("\nJoin the said two dataframes along rows:")
print(result_data)


# 2. Write a Pandas program to join the two given dataframes along columns and assign all data.
import pandas as pd

# Create the first dataframe
student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

# Create the second dataframe
student_data2 = pd.DataFrame({
    'student_id': ['S4', 'S5', 'S6', 'S7', 'S8'],
    'name': ['Scarlette Fisher', 'Carla Williamson', 'Dante Morse', 'Kaiser William', 'Madeeha Preston'],
    'marks': [201, 200, 198, 219, 201]
})

# Display the original DataFrames
print("Original DataFrames:")
print(student_data1)
print()
print(student_data2)

# Join the two dataframes along columns
result_data = pd.concat([student_data1, student_data2], axis=1)

# Print the result
print("\nJoin the said two dataframes along columns:")
print(result_data)

# 3. Write a Pandas program to append rows to an existing DataFrame and display the combined data.
import pandas as pd

# Create the first dataframe with initial data
student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

# Create a new row intended to be appended to the DataFrame
new_row = pd.DataFrame({
    'student_id': ['S6'],
    'name': ['Scarlette Fisher'],
    'marks': [205]
})

# Combine the original DataFrame with the new row
combined_data = pd.concat([student_data1, new_row], ignore_index=True)

# Print the original DataFrame, the new row, and the combined data
print("Original DataFrame:")
print(student_data1)
print("\nNew Row(s):")
print(new_row)
print("\nCombined Data:")
print(combined_data)

# 4. Write a Pandas program to append a list of dictionaries or series to a existing DataFrame and display the combined data.
import pandas as pd

# Create the first dataframe with initial data
student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

# Create a DataFrame from a list of dictionaries to represent new rows
new_rows = pd.DataFrame([
    {'student_id': 'S6', 'name': 'Scarlette Fisher', 'marks': 203},
    {'student_id': 'S7', 'name': 'Bryce Jensen', 'marks': 207}
])

# Combine the original DataFrame with the new rows
combined_data = pd.concat([student_data1, new_rows], ignore_index=True)

# Print the original DataFrame, the new rows, and the combined data
print("Original DataFrame:")
print(student_data1)
print("\nNew Rows:")
print(new_rows)
print("\nCombined Data:")
print(combined_data)

# 5. Write a Pandas program to join the two given dataframes along rows and merge with another dataframe along the common column id.
import pandas as pd

# Create the first dataframe with initial data
student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

# Create the second dataframe with additional data
student_data2 = pd.DataFrame({
    'student_id': ['S4', 'S5', 'S6', 'S7', 'S8'],
    'name': ['Scarlette Fisher', 'Carla Williamson', 'Dante Morse', 'Kaiser William', 'Madeeha Preston'],
    'marks': [201, 200, 198, 219, 201]
})

# Create an exam data dataframe
exam_data = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5', 'S6', 'S7', 'S8', 'S9', 'S10', 'S11', 'S12', 'S13'],
    'exam_id': [23, 45, 12, 67, 21, 56, 83, 88, 12]
})

# Concatenate the first two dataframes along rows
result_data = pd.concat([student_data1, student_data2])

# Merge the concatenated dataframe with the exam data dataframe on 'student_id'
final_merged_data = pd.merge(result_data, exam_data, on='student_id')

# Display the data
print("Original DataFrames:")
print(student_data1)
print(student_data2)
print(exam_data)
print("\nJoin first two said dataframes along rows:")
print(result_data)
print("\nNow join the said result_data and df_exam_data along student_id:")
print(final_merged_data)


# 6. Write a Pandas program to join the two dataframes using the common column of both dataframes.
import pandas as pd

# Create the first dataframe with initial data
student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

# Create the second dataframe with additional data
student_data2 = pd.DataFrame({
    'student_id': ['S4', 'S5', 'S6', 'S7', 'S8'],
    'name': ['Scarlette Fisher', 'Carla Williamson', 'Dante Morse', 'Kaiser William', 'Madeeha Preston'],
    'marks': [201, 200, 198, 219, 201]
})

# Display the original DataFrames
print("Original DataFrames:")
print(student_data1)
print(student_data2)

# Perform an inner join on 'student_id'
merged_data = pd.merge(student_data1, student_data2, on='student_id', how='inner')

# Print the merged data
print("Merged data (inner join):")
print(merged_data)


# 7. Write a Pandas program to join the two dataframes with matching records from both sides where available.
import pandas as pd

# Create the first dataframe with initial data
student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

# Create the second dataframe with additional data
student_data2 = pd.DataFrame({
    'student_id': ['S4', 'S5', 'S6', 'S7', 'S8'],
    'name': ['Scarlette Fisher', 'Carla Williamson', 'Dante Morse', 'Kaiser William', 'Madeeha Preston'],
    'marks': [201, 200, 198, 219, 201]
})

# Display the original DataFrames
print("Original DataFrames:")
print(student_data1)
print(student_data2)

# Perform an outer join on 'student_id'
merged_data = pd.merge(student_data1, student_data2, on='student_id', how='outer')

# Print the merged data
print("Merged data (outer join):")
print(merged_data)

# 8. Write a Pandas program to join (left join) the two dataframes using keys from left dataframe only.
import pandas as pd
data1 = pd.DataFrame({'key1': ['K0', 'K0', 'K1', 'K2'],
                     'key2': ['K0', 'K1', 'K0', 'K1'],
                     'P': ['P0', 'P1', 'P2', 'P3'],
                     'Q': ['Q0', 'Q1', 'Q2', 'Q3']}) 
data2 = pd.DataFrame({'key1': ['K0', 'K1', 'K1', 'K2'],
                      'key2': ['K0', 'K0', 'K0', 'K0'],
                      'R': ['R0', 'R1', 'R2', 'R3'],
                      'S': ['S0', 'S1', 'S2', 'S3']})
print("Original DataFrames:")
print(data1)
print("--------------------")
print(data2)
print("\nMerged Data (keys from data1):")
merged_data = pd.merge(data1, data2, how='left', on=['key1', 'key2'])
print(merged_data)
print("\nMerged Data (keys from data2):")
merged_data = pd.merge(data2, data1, how='left', on=['key1', 'key2'])
print(merged_data)


9. Write a Pandas program to join two dataframes using keys from right dataframe only.
import pandas as pd
data1 = pd.DataFrame({'key1': ['K0', 'K0', 'K1', 'K2'],
                     'key2': ['K0', 'K1', 'K0', 'K1'],
                     'P': ['P0', 'P1', 'P2', 'P3'],
                     'Q': ['Q0', 'Q1', 'Q2', 'Q3']}) 
data2 = pd.DataFrame({'key1': ['K0', 'K1', 'K1', 'K2'],
                      'key2': ['K0', 'K0', 'K0', 'K0'],
                      'R': ['R0', 'R1', 'R2', 'R3'],
                      'S': ['S0', 'S1', 'S2', 'S3']})
print("Original DataFrames:")
print(data1)
print("--------------------")
print(data2)
print("\nMerged Data (keys from data2):")
merged_data = pd.merge(data1, data2, how='right', on=['key1', 'key2'])
print(merged_data)
print("\nMerged Data (keys from data1):")
merged_data = pd.merge(data2, data1, how='right', on=['key1', 'key2'])
print(merged_data)
10. Write a Pandas program to merge two given datasets using multiple join keys.
import pandas as pd
data1 = pd.DataFrame({'key1': ['K0', 'K0', 'K1', 'K2'],
                     'key2': ['K0', 'K1', 'K0', 'K1'],
                     'P': ['P0', 'P1', 'P2', 'P3'],
                     'Q': ['Q0', 'Q1', 'Q2', 'Q3']}) 
data2 = pd.DataFrame({'key1': ['K0', 'K1', 'K1', 'K2'],
                      'key2': ['K0', 'K0', 'K0', 'K0'],
                      'R': ['R0', 'R1', 'R2', 'R3'],
                      'S': ['S0', 'S1', 'S2', 'S3']})
print("Original DataFrames:")
print(data1)
print("--------------------")
print(data2)
print("\nMerged Data:")
merged_data = pd.merge(data1, data2, on=['key1', 'key2'])
print(merged_data)


11. Write a Pandas program to create a new DataFrame based on existing series, using specified argument and override the existing columns names.
import pandas as pd

# Creating three Series with specified names
s1 = pd.Series([0, 1, 2, 3], name='col1')
s2 = pd.Series([0, 1, 2, 3], name='col2')
s3 = pd.Series([0, 1, 4, 5], name='col3')

# Concatenating the series into a DataFrame along columns, and specifying custom column names
df = pd.concat([s1, s2, s3], axis=1, keys=['column1', 'column2', 'column3'])

# Printing the resulting DataFrame
print(df)


# 12. Write a Pandas program to create a combination from two dataframes where a column id combination appears more than once in both dataframes.
import pandas as pd
data1 = pd.DataFrame({'key1': ['K0', 'K0', 'K1', 'K2'],
                     'key2': ['K0', 'K1', 'K0', 'K1'],
                     'P': ['P0', 'P1', 'P2', 'P3'],
                     'Q': ['Q0', 'Q1', 'Q2', 'Q3']}) 
data2 = pd.DataFrame({'key1': ['K0', 'K1', 'K1', 'K2'],
                      'key2': ['K0', 'K0', 'K0', 'K0'],
                      'R': ['R0', 'R1', 'R2', 'R3'],
                      'S': ['S0', 'S1', 'S2', 'S3']})
print("Original DataFrames:")
print(data1)
print("--------------------")
print(data2)
print("\nMerged Data (many-to-many join case):")
result = pd.merge(data1, data2, on='key1')
print(result)


# 13 Write a Pandas program to combine the columns of two potentially differently-indexed DataFrames into a single result DataFrame.

import pandas as pd
data1 = pd.DataFrame({'A': ['A0', 'A1', 'A2'],
                      'B': ['B0', 'B1', 'B2']},
                     index=['K0', 'K1', 'K2'])

data2 = pd.DataFrame({'C': ['C0', 'C2', 'C3'],
                      'D': ['D0', 'D2', 'D3']},
                     index=['K0', 'K2', 'K3'])
 
print("Original DataFrames:")
print(data1)
print("--------------------")
print(data2)
print("\nMerged Data (Joining on index):")
result = data1.join(data2)
print(result)

# 14. Write a Pandas program to merge two given dataframes with different columns.

import pandas as pd
data1 = pd.DataFrame({'key1': ['K0', 'K0', 'K1', 'K2'],
                     'key2': ['K0', 'K1', 'K0', 'K1'],
                     'P': ['P0', 'P1', 'P2', 'P3'],
                     'Q': ['Q0', 'Q1', 'Q2', 'Q3']}) 
data2 = pd.DataFrame({'key1': ['K0', 'K1', 'K1', 'K2'],
                      'key2': ['K0', 'K0', 'K0', 'K0'],
                      'R': ['R0', 'R1', 'R2', 'R3'],
                      'S': ['S0', 'S1', 'S2', 'S3']})
print("Original DataFrames:")
print(data1)
print("--------------------")
print(data2)
print("\nMerge two dataframes with different columns:")
result = pd.concat([data1,data2], axis=0, ignore_index=True)
print(result)

# 15. Write a Pandas program to Combine two DataFrame objects by filling null values in one DataFrame with non-null values from other DataFrame.

import pandas as pd
df1 = pd.DataFrame({'A': [None, 0, None], 'B': [3, 4, 5]})
df2 = pd.DataFrame({'A': [1, 1, 3], 'B': [3, None, 3]})
df1.combine_first(df2)
print("Original DataFrames:")
print(df1)
print("--------------------")
print(df2)
print("\nMerge two dataframes with different columns:")
result = df1.combine_first(df2)
print(result)


