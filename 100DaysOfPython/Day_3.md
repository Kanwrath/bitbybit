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
### Longer example of code block using all the Operators from this module
``` python
print("Welcome to the rollercoaster!")
height = int(input("What is your height in cm? "))
bill = 0

if height >= 120:
  print("You are tall enough to ride roller     coaster.\n Enjoy the Ride!")
  age = int(input("What is your age? "))
  if age < 12:
    bill = 5
    print("Please pay $5.")
  elif age <= 18: 
    bill = 7
    print("Please pay $7.")
  else:
    bill = 12
    print("Please pay $12.")
    
  wants_photo = input("Do you wantr a photo taken? Y or N")
  if wants_photo == "Y"
  #Add $3 to the bill
  bill = bill + 3
  #or write bill += 3. This is short hand for adding value to most recently held value of the variable. 

print(f"Your final bill is ${bill}")
else:
  print(" Sorry you need to grow a little more before riding the rollercoaster.\n Please come back in a few years!")
```

### Day 3 challenge - Build an automatic pizza order program.

Parameters:
Based on a user's order, work out their final bill.

* Small Pizza: $15

* Medium Pizza: $20

* Large Pizza: $25

* Pepperoni for Small Pizza: +$2

* Pepperoni for Medium or Large Pizza: +$3

* Extra cheese for any size pizza: + $1

``` python
#Don't change the code below
print("Welcome to Python Pizza Deliveries!")
size = input("What size pizza do you want? S, M, or L ")
add_pepperoni = input("Do you want pepperoni? Y or N ")
extra_cheese = input("Do you want extra cheese? Y or N ")
#Don't change the code above

#Write your code below this line
#Define price variable for if statements to reference
price = 0

#Nested if statements
if size == "S":
 price += 15
elif size == "M":
 price += 20
#if user does not pick S or M then it will be L so use Else statement for this
else:
 price += 25
#if the user adds pepperoni to small pizza add $3
if add_pepperoni == "Y":
 if size == "S":
  price += 2
 #The addiitonal cost for pepperoni is the same for M & L so use else statement
 else:
    price += 3
#The cost for extra cheese is the same for all pizza sizes so use on if statement to ad $1 to the total
if extra_cheese == "Y":
    price += 1

print (f"Your final bill is: ${price}")
```
### Day 3 - Logical Operators

* And
  - Logical AND: True if both the operands are true
* Or
  - Logical OR: True if either of the operands is true
* Not
  - Logical NOT: True if operand is false
