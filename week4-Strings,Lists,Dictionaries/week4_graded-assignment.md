#### question 1:
Fill in the blank to complete the “first_character” function. This function should return the first character of any string passed in.  Complete the string operation needed in this function so that input like "Hello, World" will produce the output "H".
```
def first_character(string):
    # Complete the return statement using a string operation.
    return string[0]


print(first_character("Hello, World")) # Should print H
print(first_character("Python is awesome")) # Should print P
print(first_character("Keep going")) # Should print K
```

#### question 2:
Complete the for loop and string method needed in this function so that a function call like "alpha_length("This has 1 number in it")" will return the output "17". This function should:

accept a string through the parameters of the function;

iterate over the characters in the string;

determine if each character is a letter (counting only alphabetic characters; numbers, punctuation, and spaces should be ignored);

increment the counter;

return the count of letters in the string.

```
def alpha_length(string):
    character = ""
    count_alpha = 0
    # Complete the for loop sequence to iterate over "string".
    for letter in string: 
        # Complete the if-statement using a string method. 
        if letter.isalpha():
            count_alpha += 1  
    return count_alpha
 
print(alpha_length("This has 1 number in it")) # Should print 17
print(alpha_length("Thisisallletters")) # Should print 16
print(alpha_length("This one has punctuation!")) # Should print 21
```


#### question 3:
Consider the following scenario about using Python lists: 

A professor gave his two assistants, Aniyah and Imani, the task of keeping an attendance list of students in the order they arrived in the classroom. Aniyah was the first one to note which students arrived, and then Imani took over. After class, they each entered their lists into the computer and emailed them to the professor. The professor wants to combine the two lists into one and sort it in alphabetical order. 

Complete the code by combining the two lists into one and then sorting the new list. This function should:

accept two lists through the function’s parameters;,

combine the two lists;

sort the combined list in alphabetical order;

return the new list. 
```
def alphabetize_lists(list1, list2):


  new_list = [] # Initialize a new list.
  list1.extend(list2) # Combine the lists.
  list1.sort() # Sort the combined lists.
  new_list = list1 # Assign the combined lists to the "new_list".
  return new_list 


Aniyahs_list = ["Jacomo", "Emma", "Uli", "Nia", "Imani"]
Imanis_list = ["Loik", "Gabriel", "Ahmed", "Soraya"]


print(alphabetize_lists(Aniyahs_list, Imanis_list))
# Should print: ['Ahmed', 'Emma', 'Gabriel', 'Imani', 'Jacomo', 'Loik', 'Nia', 'Soraya', 'Uli']
```

#### question 4:
Fill in the blank to complete the “squares” function. This function should use a list comprehension to create a list of squared numbers (using either the expression n*n or n**2). The function receives two variables and should return the list of squares that occur between the “start” and “end” variables inclusively (meaning the range should include both the “start” and “end” values). Complete the list comprehension in this function so that input like “squares(2, 3)” will produce the output “[4, 9]”.
```
def squares(start, end):
    return [ x**2 for x in range(start, end+1) ] # Create the required list comprehension.


print(squares(2, 3)) # Should print [4, 9]
print(squares(1, 5)) # Should print [1, 4, 9, 16, 25]
print(squares(0, 10)) # Should print [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

#### question 5:
Fill in the blanks to complete the “endangered_animals” function. This function accepts a dictionary containing a list of endangered animals (keys) and their remaining population (values).  For each key in the given “animal_dict” dictionary, format a string to print the name of the animal, with one animal name per line.
```
def endangered_animals(animal_dict):
    result = ""
    # Complete the for loop to iterate through the key and value items 
    # in the dictionary.    
    for animal in animal_dict.keys(): 
        # Use a string method to format the required string.
        result += "{}\n".format(animal) 
    return result


print(endangered_animals({"Javan Rhinoceros":60, "Vaquita":10, "Mountain Gorilla":200, "Tiger":500}))

# Should print:
# Javan Rhinoceros
# Vaquita
# Mountain Gorilla
# Tiger
```

#### question 6:
Consider the following scenario about using Python dictionaries: 

Tessa and Rick are hosting a party. Both sent out invitations to their friends, and each one collected responses into dictionaries, with names of their friends and how many guests each friend was bringing. Each dictionary is a partial guest list, but Rick's guest list has more current information about the number of guests. 

Complete the function to combine both dictionaries into one, with each friend listed only once, and the number of guests from Rick's dictionary taking precedence, if a name is included in both dictionaries. Then print the resulting dictionary. This function should:

accept two dictionaries through the function’s parameters;

combine both dictionaries into one, with each key listed only once;

the values from the “guests1” dictionary taking precedence, if a key is included in both dictionaries;

then print the new dictionary of combined items.

```
def combine_guests(guests1, guests2):
  guests2.update(guests1) # Use a dictionary method to combine the dictionaries.
  return guests2

Ricks_guests = { "Adam":2, "Camila":3, "David":1, "Jamal":3, "Charley":2, "Titus":1, "Raj":4}
Tessas_guests = { "David":4, "Noemi":1, "Raj":2, "Adam":1, "Sakira":3, "Chidi":5}

print(combine_guests(Ricks_guests, Tessas_guests))
# Should print:
# {'David': 1, 'Noemi': 1, 'Raj': 4, 'Adam': 2, 'Sakira': 3, 'Chidi': 5, 'Camila': 3, 'Jamal': 3, 'Charley': 2, 'Titus': 1}

```

#### question 7:
Use a dictionary to count the frequency of numbers in the given “text” string. Only numbers should be counted. Do not count blank spaces, letters, or punctuation. Complete the function so that input like "1001000111101" will return a dictionary that holds the count of each number that occurs in the string  {'1': 7, '0': 6}. This function should: 

accept a string “text” variable through the function’s parameters;

initialize an new dictionary;

iterate over each text character to check if the character is a number’

count the frequency of numbers in the input string, ignoring all other characters;

populate the new dictionary with the numbers as keys, ensuring each key is unique, and assign the value for each key with the count of that number;

return the new dictionary.
```
def count_numbers(text):
  # Initialize a new dictionary.
  dictionary = {}
  # Complete the for loop to iterate through each "text" character.
  for character in text:
    # Complete the if-statement using a string method to check if the
    # character is a number.
    if character.isnumeric():
      # Complete the if-statement using a logical operator to check if 
      # the number is not already in the dictionary.
      if character not in dictionary:
           # Use a dictionary operation to add the number as a key
           # and set the initial count value to zero.
           dictionary[character] = 0
      # Use a dictionary operation to increment the number count value 
      # for the existing key.
      dictionary[character] += 1
  return dictionary

print(count_numbers("1001000111101"))
# Should be {'1': 7, '0': 6}

print(count_numbers("Math is fun! 2+2=4"))
# Should be {'2': 2, '4': 1}

print(count_numbers("This is a sentence."))
# Should be {}

print(count_numbers("55 North Center Drive"))
# Should be {'5': 2}
```

#### question 8:
What do the following commands return when genre = "transcendental"?
```
print(genre[:-8])
print(genre[-7:9])
```

- ran, ental
- **transc, nd**
- endental, tr
- dental, trans

#### question 9:
What does the list "music_genres" contain after these commands are executed?
```
music_genres = ["rock", "pop", "country"]
music_genres.append("blues")
```
- ['rock', 'pop', 'blues']
- ['rock', 'blues', 'pop', 'country']
- **['rock', 'pop', 'country', 'blues']**
- ['rock', 'blues', 'country']

#### question 10:
What do the following commands return?
```
host_addresses = {"router": "192.168.1.1", "localhost": "127.0.0.1", "google": "8.8.8.8"}
host_addresses.keys()
```

- dict_keys(['192.168.1.1', '127.0.0.1', '8.8.8.8'])
- dict_keys(["router", "192.168.1.1", "localhost", "127.0.0.1", "google", "8.8.8.8"])
- **dict_keys(['router', 'localhost', 'google'])**
- dict_keys({"router": "192.168.1.1", "localhost": "127.0.0.1", "google": "8.8.8.8"})

