# EX 2C BACKTRACKING- SUBSET SUM PROBLEM
## DATE:11-07-2025
## AIM:
To demonstrate that the sum of the subset of a given set is equal to the given sum.


## Algorithm


1. Input the number of elements (`size`).  
2. Input `size` elements into list `a`.  
3. Input the `target` sum.  
4. Define recursive function `SubsetSum(a, i, sum, target, n)`.  
5. If `i == n`, return `sum == target`.  
6. If `sum > target`, return `False`.  
7. If `sum == target`, return `True`.  
8. Recursively return `SubsetSum(a, i+1, sum, target, n) or SubsetSum(a, i+1, sum + a[i], target, n)`.  
9. Print list `a` and result message based on the function's return value.  


## Program:
```
/*
Program to implement Subset sum problem.
Developed by: GANESH PRABHU J
Register Number: 212223220023
*/
```
```PY
def SubsetSum(a,i,sum,target,n):
    if i==n:
        return sum==target
    if sum>target:
        return False
    if sum==target:
        return True
    return SubsetSum(a,i+1,sum,target,n) or SubsetSum(a,i+1,sum+a[i],target,n)

a=[]
size=int(input())
for i in range(size):
    x=int(input())
    a.append(x)

target=int(input())
n=len(a)
if(SubsetSum(a,0,0,target,n)==True):
    for i in range(size):
        print(a[i])
    print("True,subset found")
else:
    for i in range(size):
        print(a[i])
    print("False,subset not found")


```
## Output:

![image](https://github.com/user-attachments/assets/261e25e9-791c-484b-98e4-a3037400fb8c)

## Result:
The Subset Sum program executed successfully, and the result was determined based on whether a subset matching the target sum was found or not.
