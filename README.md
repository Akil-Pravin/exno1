
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
            df.fillna('sample value')
            <img width="1810" height="592" alt="image" src="https://github.com/user-attachments/assets/3af0af4d-b173-4cb5-9cbe-53c703dc4ecc" />
            ffil=df.fillna(method='ffill') #fflill=forward fill
ffil
            <img width="1819" height="647" alt="image" src="https://github.com/user-attachments/assets/bee5e3cd-c99d-42d0-893e-c88f2eca1603" />
            bfil=df.fillna(method='bfill')
bfil
            <img width="1821" height="660" alt="image" src="https://github.com/user-attachments/assets/9623de16-e766-4f31-9674-79d47c0a464f" />
            m=df.num_episodes.mean()
m
            <img width="1820" height="128" alt="image" src="https://github.com/user-attachments/assets/e328cd84-73c6-40af-a2f6-8bdc421f8f85" />
            n=df.fillna(df['num_episodes'].mean())
n
            <img width="1821" height="618" alt="image" src="https://github.com/user-attachments/assets/307fade3-89a8-4c25-9204-46c1cbc4b55c" />
            fmean=df['lifetime_popularity_rank'].fillna(value=df['lifetime_popularity_rank'].mean())
fmean
            <img width="1823" height="655" alt="image" src="https://github.com/user-attachments/assets/91d48228-68e6-429b-92f5-673af6acefd0" />
            import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS (2).csv')
df
            <img width="1818" height="798" alt="image" src="https://github.com/user-attachments/assets/1ff25d30-7cdf-4a59-bca1-5c5d2e2b35fe" />
            df.shape
            <img width="1826" height="100" alt="image" src="https://github.com/user-attachments/assets/b9509b1e-841b-4f89-84de-26d31ac8f984" />
            df.describe()
            <img width="1821" height="440" alt="image" src="https://github.com/user-attachments/assets/72a98782-8edf-4a4d-86fd-3103a4bcda16" />
            df.info()
            <img width="1822" height="494" alt="image" src="https://github.com/user-attachments/assets/3ffd196b-2e44-43ee-99f8-ed9c9765bc8b" />
            df['GENDER'].value_counts()
            <img width="1822" height="273" alt="image" src="https://github.com/user-attachments/assets/251f9c24-2e33-4ae6-9ff1-8d2d294b6aec" />
            df.dropna(how='any').shape
            <img width="1823" height="100" alt="image" src="https://github.com/user-attachments/assets/a1da424b-0162-468a-9170-aa2a03d7441b" />
            x1=df.dropna(how='any')
x1
            <img width="1815" height="652" alt="image" src="https://github.com/user-attachments/assets/6f4f3228-36dd-4ee7-b8f7-21daf912ca79" />
            res=df.dropna(subset=['M1','M2','M3','M4'],how='any')
res
            <img width="1818" height="660" alt="image" src="https://github.com/user-attachments/assets/36b366f9-af99-4742-b5da-f6932794668a" />
            m2=df.TOTAL.mean()
m2
            <img width="1822" height="130" alt="image" src="https://github.com/user-attachments/assets/59e22061-777c-4987-946e-31e7c777f912" />
            df.TOTAL.fillna(m2,inplace=False)
df
            <img width="1825" height="806" alt="image" src="https://github.com/user-attachments/assets/41633628-f866-4cc1-90db-b7d040312bdc" />
            df.isnull()
            <img width="1808" height="800" alt="image" src="https://github.com/user-attachments/assets/548ffedb-fc87-49d4-9bc2-37eb659fb81d" />
            import seaborn as sns
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
            <img width="1821" height="723" alt="image" src="https://github.com/user-attachments/assets/f1ea3c1f-6f01-4c1e-9ac5-3e8d31ac4945" />
            sns.heatmap(df.isnull(),yticklabels=True,annot=True)
            <img width="1818" height="700" alt="image" src="https://github.com/user-attachments/assets/3903bba7-c1bc-441e-987e-034fdf58c39c" />
            df.dropna(inplace=True)
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
            <img width="1813" height="720" alt="image" src="https://github.com/user-attachments/assets/58598179-734a-47e8-9e4a-ade5f17ed607" />
            df=pd.read_csv('/content/heights (1).csv')
df
            <img width="1812" height="693" alt="image" src="https://github.com/user-attachments/assets/430d871e-bd4c-404a-b45d-81132673d7e0" />
            sns.boxplot(data=df)
            <img width="1829" height="616" alt="image" src="https://github.com/user-attachments/assets/6370ab7e-e434-49cc-9783-5ac0b8d52d8b" />
            sns.scatterplot(data=df)
            <img width="1808" height="612" alt="image" src="https://github.com/user-attachments/assets/cef5ceda-92ca-486a-876e-aa30270223f3" />
            max=df['height'].quantile(0.75)
min=df['height'].quantile(0.25)
iqr=max-min
iqr
            <img width="1821" height="173" alt="image" src="https://github.com/user-attachments/assets/bd7b9201-c387-4bf2-9744-5159119c5cce" />
            lb=min-1.5*iqr
ub=max+1.5*iqr
outliers=df[(df['height']<lb)|(df['height']>ub)]
print("Lower bound",lb)
print("Upper bound",ub)
print("outliers",outliers)
            <img width="1818" height="303" alt="image" src="https://github.com/user-attachments/assets/4ca651d1-6a57-4c8a-9b59-883e67f77770" />
            no_outliers=df[~((df['height']<lb)|(df['height']>ub))]
no_outliers
            <img width="1817" height="602" alt="image" src="https://github.com/user-attachments/assets/066c6a58-bbcf-4868-b011-28c9ac2ac4d0" />
            sns.boxplot(data=no_outliers)
            <img width="1816" height="619" alt="image" src="https://github.com/user-attachments/assets/1f4546ef-0102-47da-8c8a-94275b99316c" />
            sns.scatterplot(data=no_outliers)
            <img width="1823" height="622" alt="image" src="https://github.com/user-attachments/assets/358a2b30-97f1-4a4a-86c4-568ddfeaf04f" />
            import matplotlib.pyplot as plt
df
            <img width="1816" height="699" alt="image" src="https://github.com/user-attachments/assets/c9a5b357-6626-454d-bde4-573b14b2e1d5" />
            max=df['height'].quantile(0.75)
q2=df['height'].quantile(0.5)
min=df['height'].quantile(0.25)
iqr=max-min
lb=min-1.5*iqr
ub=max+1.5*iqr
dfs=df[(df['height']>=lb)&(df['height']<=ub)]
dfs
            <img width="1813" height="753" alt="image" src="https://github.com/user-attachments/assets/986381b8-e0aa-4bff-8322-eb781bd5db63" />
            import numpy as np
from scipy import stats
z= np.abs(stats.zscore(df['height']))
z
            <img width="1824" height="216" alt="image" src="https://github.com/user-attachments/assets/c2141add-e3ec-4ce2-8c14-68aa74c79550" />
            df1=df[z<3]
df1
            <img width="1808" height="658" alt="image" src="https://github.com/user-attachments/assets/47b96e34-f83f-4615-8b3c-10ff48ada1ef" />
            val=df['height']
val
            <img width="1811" height="742" alt="image" src="https://github.com/user-attachments/assets/edb3404a-436e-40af-9010-b7a2867dd716" />
            out=[]
def d_o(val):
  ts=3
  m=np.mean(val)
  sd=np.std(val)
  for i in val:
    z=(i-m)/sd
    if np.abs(z)>ts:
      out.append(i)
      return out
            <img width="1820" height="250" alt="image" src="https://github.com/user-attachments/assets/eab42673-0d1d-4e7a-947a-d810359f3a24" />
            op=d_o(val)
op
            <img width="1820" height="131" alt="image" src="https://github.com/user-attachments/assets/4d598e78-8140-4dd9-99b7-149fbc63629b" />













            








            















            
            


            
            








            




# Result
          THUS WE HAVE CLEANED THE DATA AND REMOVED THE OUTLIERS BY DETECTION USING IQR AND Z-SCORE METHOD.
