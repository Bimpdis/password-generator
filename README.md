# password-generator
Final attempt at creating a rolling password generator

```python
# D = Today’s Date.
# C = 121206 (Code).
# N = Employee Number.
# W = Today's Day of the Week.
# Correct Password = print(D+C+N+W).
```

```python
import datetime

# Get the current date and time.
now = datetime.datetime.now()

# Use today's date as integer for 'Correct_Date'.
Correct_Date = int(now.strftime("%d%m%y"))

# Correct Date - delete when in use.
# print(Correct_Date)

# Enter day, month and year in numerical sequence, no characters (ddmmyy).
D = int(input("Please Enter Number: ")) 

# If the entered number is too large, print ‘False’. 
if D < Correct_Date:
    D = 0
    print("False")
# If the number is too small, print ‘False’.
elif D > Correct_Date:
    D = 0
    print("False") 
# If the number matches the date, print ‘True’.
elif D == Correct_Date:
    print("True") 


# Static code.
Correct_Code = 121206

# Correct Code - delete when in use.
# print(Correct_Code)

 # Enter unchangeable code.
C = int(input("Please Enter Code: "))

# If the number is too large, print ‘Alert System’.
if C < 121206:
    C = 0
    print("Alert System")
# If the number is too small, print ‘Alert System’. 
elif C > 121206:
    C = 0
    print("Alert System")
# If the number matches the code, print ‘True’. 
elif C == 121206:
    print("True") 


# Ensure neither Correct_Code or Correct_Date are revealed when there's an error.
if C == 0:
    D = 0
if D == 0:
    C = 0
E = D + C

# Displays 0 when in error - delete when in use.
# print(E)

# Enter Employee Number. 
Employee_Number = int(input("Please Enter Employee Number: "))

# Approved list of valid employee names and numbers.
# Simple examples for readability. Amend code to import and read a .txt file in practice.
Employee1 = 1000
Employee2 = 2000
Employee3 = 3000
Employee4 = 4000
Registered_Employee_Names = [Employee1, Employee2, Employee3, Employee4]


# Identify if entered number is in approved list.
if Employee_Number in Registered_Employee_Names:
    print("True")
else:
    print("False")

# If entered number is in approved list, the final password is ready to be created.
if Employee_Number in Registered_Employee_Names:
    N = Employee_Number

# Correct Employee_Number - delete when in use.
# print(N)

# If entered number isn't in the approved list, offer to create a "Guest Password".
else:
    print("Create Guest Password?")

Guest_Password = ""

# Use the entered number to create a "Guest Password" using the same formula as an authorised password.
# Previous incorrect entries with a "Guest password" return the same value as the incorrect Employee_Number.
N = Employee_Number or Guest_Password

# Use the numeric value of the current day of the week as an additional layer of code.
W = datetime.datetime.today().weekday()

# Day of the week - delete when in use.
# print(W)

# Create final password.
if C == 0:
    D = 0
if D == 0:
    C = 0
if N == 0:
    E = 0
if E == 0:
    W = 0
E = D + C + N + W

print("Password: ")
print(E)

```


- make D changeable, using definitive calendar - COMPLETE.
- make C and N change D in slices so only ever single digit answer (0-9) - COMPLETE - C and D can only read as 0 in error. N is user input and can still be read.
- make sure C error doesn’t reveal D data - COMPLETE.
- N is changeable, no matter if it's entered incorrectly. Automated code that is performed separately will produce definitive code per employee per day, regardless of user error - COMPLETE.
- include extra number to define day of the week so codes don’t repeat annually - COMPLETE - year is included aswell as a simple precaution.
