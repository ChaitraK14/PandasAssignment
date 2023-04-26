# PandasAssignment

Q1. How do you load a CSV file into a Pandas DataFrame?

A: By using read_csv() function.

   Ex:
   
          pandas.read_csv(data.csv)

Q2. How do you check the data type of a column in a Pandas DataFrame?

A: By using dtypes attribute.

   Ex:
   
          pandas.DataFrame[column_name].dtypes

Q3. How do you select rows from a Pandas DataFrame based on a condition?

A: 
          
          import pandas as pd
          
          d = {'Name':['abc','xyz','pqr','lmn'],'age':[16,14,19,24],'gender':['M','F','M','F']}
          df=pd.DataFrame(data=d)
          eligible_to_vote = df[df.age>18]
          print(eligible_to_vote)
          
Q4. How do you rename columns in a Pandas DataFrame?
A: By using rename() function.

          df.rename(column={'age':'Age'})
          
Q5. How do you drop columns in a Pandas DataFrame?

A: By using drop() function.
          
          df_new = df.drop('gender',axis=1)
          df_new

Q6. How do you find the unique values in a column of a Pandas DataFrame?

A: By using unique() function.

          df.gender.unique()

Q7. How do you find the number of missing values in each column of a Pandas DataFrame?

A: number of missing values in each column of a Pandas DataFrame can be found as below:

          df.isna().sum()

Q8. How do you fill missing values in a Pandas DataFrame with a specific value?

A: By using fillna() funtion.

          df.state.fillna('Karnataka',inplace=True)

Q9. How do you concatenate two Pandas DataFrames?

A: By using concat() function.

          df_new = pd.concat([df,df2])
          df_new

Q10. How do you merge two Pandas DataFrames on a specific column?

A:        

          df1 = pd.DataFrame(data={'Name':['A','B','C','D'],'Marks':[45,79,68,90]})
          df2 = pd.DataFrame(data={'Name':['A','B','C','D'],'Grade':['D','B','C','A']})

          df_merge = df2.merge(df1,on='Name')
          df_merge

Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?

A: 

          df1 = pd.DataFrame(data={'Name':['A','B','C','D','B','D','C','A'],'Marks':[45,79,68,90,72,45,58,83],'Grade':['D','B','C','A','B','D','C','A']})
          df1.groupby('Name')['Marks'].sum()

Q12. How do you pivot a Pandas DataFrame?

A:  

          df1 = pd.DataFrame(data={'Name':['Ram','Jai','John','Ravi'],'Marks':[45,79,68,90],'Grade':['D','B','C','A']})
          df1.pivot('Name','Grade','Marks')

Q13. How do you change the data type of a column in a Pandas DataFrame?

A: By using astype() function.

          df = pd.DataFrame(data={'Name':['Ram','Jai','John','Ravi'],'Marks':['45','79','68','90'],'Grade':['D','B','C','A']})
          df_new = df.astype({'Marks':int})
          
                                or
                                
          df = pd.DataFrame(data={'Name':['Ram','Jai','John','Ravi'],'Marks':['45','79','68','90'],'Grade':['D','B','C','A']})
          df_new = df[['Marks']].apply(pd.to_numeric)
          df_new.Marks.dtypes

Q14. How do you sort a Pandas DataFrame by a specific column?

A: By using sort_values() function.


           df = pd.DataFrame(data={'Name':['Jai','Abhi','Kishan','Bheem'],'Age':[12,35,24,16]})
           df.sort_values('Name')

Q15. How do you create a copy of a Pandas DataFrame?

A: By using copy() function.

            df = pd.DataFrame(data={'Name':['Jai','Abhi','Kishan','Bheem'],'Age':[12,35,24,16]})
            df_copy = df.copy()

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?

A: filter rows of a Pandas DataFrame by multiple conditions can be achieved in any one of the below ways.

   1.loc works with column labels and indexes.
   2.eval and query works only with columns.
   3.Boolean indexing works with values in a column only.

Q17. How do you calculate the mean of a column in a Pandas DataFrame?

Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?

Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?

Q20. How do you select specific columns in a DataFrame using their labels?

Q21. How do you select specific rows in a DataFrame using their indexes?

Q22. How do you sort a DataFrame by a specific column?

Q23. How do you create a new column in a DataFrame based on the values of another column?

Q24. How do you remove duplicates from a DataFrame?

Q25. What is the difference between .loc and .iloc in Pandas?
