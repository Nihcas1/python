# PROBLEM STATEMENT: 
Find the Majority Element in an Array Write a program to find the majority element in an 
array (an element that appears more than n/2 times). For example, in the array [3, 3, 4, 
2, 4, 4, 2, 4, 4], the output should be 4. Do not use any built-in functions for array 
manipulation or counting. Instructions: Implement a manual count and comparison 
logic to find the majority element. 
 
CODE: 
def major_element(list): 
    count = {} 
     
    for i in list: 
        if i in count: 
            count[i] += 1 
        else: 
            count[i] = 1 
             
    n = len(list) 
    for j in count: 
        if count[j] > n // 2: 
            return j  
     
    return None 
 
 
SAMPLE INPUTS: 
l = [3, 3, 4, 2, 4, 4, 2, 4, 4] 
result = major_element(l) 
if result is not None: 
print("Majority Element:", result) 
else: 
print("No majority element found.") 
OUTPUT: Majority Element: 4 
l = [9, 9, 9, 2, 2, 2, 9] 
result = major_element(l) 
if result is not None: 
print("Majority Element:", result) 
else: 
print("No majority element found.") 
OUTPUT: Majority Element: 9 
l = [1, 2, 3, 4, 5] 
result = major_element(l) 
if result is not None: 
print("Majority Element:", result) 
else: 
print("No majority element found.") 
OUTPUT: No majority element found.
