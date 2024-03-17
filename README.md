# password-generator
First attempt at creating a unique password generator

```python
D = 1303 #Today’s Date.
C = 1212 #Code.
N = 100 #Employee Number.
print(D+C+N) #Correct Password.
```

```python
D = int(input('Please Enter Number: ')) #Enter day and month in numerical sequence, no characters.

if D <1303:
    D = 0
    print('False') #If the number is too large, print ‘False’.
elif D >1303:
    D = 0
    print('False') #If the number is too small, print ‘False’.
elif D ==1303:
    print('True') #If the number matches the date, print ‘True’.

C = int(input('Please Enter Code: ')) #Enter unchangeable code.

if C <1212:
    C = 0
    print('Alert System') #If the number is too large, print ‘Alert System’.
elif C >1212:
    C = 0
    print('Alert System') #If the number is too small, print ‘Alert System’.
elif C ==1212:
    print('True') #If the number matches the code, print ‘True’.

N = int(input('Please Enter Employee Number: ')) #Enter Employee number.

if N <100:
    N = 0
    print('Not Recognised') #If the number is too large, print ‘Not Recognised’.
elif N >100:
    N = 0
    print('Not Recognised') #If the number is too large, print ‘Not Recognised’.
elif N ==100:
    print('True') #If the number matches Employee Number, print ‘True’.

print(D+C+N) #Correct Password
```


- make D changeable, using definitive calendar
- make C and N change D in slices so only ever single digit answer (0-9)
- make sure C error doesn’t reveal D data
- make N changeable
- include extra number to define day of the week so codes don’t repeat annually
