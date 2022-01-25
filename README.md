# data-science
#jupyter
import pandas as pd
fname = '-/data/titanic/survive.csv'
data = pd.read_csv (fname)

len (data)
data.head()
Passengerid: serialID
Survived: 1 = survived, 0 = didn`t survived
Pclass : passenger class (1,2,3)
Name: full name of the passenger
Sex: male or female
Age: in years
SibSp:siblings or spouse abord the Titanic
Parch:parents of children abord the Titanic
Ticket:ticket number
Fare: passenger fare
Cabin: cabin number
Embarked: port of embarktion  ( Cherbourg = C, Queenstown = Q, Southampton = S)

data.count()
data['age'],min(), data['age'].max()
data['survived'].value_counts()
data['survived'].value_counts() * 100 / len(data)
data['sex'].value_counts()
data['Pclass'].value_counts()
%matplotlib inline
alpha_color = 0.5
data ['Survived'].value_counts().plot(kind='bar')
data['sex'].value_counts().plot(kind= 'bar',
                                color['b','r'],
                                alpha=alpha_color)
data['Pclass'].value_counts().sort_index().plot(kind='bar',
                                                alpha=alpha_color)
data.plot(kind='scatter', x= 'survived', y='age')
data[data['survived'] ==1]['Age'].value_counts().sort_index().plot(kind='bar')
bins = [0,10,20,30,40,50,60,70,80]
data['ageBin'] = pd.cut(data['age'].bins)
data[data['survived'] == 1]['AgeBin'].value_counts().sort_index().plot(kind='bar')
data[data['survived'] == 0]['AgeBin'].value_counts().sort_index().plot(kind='bar')
data['ageBin'].value_counts().sort_index().plot(kind='bar')
data[data['Pclass'] == 1]['Survived'].value_counts().plot(kind='bar')
data[data['Pclass'] == 3]['Survived'].value_counts().plot(kind='bar')
data[data['Sex'] == 'male']['Survived'].value_counts().plot(kind='bar')
data[data['Sex'] == 'female']['Survived'].value_counts().plot(kind='bar')
