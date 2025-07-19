"""
Write a program that finds all the prime pairs between given positive numbers A and B exclusively (0 < A < B < 10,000). 
A prime pair is composed of two prime numbers that have difference of two. Input has two integers, A and B. 
In the output, the first line is the number of prime pairs, the prime pairs is printed in the remaining lines in increasing order.
"""


# Read A and B from one line without using map
line = input()
parts = line.split()
A = int(parts[0])
B = int(parts[1])

# Generate primes between A and B (exclusive)
primes = []
for num in range(A + 1, B):
    is_prime = True
    if num < 2:
        is_prime = False
    else:
        i = 2
        while i * i <= num:
            if num % i == 0:
                is_prime = False
                break
            i += 1
    if is_prime:
        primes.append(num)

# Find prime pairs with difference of 2
pairs = []
i = 0
while i < len(primes) - 1:
    if primes[i + 1] - primes[i] == 2:
        pairs.append((primes[i], primes[i + 1]))
    i += 1

# Output result
print(len(pairs))
for p in pairs:
    print(p[0], p[1])
