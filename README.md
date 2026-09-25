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

## Date:25/09/2026
## 1. Student Attendance Analysis
A college maintains the daily attendance details of its students in the form of a list containing student IDs. Some students may have attended multiple sessions on the same day. The administration wants to identify the longest continuous sequence of sessions in which no student ID is repeated. Develop a solution that determines the maximum length of such a sequence.

```
stu = [101, 102, 103, 101, 104, 105]
long = 0
for i in range(len(stu)):
    seen = []
    for j in range(i, len(stu)):
        if stu[j] in seen:
            break
        seen.append(stu[j])
        if len(seen) > long:
            long = len(seen)
print(long)
```
## output:
<img width="371" height="210" alt="image" src="https://github.com/user-attachments/assets/f7f11a76-a65e-485b-86d6-98cd4fdd8c75" />

## 2. Online Shopping Price Analysis
An online shopping application stores the prices of products viewed by a customer during a browsing session. The customer wants to identify a continuous range of products that provides the maximum possible total discount value. Given the discount values, determine the maximum value that can be obtained from any continuous range.

```

dis = [2, -1, 3, 4, -2]
max = dis[0]
for i in range(len(dis)):
    total = 0
    for j in range(i, len(dis)):
        total = total + dis[j]
        if total > max:
            max= total
print(max)
```

## Output :
<img width="278" height="199" alt="image" src="https://github.com/user-attachments/assets/11327190-792a-4189-8766-77f0296fba15" />

## 3. Rainwater Collection System
A city installs buildings of different heights along a straight road. During rainfall, water gets collected between taller buildings. The engineering team needs to calculate the total amount of water that can remain trapped after heavy rainfall based on the heights of the buildings.

```
heights = [3, 0, 2, 0, 4]
water = 0
for i in range(len(heights)):
    left = max(heights[:i + 1])
    right= max(heights[i:])
    trapped = min(left, right) - heights[i]
    water = water + trapped
print(water)
```
## Output:

<img width="233" height="253" alt="image" src="https://github.com/user-attachments/assets/6e381a2a-5048-46ff-8275-c13378f0deec" />

## 4. Employee Performance Analysis
A company stores the monthly performance scores of an employee for several months. The scores may contain both positive and negative values depending on the employee's performance. Management wants to identify the continuous period during which the employee achieved the highest overall performance.

```
scores = [2, -1, 3, 4, -2]
max= scores[0]
for i in range(len(scores)):
    total = 0
    for j in range(i, len(scores)):
        total = total + scores[j]
        if total > max:
            max = total
print("Maximum performance:", max)
```

## Output:
<img width="360" height="191" alt="image" src="https://github.com/user-attachments/assets/fd48cd7b-dc37-4b26-a121-3521bccb669d" />

## 5. Product Sales Analysis
A retail company stores the daily sales quantity of a product for several consecutive days. Due to seasonal changes, some days may have negative adjustments. The company wants to identify the period that produced the highest multiplication of sales-related values. Develop a solution to determine this maximum product.

```
sales = [-2, 3, -4]
max = sales[0]
for i in range(len(sales)):
    product = 1
    for j in range(i, len(sales)):
        product = product * sales[j]
        if product > max:
            max = product
print("Maximum product:", max)
```
## output:
<img width="428" height="272" alt="image" src="https://github.com/user-attachments/assets/ad3fa1e8-3800-49f9-a3d5-4101277eec6d" />


