## JUSTDIAL (Manual Testing)

https://docs.google.com/spreadsheets/d/11qEDleN0FUnEEn5bkuPphq-Mz0ox23Yuech_V3_JNVs/edit?usp=sharing

## Manual Testing Exercise :

https://docs.google.com/spreadsheets/d/1KD4KbGxn93QfRMy9FRZF4MR4ar3G-BviYhQAOdUKxzk/edit?usp=sharing


## Python Code:

Write a Python program which accepts a sequence of comma separated 4 digit
binary numbers as its input and then check whether they are divisible by 5 or not.
The numbers that are divisible by 5 are to be printed in a comma separated
sequence.
Example:
0100,0011,1010,1001
Then the output should be:
1010

```
n=input().split(",")
res=[]

for i in n:
  dec=int(i,2)
  if(dec%5==0):
    res.append(i)

print(",".join(res))
```

Write a Python program that accepts a sentence and calculate the number of
letters and digits.
Suppose the following input is supplied to the program:
hello world! 123
Then, the output should be:
LETTERS 10
DIGITS 3

```

n=input()
count=0
alpha=0
for ch in n:
  if ch.isdigit():
    count=count+1

for ch in n:
  if ch.isalpha():
    alpha=alpha+1


print("digit",count)
print("alpha",alpha)
```

Write a program which can compute the factorial of a given numbers.The
results should be printed in a comma-separated sequence on a single
line.Suppose the following input is supplied to the program:8
Then, the output should be:40320

```
n=int(input())
fact=1
for i in range(1,n+1):
  fact=fact*i;

print(fact)

```
