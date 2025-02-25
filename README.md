### EXP. NO: 04
### DATE: 11.05.2022

# Correlation and Regression for Data Analysis
# Aim : 
To analyse given data using  coeffificient of correlation and regression line.
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)

# Software required :  
Python

# Theory:
Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  
If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :
<img src ="https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png" width ="300" height="200">

# Program:
```python
''' 
Developed by : M Lokesh Krishnaa 
Register No: 212220230030
'''
import math
import numpy as np
import matplotlib.pyplot as plt
x = [25,28,35,32,31,36,29,38,34,32]
y = [43,46,49,41,36,32,31,30,33,39]
sx=sy=sxy=sx2=sy2=0
for i in range(0,10):
    sx +=x[i]
    sy +=y[i]
    sxy+=x[i]*y[i]
    sx2+=x[i]**2
    sy2+=y[i]**2
   
n=10
r = (n*sxy-sx*sy)/(math.sqrt(n*sx2-sx**2)*math.sqrt(n*sy2-sy**2))
print("The Correlation Coefficient is %.3f"%r)
byx=(n*sxy-sx*sy)/(n*sx2-sx**2)
xmean=sx/n
ymean=sy/n
print("the reg line Y on x : Y=%0.3f %0.3f(X-%0.3f)"%(ymean,byx,xmean))
plt.scatter(x,y)
def Reg(x):
    return ymean+byx*(x-xmean)
x=np.linspace(20,40,51)
y1=Reg(x)
plt.plot(x,y1,'r')
plt.xlabel("x-data")
plt.ylabel("y-label")
plt.legend(['REGRESSION LINE', 'DATA POINTS'])
plt.show()
```

# Output : 
<img width="330" height="200" alt="maths" src="https://user-images.githubusercontent.com/75234646/170188636-e64f13f3-205b-4800-9fdb-55a6ad34e6e4.png">

# Result:
Thus the given data has been analysed and coeffificient of correlation has been found and regression line is plotted .
