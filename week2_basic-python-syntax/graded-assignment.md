#### question 1:

Complete the code to output the statement, “192.168.1.10 is the IP address of Printer Server 1”. Remember that precise syntax must be used to receive credit.

```
IP_address = "192.168.1.10"
host_name = "Printer Server 1"
print(IP_address + " is the IP address of " + host_name)
# Should print "192.168.1.10 is the IP address of Printer Server 1"
```

<br>

#### question 2:

What's the value of this Python expression: "big" > "small"?
- True
- **False**
- Big
- Small
> as alphabetically, b is smaller than s

<br>

#### question 3:
In the following code, what would be the output?
```
number = 4
if number * 4 < 15:
 print(number / 4)
elif number < 5:
 print(number + 3)
else:
 print(number * 2 % 5)
```

output:
7

<br>

#### question 4:
Consider the following scenario about using if-elif-else statements:
The fall weather is unpredictable.  If the temperature is below 32 degrees Fahrenheit, a heavy coat should be worn.  If it is above 32 degrees but not above 50 degrees, then a jacket should be sufficient.  If it is above 50 but not above 65 degrees, a sweatshirt is appropriate, and above 65 degrees a t-shirt can be worn.  
Fill in the blanks in the function below so it returns the proper clothing type for the temperature.

```
def clothing_type(temp):
    if temp > 65:
        clothing = "T-Shirt"
    elif temp > 50 and temp <= 65:
        clothing = "Sweatshirt"
    elif temp > 32 and temp <= 50:
        clothing = "Jacket"
    else:
        clothing = "Heavy Coat"
    return clothing


print(clothing_type(72)) # Should print T-Shirt
print(clothing_type(55)) # Should print Sweatshirt
print(clothing_type(65)) # Should print Sweatshirt
print(clothing_type(50)) # Should print Jacket
print(clothing_type(45)) # Should print Jacket
print(clothing_type(32)) # Should print Heavy Coat
print(clothing_type(0)) # Should print Heavy Coat
```

<br>

#### question 5:
What's the value of the comparison in this if statement? Hint: The answer is not what the code will print. 

```
n = 4
if n*6 > n**2 or n%2 == 0:
    print("Check")

```

- 24 > 16 or 0
- Check
- **True**
- False

<br>

#### questoin 6:
Fill in the blanks to complete the function. The “identify_IP” function receives an “IP_address” as a string through the function’s parameters, then it should print a description of the IP address. Currently, the function should only support three IP addresses and return "unknown" for all other IPs.

```
def identify_IP(IP_address):
    if IP_address == "192.168.1.1":
        IP_description = "Network router"
    elif IP_address == "8.8.8.8" or IP_address == "8.8.4.4":
        IP_description = "Google DNS server"
    elif IP_address == "142.250.191.46":
        IP_description = "Google.com"
    else:
        IP_description = "unknown"
    return IP_description


print(identify_IP("8.8.4.4")) # Should print 'Google DNS server'
print(identify_IP("142.250.191.46")) # Should print 'Google.com'
print(identify_IP("192.168.1.1")) # Should print 'Network router'
print(identify_IP("8.8.8.8")) # Should print 'Google DNS server'
print(identify_IP("10.10.10.10")) # Should print 'unknown'
print(identify_IP("")) # Should Should print 'unknown'
```

<br>

#### question 7:
Can you calculate the output of this code?

```
def sum(x, y):
        return(x+y)
print(sum(sum(1,2), sum(3,4)))
```

output:
10

<br>

#### question 8:
What's the value of this Python expression?
```
x = 5*2

((10 != x) or (10 > x))
```
- True
- **False**
- 15
- 10

<br>

#### question 9:
Fill in the blanks to complete the function. The fractional_part function divides the numerator by the denominator, and returns just the fractional part (a number between 0 and 1). Complete the body of the function so that it returns the right number. Note: Since division by 0 produces an error, if the denominator is 0, the function should return 0 instead of attempting the division.

```
def fractional_part(numerator, denominator):
    # Operate with numerator and denominator to
    # keep just the fractional part of the quotient 
    if denominator == 0 or numerator==0 or numerator==denominator:
        part = 0
    else:
        part = (numerator%denominator)/denominator
    return part


print(fractional_part(5, 5)) # Should print 0
print(fractional_part(5, 4)) # Should print 0.25
print(fractional_part(5, 3)) # Should print 0.66...
print(fractional_part(5, 2)) # Should print 0.5
print(fractional_part(5, 0)) # Should print 0
print(fractional_part(0, 5)) # Should print 0
```

<br>

#### question 10:
Code that is written so that it is readable and doesn’t conceal its intent is called what?

- Obvious cpde
- **Self-documenting code**
- Intentional code
- Maintainable code
