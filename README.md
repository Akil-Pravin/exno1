# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
            import pandas as pd
df=pd.read_csv('/content/Data_set (5).csv')
            <img width="1825" height="511" alt="image" src="https://github.com/user-attachments/assets/c2b2c216-4364-4e29-922a-3d0fc38f91f7" />
            df.describe()
            <img width="1823" height="435" alt="image" src="https://github.com/user-attachments/assets/e9bc30c1-e4e6-4312-86fb-392e3719086a" />
            df.head(16)
            <img width="1810" height="734" alt="image" src="https://github.com/user-attachments/assets/d74a4130-411d-412f-ba3d-cad58714ade2" />
            df.tail(5)
            <img width="1822" height="307" alt="image" src="https://github.com/user-attachments/assets/e75ce497-01c6-4cfd-b5a2-6cd0a668303e" />
            df.shape
            <img width="1823" height="97" alt="image" src="https://github.com/user-attachments/assets/b08f3a65-b53c-4d4a-b90f-b1f4a4162a04" />
            df.isnull()
            <img width="1820" height="589" alt="image" src="https://github.com/user-attachments/assets/fb6df455-1bf5-4e41-8a03-7695528e00d0" />
            df.notnull()
            <img width="1821" height="593" alt="image" src="https://github.com/user-attachments/assets/bc846a0e-2d23-4316-818f-5c7c47eec545" />
            df.notnull().sum()
            <img width="1817" height="520" alt="image" src="https://github.com/user-attachments/assets/e8fc511d-4709-48d5-af9b-f06c135ee11e" />
            df.isnull().sum() /len(df)*100
            <img width="1820" height="511" alt="image" src="https://github.com/user-attachments/assets/2a727d3e-7b56-4d65-89a3-70707a3f21c6" />
            df.dropna(axis=0)
            <img width="1820" height="585" alt="image" src="https://github.com/user-attachments/assets/20a27e16-d152-44be-971c-499cfe3706b3" />
            df.dropna(axis=1)
            <img width="1815" height="571" alt="image" src="https://github.com/user-attachments/assets/795bef4e-3f93-499f-be32-d79c60c1e999" />
            dfs=df[df['current_overall_rank']>50]
dfs
            <img width="1814" height="651" alt="image" src="https://github.com/user-attachments/assets/5c6de04f-17da-4f64-93e0-6c270047e789" />
            df.fillna(0)
df
            <img width="1809" height="613" alt="image" src="https://github.com/user-attachments/assets/cc3004ab-cfd5-4b2a-ac34-5678e70c52c4" />
            dfs=df[df['show_name'].astype('str').str.upper().str.startswith('A','B')]
dfs
            <img width="1813" height="377" alt="image" src="https://github.com/user-attachments/assets/654f8929-a951-4885-b7b2-6746b1ff211b" />
            df.iloc[:4]
            <img width="1810" height="276" alt="image" src="https://github.com/user-attachments/assets/73f0886b-1b6f-4095-bb4c-5577b4da8a38" />
            df.iloc[[1,3,5],[1,3,5]]
            <img width="1812" height="238" alt="image" src="https://github.com/user-attachments/assets/bc3fd56c-5b41-4a70-b567-d4bf05c5b467" />
            
            <img width="1818" height="585" alt="image" src="https://github.com/user-attachments/assets/96858bef-1321-4a39-895a-4ea3960b043d" />


            
            








            




# Result
          <<include your Result here>>
