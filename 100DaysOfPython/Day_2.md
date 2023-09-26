##  Day 2 - Understanding Data Types and How to Manipulate Strings

### [Data Types;](https://www.w3schools.com/python/python_datatypes.asp) Strings, Boolean, Integers, Float. #Data Types

* Strings: Anything within single, double or triple quotes will be treated as a string.

* Integers: Whole numbers without decimal places.

* Float: Floating Point Number. Number with a decimal place such as Pi 3.14159.

* Boolean: True or False.

* Type: Use to check the data type you're working with
``` python
a = str(123)
print(type(a))
```
This will print <class 'str'>

Type Conversion / Casting: Change/convert the data type you're working with
``` python
print(70 + float("100.5"))
```
This will change the Integer 70 and print out the float value to 170.5

### Day 2 Exercise - Write a program that adds the digits in a 2 digit number.
```python

two_digit_number = input("Type a two digit number: ")

#Write your code below this line
#print(type(two_digit_number)) - check type
#segment out the input to separate digits with index
f_d = int(two_digit_number[0])
s_d = int(two_digit_number[1])
two_digit_number = f_d + s_d
print(two_digit_number)
#or change input to list, then call int to change type and define index place for digits 
b = list(two_digit_number)
print(int(b[0])+int(b[1]))
```
### Mathematical Operations in Python

* Addition (+)
* Subtraction (-) 
* Multiplicattion (*)
* Division (/) - Always results in a float data type
* Exponent represented by double * i.e. 2^2 = 2**2
* Follows PEMDAS with slightly varied prioritization of order of operations
  - Parentheses
  - Exponents
  - Multiplication and Division are weighted under same priority and evaluated form left to right order
  - Addition and Subtraction are also weighted under same priority and evaluated from left to right.
  - You can use Paretheses to change/elevate the Mathematical Operation order.
``` python
print (3 * 3 / 3 + 3 - 3)
#Checked for parentheses, none
#Checked for Exponents, None
#Then read left to right likee: 3 * 3 = 9, 3 / 3 = 1
#Left with 10 + 3 - 3, read left to right so answer is 7
```
### Day 2 Exercise - Write a BMI Calculator
``` python
#Don't change the code below
height = input("enter your height in m: ")
weight = input("enter your weight in kg: ")
#Don't change the code above

#Write your code below this line
height = float(height)
weight = int(weight)
BMI = int(weight / (height**2))
print(BMI)
```
### Number Manipulation and F Strings in Python 

* Round function is used to round float numbers
  - Example:
  ``` python
  print (round(8 / 3))
  #Also can set the decimal plact to round by specifying place with , [insert_integer]
  print (round(8 / 3, 2))
  #This will round to the second decimal place
  ```
* Floor Division: using // rather than /. Cuts off any additional digits, changes data type to Integer number
  - Note: Division using / results in Float number
* When calling a value again, can manipulate present value off of previuous value using +=.-=. etc.
  ``` python
  score = 0
  #if you want to add 1 to the score value based off previous value write this
  score += 1
  #same goes for subtracting
  score -= 1
  ```
* F Strings: Rather than converting a bunch of different data types i prefix f string before the string.
    ``` python
    score = 0
    height = 1.5
    isWinning = True
    print(f"your score is {score, youre height is {height}, you are winning is {isWinning}")
    ```
### Day 2 Exercise - Create a program using maths and f-Strings that tells us how many days, weeks, months we have left if we live until 90 years old.
``` python
#Don't change the code below
age = input("What is your current age? ")
#Don't change the code above

#Write your code below this line
age = int(age)
daysLeft = ((90 * 365) - (age * 365))
weeksLeft =((90 * 52) - (age * 52))
monthsLeft = ((90 * 12) - (age * 12))
print(f"You have {daysLeft} days, {weeksLeft} weeks, and {monthsLeft} months left.")
```
### Day 2 Coding Challenge - Tip Calculator

``` python
#Tip Calculator
#Inputs - If the bill was $150.00, split between 5 people, with 12% tip. 
#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60
#Tip: There are 2 ways to round a number. You might have to do some Googling to solve this.

#Write your code below this line
bill_total = float(input("What is the total amount of the bill? " ))
total_people = int(input("How many people is this amount split between? "))
bill_tip = int(input("How much tip % would you like to give? 10, 12, 15, or 20? "))
tip_as_percent = bill_tip / 100 + 1
amount_owed = round((bill_total / total_people) * tip_as_percent, 2)
amount_owed = format(amount_owed, ".2f")
print(f"Each person should pay: ${amount_owed}")
```
