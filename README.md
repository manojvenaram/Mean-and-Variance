#  Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


# Experiment :

![image](https://user-images.githubusercontent.com/103921593/229993174-5b67e57e-3e01-4ac4-9f83-410a932b22bf.png)

# Program :
```
import numpy as np
L=[int(i) for i in input().split()]
N=len(L)
M=max(L)
x=list()
f=list()
for i in range(M+1):
  c=0
  for j in range(N):
    if L[j]==i:
      c+=1
  f.append(c)
  x.append(i)
# print(f,x)
sf=np.sum(f)
print(sf)
p=list()
for i in range(M+1):
  p.append(f[i]/sf)
k=w=0

for i in range(M+1):
  k+=x[i]*p[i]
print("MEAN %.3f: "%k)
for i in range(M+1):
  w+=((x[i]**2)*p[i])
print("E(X^2) %.3f: "%w)
# mean=np.inner(x,p)
# EXP2=np.inner(x,p)
# var=EXP2-mean**2
var=w-k**2
print("VARIANCE %.3f: "%var)
sd=np.sqrt(var)
print("STANDARD DEVIATION: %.3f"%sd)

```

# Output :
![](exp1.png)
# Results  
The Mean and variance of arrivals of objects from feeder using probability distribution is calculated. 
