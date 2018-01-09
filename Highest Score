import operator
import random
from datetime import datetime
import csv
# Into
print('Welcome to the program')
# assigns necessary values
i = 1
x = 1
Number = 4
AName = [0] * Number
ATest1 = [int(0)] * Number
ATest2 = [int(0)] * Number
ATest3 = [int(0)] * Number
ATotal = [int(0)] * Number
Highest = [0] * 2
HighestMarks = [int(0)] * Number
HighestName = [int(0)] * Number
Key = 1
Counter = 1
High = 1
tempHighest = 1

# Function 1, Gets students name and validates them
def studentName(x):
    global Key
    while True:
        if x.isalpha():
            AName[Key - 1] = str(x)
            return AName[Key - 1]
        else:
            print("please use characters only,"),
            x = input("Try again: \n")
    
# Function to get and validate input for test 1
def studentT1(x):
    global Key
    while True:
        if x.isdigit() and 0 <= int(x) <= 20:
            ATest1[Key - 1] = x
            return ATest1[Key - 1]
        else:
            print("please enter a valid integer in the range of 0 - 20:\n")
            x = input()
            continue

# Function to get and validate input for test 2
def studentT2(x):
    global Key
    while True:
        if x.isdigit() and 0 <= int(x) <= 25:
            ATest2[Key - 1] = x
            return ATest2[Key - 1]
        else:
            print("please enter a valid integer in the range of 0 - 25:\n")
            x = input()
            continue
    
# Function to get and validate input for test 3
def studentT3(x):
    global Key
    while True:
        if x.isdigit() and 0 <= int(x) <= 35:
            ATest3[Key - 1] = x
            return ATest3[Key - 1]
        else:   
            print("please enter a valid integer in the range of 0 - 35:")
            x = input()
            continue
    
# Function to work out the class average
def classAverage():
    classAverage = sum(ATotal) / Number
    return classAverage

# Function to print out the name and marks in a loop
def nameMark():
    counter = 1
    for i in range(Number):
        print("")
        print(str(counter), '.', str(AName[counter - 1])),
        print('Total score: ', str(ATotal[counter - 1]))
        print(" ")
        counter += 1
    
# Function to work out each students total mark, and compare it to the highest so far
def Marks():
    global Key, ATest1, ATest2, ATest3, Highest, High, tempHighest, HighestName, HighestMarks, tempATotal
    ATotal[Key - 1] = float(ATest1[Key - 1]) + float(ATest2[Key - 1]) + float(ATest3[Key - 1])
    tempATotal = (ATotal[Key - 1])

def same():
    global ATotal, AName, HighestMarks, HighestName, High
    HighestMarks[x] = ATotal[Key - 1]
    HighestName[x] = AName[Key - 1]
    x += 1
    High += 1
    
def sameOrNor():
    global tempHighest, tempATotal, AName, High, HighestMarks, HighestName, Highest, x
    if tempHighest == tempATotal:
        HighestMarks[x] = ATotal[Key - 1]
        HighestName[x] = AName[Key - 1]
        x += 1
        High += 1
        return HighestMarks, HighestName, High
    elif tempHighest < tempATotal:
        Highest[1] = ATotal[Key - 1]
        Highest[0] = AName[Key - 1]
        HighestName[0] = AName[Key - 1]
        HighestMarks[0] = ATotal[Key - 1]
        tempHighest = tempATotal
        return HighestMarks, HighestName, tempHighest
    
def highestTotal():
    global High, i, HighestName, HighestMarks
    i = 1
    while True:
        if High >= 1:
            print(str(i), '. ', str(HighestName[i - 1]))
            print(str(HighestMarks[i - 1]))
            print("")
            High -= 1
            i += 1
        else:
            break
        
# Calls the functions to get student names and marks and work out totals in a loop
def start():
    global Key
    a = input("Please enter the name of student number " + str(Counter) +
    ":\n ")
    studentName(a)
    b = input("Please enter the mark of Test 1:\n ")
    studentT1(b)
    c = input("Please enter the mark of Test 2:\n ")
    studentT2(c)
    d = input("Please enter the mark of Test 3:\n ")
    studentT3(d)
    Marks()
    sameOrNor()
    Key += 1

# Program starts here
# Calls the start function 30 times to get 30 names in loop
for i in range(Number):
    start()
    Counter += 1
    
# Calls the function to print out each students name and mark
nameMark()
print("The Class Average is: " + str(classAverage()))
print("The student(s) with the highest mark and their name: ")
highestTotal()
print("The students with the highest mark and there name: " +
str(HighestName[0]) + " -", str(HighestMarks[0]))
