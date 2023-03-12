#### question 1:
How are while loops and for loops different in Python?

- While loops can be used with all data types, for loops can only be used with numbers.
- For loops can be nested, but while loops can't.
- **While loops iterate while a condition is true, for loops iterate through a sequence of elements.**
- While loops can be interrupted using break, for loops using continue.

<br>

#### question 2:
Which option would fix this for loop to print the numbers 12, 18, 24, 30, 36?

correct option:
```
for n in range(6,18+1,3):
    print(n*2)
```

<br>


### question 3:
Which for loops will print all even numbers from 0 to 18? Select all that apply.

```
for n in range(19):
    if n % 2 == 0:
        print(n)
```

```
for n in range(10):
    print(n+n)
```

<br>

#### question 4:
Fill in the blanks so that the for loop will print the first 10 cube numbers (x**3) in a range that starts with x=1 and ends with x=10.

```
for x in range(1, 11):
  print(x**3)
```

<br>

#### question 5:
Write a for loop with a three parameter range() function that prints the multiples of 7 between 0 and 100. Print one multiple per line and avoid printing any numbers that aren't multiples of 7. Remember that 0 is also a multiple of 7. 

```
for x in range(0, 101, 7): 
    print(x)
```

