# Huffman & Shannon-Fano
# NAME: SUJITHA ESTHER S
# REG NO: 212224060266
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
# Tools Required:
Python IDE with Numpy and Scipy.

# Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
<img width="820" height="1336" alt="image" src="https://github.com/user-attachments/assets/12bafc9c-a217-4639-bb78-34b115aa3af9" />
<img width="824" height="1298" alt="image" src="https://github.com/user-attachments/assets/07b9d5f4-080f-489f-baac-30d9b043b760" />



# Output
<img width="529" height="302" alt="image" src="https://github.com/user-attachments/assets/211ae8b3-607e-4596-b9a6-c0e54b1f48bb" />


# Results:

The Huffman and Shannon-Fano of the given statistics {0.4,0.2,0.2,0.1,0.1} using python are verified.
