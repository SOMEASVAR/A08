# A08-IMPLEMENT KDE PLOT WITH ANY ONE OF YOUR OWN DATA SET


## CODE:
```
Program Developed By: R.SOMEASVAR 
Register Number: 212221230103
```
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("titanic_dataset.csv")

df

#Create KDE for all the numeric variables in dataframe
sns.kdeplot(data=df)

sns.kdeplot(data=df, x='Pclass')

sns.kdeplot(data=df, x='Age')

sns.kdeplot(data=df, x='Fare')

sns.kdeplot(data=df,x='Survived',hue='Sex')

sns.kdeplot(data=df,x='Fare',hue='Sex')

sns.kdeplot(data=df,x='Survived',hue='Age')

sns.kdeplot(data=df,x='SibSp',hue='Age')

sns.kdeplot(data=df,x='Survived',hue='Pclass')

#Stack KDE on a category using MULTIPLE argument
sns.kdeplot(data=df,x='Survived',hue='Sex',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Sex',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)

sns.kdeplot(data=df,x='Fare',hue='Sex',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Pclass',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Pclass',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)

sns.kdeplot(data=df,x='Fare',hue='Pclass',multiple='stack')

#Create a bivariate KDE
sns.kdeplot(data=df, x='Survived',y='SibSp')

sns.kdeplot(data=df, x='Survived',y='Fare')

sns.kdeplot(data=df, x='Age',y='Fare')

sns.kdeplot(data=df, x='Age',y='Pclass')

```
# OUTPUT:
# Initial Dataframe:
![op](./1.jpg)
# KDE for all numeric variables of the Dataframe:
![op](./2.jpg)
## Basic KDE plot for Pclass column:
![op](./3.jpg)
## Basic KDE plot for Age column:
![op](./4.jpg)
## Basic KDE plot for Fare column:
![op](./5.jpg)
## Basic KDE plot for Survived column:
![op](./6.jpg)
## Basic KDE plot for SibSp column:
![op](./7.jpg)
# KDE on a category using MULTIPLE argument:
## Survived Vs Sex:
![op](./8.jpg)
## Fare Vs Sex:
![op](./9.jpg)
## Survived Vs Pclass:
![op](./10.jpg)
# KDE on a category using MULTIPLE argument(Using additional Parameter- stack):
## Survived Vs Sex
![op](./11.jpg)
## Fare Vs Sex
![op](./12.jpg)
## Survived Vs Pclass:
![op](./13.jpg)
## Fare Vs Pclass:
![op](./14.jpg)
# KDE on a category using MULTIPLE argument(Using additional Parameter- stack,line width):
## Survived Vs Sex:
![op](./15.jpg)
## Survived Pclass:
![op](./16.jpg)

## Bivariate KDE:
## Survived Vs SibSp:
![op](./17.jpg)
## Survived Vs Fare:
![op](./18.jpg)
## Age Vs Fare:
![op](./19.jpg)
## Age Vs Pclass:
![op](./20.jpg)