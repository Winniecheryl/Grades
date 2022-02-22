# Grades
Analysis of KCSE Grades

##Link to the code used to perform the analysis

http://localhost:8888/notebooks/ds%20task.ipynb

The performance of students in different years vary, but what stay common is that the number of boys outdo the number of girls who sit for the exams

![image](https://user-images.githubusercontent.com/58620711/153793795-e8fb8672-1ce4-4ee7-aab5-4dff7305755a.png)








##Excel form
[ds_task.csv](https://github.com/Winniecheryl/Grades/files/8057606/ds_task.csv)




``` import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
​

dataset = pd.read_csv("C:\\Users\\CHERYL\\Desktop\\Datasets\\ds_task.csv")

​
plt.savefig('chart.png')
dataset. head(10)
Gender	A	A-	B+	B	B-	C+	C	C-	D+	D	D-	E	Total no. of candidates	Unnamed: 14	Unnamed: 15
0	FEMALE(2016)	58.0	2685.0	6581.0	10204.0	13649.0	17238.0	22960.0	30979.0	41632.0	57487.0	77718.0	18007.0	299198	NaN	NaN
1	MALE(2016)	83.0	1960.0	4394.0	7012.0	10096.0	14969.0	21832.0	30047.0	39319.0	54648.0	72211.0	15322.0	271893	NaN	NaN
2	ALL(2016)	141.0	4645.0	10975.0	17216.0	23745.0	32207.0	44792.0	61026.0	80951.0	112135.0	149929.0	33399.0	571161	NaN	NaN
3	MALE(2015)	2024.0	7952.0	13517.0	19826.0	25312.0	29556.0	33437.0	37482.0	40181.0	40442.0	25531.0	3127.0	278387	NaN	NaN
4	FEMALE(2015)	661.0	4117.0	8410.0	13634.0	19269.0	25214.0	31476.0	36633.0	38976.0	39113.0	23127.0	2223.0	242853	NaN	NaN
5	ALL(2015)	2685.0	12069.0	21927.0	33460.0	44581.0	54770.0	64913.0	74115.0	79157.0	79555.0	48658.0	5350.0	521240	NaN	NaN
6	MALE (2006)	148.0	638.0	1195.0	1627.0	2108.0	2569.0	2984.0	3299.0	3418.0	3291.0	2635.0	834.0	24746	NaN	NaN
7	FEMALE (2006)	69.0	242.0	446.0	772.0	1234.0	1873.0	2554.0	3193.0	3519.0	3513.0	2909.0	897.0	21221	NaN	NaN
8	ALL (2006)	217.0	880.0	1641.0	2399.0	3342.0	4442.0	5538.0	6492.0	6937.0	6804.0	5544.0	1731.0	45967	NaN	NaN
9	MALE (2007)	110.0	563.0	1159.0	1761.0	2268.0	2871.0	3314.0	3609.0	3721.0	3493.0	2762.0	779.0	26410	NaN	NaN
<Figure size 432x288 with 0 Axes>

sns.heatmap(dataset.isnull())

sns.countplot(dataset['B+'])

sns.countplot(dataset['Gender'])

dataset_new = dataset[['B', 'Gender']]

plt.figure(figsize = (20,10))
sns.heatmap(dataset.corr())

```
