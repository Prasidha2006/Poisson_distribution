# Fitting Poisson  distribution

# NAME: PRASIDHA A

# REGISTER NUMBER: 212224230204

# Aim : 

To fit poisson distribution for the arrival of objects per minute from the feeder

# Software required :  

Python and Visual component tool

# Theory:

The Poisson distribution is the discrete probability distribution of the number of events occurring in a given time period, given the average number of times the event occurs over that time period.

![image](https://user-images.githubusercontent.com/104613195/166248326-fd042076-8b0b-40c4-8b11-1d8e8fcb74db.png)

 Conditions for Poisson Distribution:

1. An event can occur any number of times during a time period.
2. Events occur independently. I
3. The rate of occurrence is constant.
4. The probability of an event occurring is proportional to the length of the time period. 
 
# Procedure :

![image](https://user-images.githubusercontent.com/104613195/166251988-d0c53205-6080-4f7b-ae4c-398178586637.png)

# Experiment :

![image](https://user-images.githubusercontent.com/103921593/230282876-f4a5afbf-cac1-4648-a1b0-c78840638a8e.png)

# Program :

 ```
import numpy as np
from scipy.stats import poisson

n = int(input("Enter number of observations: "))
data = [int(input(f"Enter arrivals at minute {i+1}: ")) for i in range(n)]

lam = np.mean(data)

print("\nFitted Poisson Distribution (λ = {:.2f}):".format(lam))
for k in range(0, max(data)+(n-2)):
    prob = poisson.pmf(k, lam)
    print(f"P(X={k}) = {prob:.4f}")

```

# Output : 


<img width="471" height="292" alt="image" src="https://github.com/user-attachments/assets/1cf5a6bb-917e-4fbb-b08e-91bb33aa9097" />


# Results

The Poisson distribution is fitted for the objects arrived from feeder per minute and the data is tested using Chi-square test. 
 
