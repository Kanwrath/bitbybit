## Day 1 - Working with Varibles in Python to ManageData
### Working with Print Function

    print ("Hello, World!")

### Write a program in main.py that prints the same notes from the previous lesson using what you have learnt about the Python 
``` python  
print function
print("Day 1 - Python Print Function")
print("The function is declared like this:")
print('print("what to print")')
```
### Print multiple lines in one string using \n to Line Break
``` python
print ("Hello, World!\nHello, World!")
```
### Combine strings with + sign
``` python
print("Hello" + "Branden")
```
### Add space with + sign to space out strings
``` python
print("Hello " + "Branden")
```
### or
``` python
python
print("Hello" + " Branden")
```
### or
``` python
print("Hello" + " " + "Branden")
```
### Working with Input in Python
``` python
print ("Hello" + input("What is your name?") + "!")
```
### Length of input presented to user
``` python
print(len(input("What is your name?")))
```
### Working with Varibles in Python 
### This shows how variables can be changed, As the code runs, this variable name changes values and when this is ran the output changes accordingly with this change
``` python
name = "Jack"
print(name)

name = "Angela"
print(name)

name = input("What is your name?")
length = len(name)
print(length)
```
### Day 1 Code Challenge - Band Name Generator
### This program will take user provided City name and Pet name and create a band name for the user
``` python
    print("Hello, this is a band name generator so you can name your rad new band!")
    city_name = input("What is the name of a city that you grew up in?\n ")
    pet_name = input("What is the name of a pet that you have had in your life?\n ")
    print("This is the name of your band! The "+ city_name + " " + pet_name + "'s")
```
