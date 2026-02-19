# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
1.Personal computer

2.Colab
# Program:
```
import math

n = int(input("Enter the number of Samples : "))
p = [float(input(f"Enter the probability of sample values {i+1}: ")) for i in range(n)]
lk = [float(input(f"Enter the length of the sample values {i+1}: ")) for i in range(n)]

L = sum(p[i]*lk[i] for i in range(n))
hs = round(sum(p[i]*math.log2(1/p[i]) for i in range(n)), 3)
eff = round(hs/L, 3)
red = round(1-eff, 3)
var = round(sum(p[i]*(lk[i]-L)**2 for i in range(n)), 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")

```
# Calculation:

<img width="724" height="984" alt="Screenshot 2026-02-19 161050" src="https://github.com/user-attachments/assets/88ff74f9-5eb0-4955-bb69-fef1f82bab76" />

<img width="747" height="1001" alt="Screenshot 2026-02-19 161112" src="https://github.com/user-attachments/assets/5de906e6-01e8-446b-8c15-7af7080676f7" />

# Output

<img width="871" height="527" alt="image" src="https://github.com/user-attachments/assets/2ba45418-9c58-477a-b783-74515dc94776" />

# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
