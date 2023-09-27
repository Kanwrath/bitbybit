## Day 3 - Conditional Statements, Logical Operators, Code Blocks and Scope

### Control Flow with Conditional Operators
* If / Else: If this condition is present then do this action, else perform this action
``` python
print("Welcome to the rollercoaster!")
height = int(input("What is your height in cm? "))
if height > 120:
  print("You are tall enough to ride roller coaster.\n Enjoy the Ride!")
else:
  print(" Sorry you need to grow a little more before riding the rollercoaster.\n Please come back in a few years!")
```
* Comparison Operators
    - ">:" Greater than
    - "<:" Less than
    - ">=" Greater than or equal to
    - "<=" Less than or equal to
    - "==" Check if value equals assigned value

### Day 2 - Coding Challenege - Write a program that works out whether if a given number is an odd or even number.

* Modulo Operation - %
    - Gives you the remainder after division is complete
 
``` python
#Don't change the code below
number = int(input("Which number do you want to check? "))
#Don't change the code above
if number % 2 == 0:
    print("This is an even number.")
else: 
    print("This is an odd number.")
```
### Nested if statements and elif statements
* Computer reads the first if condition and if it is true goes to end otherwise it goes to the nested statement. 
``` python
if condition:
  elif another condition:
     do this
else:
  do this
```
``` python
print("Welcome to the rollercoaster!")
height = int(input("What is your height in cm? "))

if height >= 120:
  print("You are tall enough to ride roller     coaster.\n Enjoy the Ride!")
  age = int(input("What is your age? "))
  if age < 12:
    print("Please pay $5.")
  elif age <= 18: 
    print("Please pay $7.")
  else:
    print("Please pay $12.")
else:
  print(" Sorry you need to grow a little more before riding the rollercoaster.\n Please come back in a few years!")
```
### Day 2 - Coding Challenege - BMI 2.0. 
### Write a program that interprets the Body Mass Index (BMI) based on a user's weight and height.

It should tell them the interpretation of their BMI based on the BMI value.

* Under 18.5 they are underweight
* Over 18.5 but below 25 they have a normal weight
* Over 25 but below 30 they are slightly overweight
* Over 30 but below 35 they are obese
* Above 35 they are clinically obese.

``` python 
#Don't change the code below
height = float(input("enter your height in m: "))
weight = float(input("enter your weight in kg: "))
#Don't change the code above

#Write your code below this line
height = float(height)
weight = int(weight)
BMI = round(weight / (height**2))
if BMI < 18.5:
  print(f"Your BMI is {BMI}, you are underweight.")
elif BMI < 25:
    print(f"Your BMI is {BMI}, you have a normal weight.")
elif BMI < 30:
    print(f"Your BMI is {BMI}, you are slightly overweight") 
elif BMI < 35:
    print(f"Your BMI is {BMI} you are obese")
else:
    print(f"Your BMI is {BMI}, you are clinically obese")
```
### Day 2 - Coding Challenege - Write a program that works out whether if a given year is a leap year

* Conditions for leap year
  - on every year that is evenly divisible by 4 

  - **except** every year that is evenly divisible by 100 

  - **unless** the year is also evenly divisible by 400
 
  Use nested if statements as noted below

  ``` python
  #Don't change the code below
  year = int(input("Which year do you want to check? "))
  #Don't change the code above

  #Write your code below this line
  if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print("Leap year")
        else:
            print("Not leap year")
    else:
        print("Leap year")
  else:
    print("Not leap year")
  ```
### Multiple if conditions
as opposed to if/elif/else where only one of the items will happen, when using if/if/if all conditions will be executed
``` python
if condition:
  elif another condition:
     do this
else:
  do this
#
#VS
#
if condition
do this
if condition
and do this
if condition
and do this
```
