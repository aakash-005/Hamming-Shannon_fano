# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
google colab

# Program:
```
import math

# Probabilities given
p = [0.30, 0.25, 0.20, 0.12, 0.08, 0.05]

# Corresponding Huffman/Shannon-Fano code lengths
lk = [2, 2, 2, 3, 4, 4]

n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)

# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

# Output
print(f"Average Codeword Length is : {L:.3f}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")

```
# Calculation:
<img width="901" height="1280" alt="image" src="https://github.com/user-attachments/assets/d8e6f055-9e7b-4afd-b98a-806b61285424" />
<img width="926" height="1280" alt="image" src="https://github.com/user-attachments/assets/6192ade7-2461-4688-a538-f07a5f7bb732" />
<img width="2818" height="1803" alt="image" src="https://github.com/user-attachments/assets/34c2cc9e-bf28-4f35-a5ec-aeaf834e953e" />






# Output

<img width="439" height="138" alt="image" src="https://github.com/user-attachments/assets/d7824de5-1445-42eb-a932-daabb3684294" />


# Results:
The Huffman and Shannon-Fano coding techniques have been successfully applied to the given source. The average codeword length, entropy, variance, redundancy, and efficiency have been computed.



