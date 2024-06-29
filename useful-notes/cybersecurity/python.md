# Python

1. Use `mousepad file.py` to create python file
2.

```
<aside>
```

```
💡 `#!/bin/python3` (add this once creating a python file in Linux to calling out the directory)

</aside>
```

3\. Use `./file.py` || `python3 file.py` to run python file 4. Additional use `#comment` for adding additional information for easy understanding

## Strings

```python
#!/bin/python3

#basic string printing
print("Hello World!")
print('Hello World!')

#triple quote for multi-line
print("""This string runs
multiple lines!""")

#concatenate
print("THis string is " + "awesome!")

#print new line
print('\n')
print('Printing new line out.')
```

Output:

```bash
Hello World!
Hello World!
This string runs
multiple lines!
THis string is awesome!

Printing new line out.
```

## Math

```python
#!/bin/python3

print(50 + 50) #addition
print(50 - 50) #subtraction
print(50 * 50) #multiplication
print(50 / 50) #division
print(50 + 50 - 50 * 50 / 50) #PEMDAS
print(50 ** 2) #exponents
print(50 % 6) #modulos (leftover)
print(50 / 6) #division with remainder (or a float)
print(50 // 6) #no remainder
```

Output

```bash
100
0
2500
1.0
50.0
2500
2
8.33333333334
8
```

## Variables and Methods

## Functions

```python
#!/bin/python3

#function without parameters
def who_am_i(): 
	#local variable
	name = "keshi"
	age = 22
	
	print("My name is " + name + " and I am " + str(age) + " years old.")
	
who_am_i()

#function with parameters
def add_one_hundred(num):
	print(num + 100)
	
add_one_hundred(100)

#function with multiple parameters
def add(x,y):
	print(x+y)

add(7,7)
```

Output:

```python
┌──(k3shi㉿kali)-[~/python]
└─$ python3 func.py
My name is keshi and I am 22 years old.
200
14
```

## Conditional Statements (if / else)

```python
#!/bin/python3

def drink(money):
	if money >= 2:
		return "You've got yourself a drink!"
	else:
		return "No drink for you!"

print(drink(3))
print(drink(1))

#multiple parameters
def alcohol(age, money):
	if (age >= 21) and (money >= 5):
		return "We're getting a drink!"
	elif (age >= 21) and (moeny < 5):
		return "Come back with more money."
	elif (age < 21) and (moeny >= 5):
		return "Nice try, kid!"
	else:
		return "You're too young and too poor."

print(alcohol(21,5))
print(alcohol(21,4))
print(alcohol(20,5))
print(alcohol(20,4))
```

## Lists \[]

```python
#index 0, 1, 2, 3	
movies = ["item1", "item2", "item3", "item4"]

#[1] = index 1 = 2nd element
print(movies[1])
Output: item2

#return 1st index number give right until the last number, 
#but not include the 3rd item
#[postition 1:position 3(excluded)]
print(movies[1:3])

#1st index number until the end, last item in included
print(movies[1:]) 
print(movies[1:]) #last item excluded
print(movies[-1]) #return last item

print(len(movies)) #count items in the list
movies.append("item5") #appends to the end of the list
movies.insert(2, "newItem") #insedrt "newItem" in 2nd position
movies.pop() #removes the last item

#combine list
other_movies = ["item6", "item7"]
combine_movies = movies + other_movies
print(combine_movies)
```

## Tuples

💡 Do not change, ()

```python
grades = ("a", "b", "c", "d", "f")
print(grades[1])
```

## Looping

for loops - start to finish of an iterate

```python
vegetables = ["cucumber", "spinach", "cabbage"]
for x in vegetables;
	print(x);
```

while loops - execute as long as True

```python

i = 1
while i < 10;
	print(i)
	i += 1
```

## Advanced Strings

```python
my_name = "keshi"
print(my_name[0]) #first letter
print(my_name[-1]) #last letter

//split()
sentence = "This is a sentence."
print(sentence[:4]) #zero to four, four excluded
print(sentence.split()) #delimiter - default is a space

//join()
#deconstruct sentences based on delimiter
sentence_split = sentence.split()
sentence_join = ' '.join(sentence_split)
print(sentence_join)

//quote in quote
quote = "He said, 'give me all your money'"
print(quote)
quote = "He said, \"give me all your money\""
print(quote)

//strip() - remove space delimiter
too_much_space = "             hello      "
print(too_much_space.strip())

//lower()
print("A" in "Apple") #True
print("A" in "Apple") #False

letter = "A"
word = "Apple"
print(letter.lower() in word.lower()) 

//format() with emtpy {} method
movie = "The Hangover"
print("My favourite movie is {}.".format(movie))

//% method
print("My favourite movie is %s." % movie)

//f with {word} method
print(f"My favourite movie is {movie}." - most useful

```

Output:

```python
k
i
This
['This', 'is', 'a', 'sentence.']
This is a sentence.
He said, 'give me all your money'
He said, "give me all your money"
hello
True
Flase
True
My favourite movie is The Hangover.
My favourite movie is The Hangover.
My favourite movie is The Hangover.
```

## Dictionaries

💡 key / value pairs {}

```python
#left is key: right is value
drinks = {"Watermelon": 7, "Carrot": 10, "Lemon": 8 } 
print(drinks)

drinks['Watermelon'] = 8
print(drinks)

employees = {"Finance": ["Bob", "Linda", "Tina"], "IT": ["Gene", "Louise", "Teddy"],
							"HR": ["Jimmy Jr.", "Mort"]}
print(employees)

//add
employess['Legal'] = ["Mr. Frond"] #adds new key:value pair
print(employees)

//update
employees.update({"Sales": ["Andie", "Ollie"]}) #adds new key:value pair
print(employees)

//get()
print(drinks.get("Lemon"))
```

Output:

```python
{'Watermelon': 7, 'Carrot': 10, 'Lemon': 8 } 
{'Watermelon': 8, 'Carrot': 10, 'Lemon': 8 } 
{'Finance': ['Bob', 'Linda', 'Tina'], 'IT': ['Gene', 'Louise', 'Teddy'],
	'HR': ['Jimmy Jr.', 'Mort']}
//add
{'Finance': ['Bob', 'Linda', 'Tina'], 'IT': ['Gene', 'Louise', 'Teddy'],
	'HR': ['Jimmy Jr.', 'Mort'], 'Legal': ['Mr. Frond']}
//update
{'Finance': ['Bob', 'Linda', 'Tina'], 'IT': ['Gene', 'Louise', 'Teddy'],
	'HR': ['Jimmy Jr.', 'Mort'], 'Legal': ['Mr. Frond'], 'Sales': ['Andie', 'Ollie']}
//get()
8
```

## Importing Modules

💡 Python modules exist within python and built in but not available without importing.

```python
#!/bin/python3

#system function with parameters
import sys
from datetime import datetime #import datetime feature from datetime
from datetime import datetime as dt #import with alias

print(sys.version)
print(datetime.now())
print(dt.now())
```

Output:

```python
┌──(k3shi㉿kali)-[~/python]
└─$ python3 import.py
3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0]
2024-02-21 17:24:48.359614
2024-02-21 17:24:48.360271
```

## Sockets

💡 Use to make a connection between ports with IP addresses

```python
#!/bin/python3

import socket

HOST = '127.0.0.1'
PORT = 111 #tcp active (netstat -tuln)

#af_inet = ipv4
#sock_stream = port
s = socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.connect((HOST,PORT))
```

```python
┌──(k3shi㉿kali)-[~/python]
└─$ nc -nvlp 111
```

## Building Basic Port Scanner

💡 Make sure that you have a machine (windows) that can check the default gateway / router ip: - to scan open port 53 / 80 - modify script

```python
#!/bin/python3

import sys
import socket
from datetime import datetime

#Define our target

#python3 scanner.py (1st arguments) 192.168.1.1 (2nd arguments)
#if <2 || >2 arguments will break
if len(sys.argv) == 2: 
	#translate hostname to IPv4
	#e.g: python3 scanner.py Punisher
	target = socket.gethostbyname(sys.argv[1]) #argv = IP address
else:
	print("Invalid amount of argumnets.")
	print("SYntax: python3 scanner.py <ip>")

#Add a pretty banner
print("-" * 50)
print("Scanning target: " + target)
print("TIme started: " + str(datetime.now()))
print("-" * 50)

try:
	for port in range(50, 85): #range for dns, http
		s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
		#move on if not respond within a sec
		#to make the script not to takes so long
		socket.setdefaulttimeout(1)
		result = s.connect_ex((target,port))
		if result == 0: #when port is opened
			print(f"Port {port} is open")
		s.close() #close socket connection and continue
except KeyboardInterrupt:
	print("\nExiting program.")
	sys.exit()

except socket.gaierror:
	print("Hostname could not be resolved.")
	sys.exit()

except socket.error:
	print("Could not connect to server.")
	sys.exit()
```

Output:

```python
┌──(k3shi㉿kali)-[~/python]
└─$ python3 scanner.py 192.168.0.1 (gateaway/router ip)
--------------------------------------------------
Scanning target: 192.168.0.1
TIme started: 2024-02-22 00:06:50.078055
--------------------------------------------------
Port 53 is open
Port 80 is open
```

## User Input

```python
#!/bin/python3

x = float(input("Give me a number: "))
o = input("Give me an operator: ")
y = float(input("Give me another number: "))

if o == "+":
	print(x + y)
elif o == "-":
	print(x - y)
elif o == "/":
	print(x / y)
elif o == "*":
	print(x + y)
else:
	print("Unknown operator.")

```

Output:

```python
┌──(k3shi㉿kali)-[~/python]
└─$ python3 input.py
Give me a number: 3
Give me an operator: +
Give me another number: 2
5.0
                                                                                        
┌──(k3shi㉿kali)-[~/python]
└─$ python3 input.py
Give me a number: 3
Give me an operator: %
Give me another number: 2
Unknown operator.
```

## Reading and Writing Files

Read files:

```python
#!/bin/python3

months = open('months.txt')

print(months)
print(months.read())
print(months.readline())
print(months.readline())
months.seek(0)
print(months.readline())

#for loop
for month in months:
	print(month.strip())

months.close

```

Write files:

```python
days = open('days.txt', "w")
days.write("Monday")
days.close()
```

Append files:

```python
days = open('days.txt', "a")
days.write("\nTuesday")
days.close()
```

## Classes and Objects

Employees.py

```python
class Employees:

	def __init__(self, name, department, role, salary, years_employed):
		self.name = name
		self.department = department
		self.role = role
		self.salary = salary
		self.years_employed = years_employed
	
	def eligible_for_retirement(self):
		if self.years_employed >= 20:
			return True
		else:
			return False
		

```

ouremployees.py

```python
#!/bin/python

from Employees import Employees

e1 = Employees("Bob", "Sales", "Director of Sales", 100000, 20)
e2 = Employees("Linda", "Executive", "CIO", 150000, 10)

print(e1.name)
print(e2.role)
print(e1.eligible_for_retirement())
print(e2.eligible_for_retirement())

```

Output:

```python
┌──(k3shi㉿kali)-[~/python]
└─$ python ouremployees.py
Bob
CIO
True
False

```
