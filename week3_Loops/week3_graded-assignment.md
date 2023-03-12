#### question 1:
Fill in the blanks to print the numbers from 15 to 5, counting down by fives.

```
# number = 15 # Initialize the variable
# while number >= 5: # Complete the while loop condition
#     print(number, end=" ")
#     number  = number - 5 # Increment the variable

# Should print 15 10 5 

for i in range(15, 4, -5):
    print (i, end=" ")
```

<br>

#### question 2:
Find and correct the error in the for loop below.  The loop should print every even number from 2 to 12.

```
for number in range(2, 13, 2):
    print(number)

# Should print:
# 2
# 4
# 6
# 8
# 10
# 12
```

<br>

#### question 3:
Fill in the blanks to complete the function “digits(n)” to count how many digits the given number has. For example: 25 has 2 digits and 144 has 3 digits. 

Tip: you can count the digits of a number by dividing it by 10 once per digit until there are no digits left.
```
def digits(n):
    count = 0
    if n == 0:
      count += 1
    while n > 0: # Complete the while loop condition
        # Complete the body of the while loop. This should include 
        # performing a calculation and incrementing a variable in the
        # appropriate order.  
        n = n//10
        count += 1

        
    return count
    
print(digits(25))   # Should print 2
print(digits(144))  # Should print 3
print(digits(1000)) # Should print 4
print(digits(0))    # Should print 1
```

<br>

#### question 4:
Fill in the blanks to complete the “rows_asterisks” function. This function should print rows of asterisks (*), where the number of rows is equal to the “rows” variable. The number of asterisks per row should correspond to the row number (row 1 should have 1 asterisk, row 2 should have 2 asterisks, etc.). Complete the code so that “row_asterisks(5)” will print:
```
*

* *

* * *

* * * *

* * * * *
```
```
def rows_asterisks(rows):
    # Complete the outer loop range to control the number of rows
    for x in range(1, rows+1): 
        # Complete the inner loop range to control the number of 
        # asterisks per row
        for y in range(1, x+1): 
            # Prints one asterisk and one space
            print("*", end=" ")
        # An empty print() function inserts a line break at the 
        # end of the row 
        print()


rows_asterisks(5)
# Should print the asterisk rows shown above

```

<br>

#### question 5:
Fill in the blanks to complete the “divisible” function. This function should count the number of values from 0 to the “max” parameter that are evenly divisible (no remainder) by the “divisor” parameter. Complete the code so that a function call like “divisible(100,10)” will return the number “10”.

```
def divisible(max, divisor):
    count = 0 # Initialize an incremental variable
    for x in range(0, max): # Complete the for loop
        if x % divisor == 0:
            count += 1 # Increment the appropriate variable
    return count

print(divisible(100, 10)) # Should be 10
print(divisible(10, 3)) # Should be 4
print(divisible(144, 17)) # Should be 9
```

<br>

#### question 6:
Fill in the blanks to complete the “even_numbers” function. This function should return a space-separated string of all positive even numbers, excluding 0, up to and including the “maximum” variable that's passed into the function. Complete the for loop so that a function call like “even_numbers(6)” will return the numbers “2 4 6”. 
```
def even_numbers(maximum):

    return_string = "" # Initializes variable as a string

    # Complete the for loop with a range that includes all even numbers
    # up to and including the "maximum" value, but excluding 0.
    for i in range(2, maximum+1, 2): 

        # Complete the body of the loop by appending the even number
        # followed by a space to the "return_string" variable.
        return_string += " " + str(i)


        

    # This .strip command will remove the final " " space at the end of
    # the "return_string".
    return return_string.strip() 

print(even_numbers(6))  # Should be 2 4 6
print(even_numbers(10)) # Should be 2 4 6 8 10
print(even_numbers(1))  # No numbers displayed
print(even_numbers(3))  # Should be 2
print(even_numbers(0))  # No numbers displayed
```

<br>
#### question 7:
The following code is supposed to add together all numbers from x to 10.  The code is returning an incorrect answer, what is the reason for this?
```
x = 1
sum = 5
while x <= 10:
    sum += x
    x += 1
print(sum)
# Should print 55
```

- **The "sum" variable is initialized with the wrong value.**
- Should use a for loop instead of a while loop.
- Not incrementing the iterator (x)
- The code is not inside of a function

<br>

#### question 8:
What is the final value of “x” at the end of this for loop? Your answer should be only one number.
```
for x in range(1, 10, 3):
    print(x)
```
output: 7


<br>


#### question 9:
What is the final value of "y" at the end of the following nested loop code? Your answer should be only one number.
```
for x in range(10):
    for y in range(x):
        print(y)
```

output: 8

<br>

#### question 10:
The following code causes an infinite loop. Can you figure out what’s missing and how to fix it?
```
def count_numbers(first, last):
  # Loop through the numbers from first to last 
  x = first
  while x <= last:
    print(x)


count_numbers(2, 6) 
# Should print:
# 2
# 3
# 4 
# 5
# 6
```

- Missing an if-else block
- **Variable x is not incremented**
- Missing the break keyword
- Wrong comparison operator is used
