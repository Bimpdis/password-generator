# password-generator
Second attempt at creating a unique password generator

```python
# D = Today’s Date.
# C = 121206 (Code).
# N = Employee Number.
# Correct Password = print(D+C+N).
```

```python
import datetime

# Get the current date and time
now = datetime.datetime.now()

# Use today's date as integer for 'Correct_Date'
Correct_Date = int(now.strftime("%d%m%y"))

# Correct Date - delete when in use
print(Correct_Date)

# Enter day and month in numerical sequence, no characters.
D = int(input("Please Enter Number: ")) 

# If the entered number is too large, print ‘False’. 
if D <Correct_Date:
    D = 0
    print("False")
# If the number is too small, print ‘False’.
elif D >Correct_Date:
    D = 0
    print("False") 
# If the number matches the date, print ‘True’.
elif D ==Correct_Date:
    print("True") 


# Static code
Correct_Code = 121206

 # Enter unchangeable code.
C = int(input("Please Enter Code: "))

# If the number is too large, print ‘Alert System’.
if C <121206:
    C = 0
    print("Alert System")
# If the number is too small, print ‘Alert System’. 
elif C >121206:
    C = 0
    print("Alert System")
# If the number matches the code, print ‘True’. 
elif C ==121206:
    print("True") 


# Ensure neither Correct_Code or Correct_Date are revealed when there's an error.
if C == 0:
    D = 0
if D == 0:
    C = 0
E = D + C

print(E)

# Enter Employee Number. 
Employee_Number = int(input("Please Enter Employee Number: "))

# List of valid Employee Names and numbers.
Employee1 = 1000
Employee2 = 2000
Employee3 = 3000
Employee4 = 4000
Registered_Employee_Names = [Employee1, Employee2, Employee3, Employee4]


# Identify if number is in list
if Employee_Number in Registered_Employee_Names:
    print("True")
else:
    print("False")

# Last code entered
if Employee_Number in Registered_Employee_Names:
    N = Employee_Number
    print(N)
else:
    print("Create Guest Password?")



print(D+C+N) #Correct Password
```


- make D changeable, using definitive calendar - COMPLETE
- make C and N change D in slices so only ever single digit answer (0-9)
- make sure C error doesn’t reveal D data - COMPLETE
- N is changeable, no matter if it's entered incorrectly. Automated code that is performed separately will produce definitive code per employee per day, regardless of user error.
- include extra number to define day of the week so codes don’t repeat annually
