# Strings & String Operations

```
# Defining strings
single_quoted_string = 'data science'
double_quoted_string = "data science"

# Multi-line strings
multi_line_string = """This is the first line.
and this is the second line
and this is the third line"""

# Raw strings (ignores escape sequences)
raw_string = r"\tThis is a raw string"

# String formatting
first_name = "Joel"
last_name = "Grus"
formatted_string = f"{first_name} {last_name}"  # f-string (Python 3.6+)

# String methods
Name = "-Data Science-"
print(len(Name))  # 14
print(Name.upper())  # Convert to uppercase
print(Name.replace("a", "e"))  # Replace 'a' with 'e'
print(Name.strip("-"))  # Remove '-' from both sides

```

# Lists & List Operations

```
# Lists are ordered and mutable
integer_list = [1, 2, 3]
heterogeneous_list = ["string", 0.1, True]  # Can hold different data types

# Indexing and slicing
x = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(x[0])  # First element
print(x[-1])  # Last element
print(x[:3])  # First three elements
print(x[::2])  # Every second element

# List modification
x.append(10)  # Add element to the end
x.extend([11, 12, 13])  # Add multiple elements
x.insert(1, 99)  # Insert at index 1
x.remove(99)  # Remove first occurrence of value 99

```

# Tuples (Immutable Lists)

```
# Tuples are immutable lists
my_tuple = (1, 2, 3)
print(my_tuple[0])  # Access first element

# Tuples cannot be modified
try:
    my_tuple[1] = 10  # This will raise an error
except TypeError:
    print("Tuples cannot be modified")

```

# Dictionaries (Key-Value Pairs)

```
# Creating dictionaries
grades = {"Joel": 80, "Tim": 95}

# Accessing values
joels_grade = grades["Joel"]  # Direct access
joels_grade_safe = grades.get("Joel", 0)  # Safe access with default

# Adding and modifying values
grades["Kate"] = 100  # Add new key-value pair
grades["Tim"] = 99  # Modify existing value

# Dictionary methods
print(grades.keys())  # Get all keys
print(grades.values())  # Get all values
print(grades.items())  # Get (key, value) pairs

```

# Sets (Unique Elements & Set Operations)

```
# Creating sets
set1 = {1, 2, 3, 4, 5}
set2 = {4, 5, 6, 7, 8}

# Set operations
print(set1.union(set2))  # Combine sets
print(set1.intersection(set2))  # Common elements
print(set1.difference(set2))  # Elements in set1 but not in set2
print(set1.symmetric_difference(set2))  # Elements unique to each set

# Checking membership
print(3 in set1)  # True
print(10 in set1)  # False

```

# Control Flow (If-Else, Loops)

```
# If-Else statement
x = 10
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is 5")
else:
    print("x is less than 5")

# Loops
for i in range(5):
    print(i)  # Prints 0 to 4

# While loop
count = 0
while count < 3:
    print(count)
    count += 1

```

# List Comprehensions (Pythonic Way of Creating Lists)

```
# Squaring numbers using list comprehension
squared_numbers = [x**2 for x in range(10)]
print(squared_numbers)

# Filtering even numbers
evens = [x for x in range(10) if x % 2 == 0]
print(evens)

```

# Randomness (Generating Random Data)

```
import random

random.seed(42)  # Ensures reproducibility
print(random.random())  # Generate random float between 0 and 1
print(random.randint(1, 10))  # Random integer between 1 and 10
print(random.choice(["apple", "banana", "cherry"]))  # Random selection from list

# Shuffle a list
items = [1, 2, 3, 4, 5]
random.shuffle(items)
print(items)

```

# Regular Expressions (Pattern Matching)

```
import re

text = "Data Science is Awesome!"
pattern = r"Science"

# Searching for a pattern
match = re.search(pattern, text)
if match:
    print("Match found:", match.group())

# Finding all occurrences
matches = re.findall(r"\b\w{5}\b", text)  # Words with exactly 5 letters
print(matches)

```

# File Handling (Reading & Writing Files)

```
# Writing to a file
with open("example.txt", "w") as file:
    file.write("Hello, Data Science!\n")

# Reading from a file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)

```

# defaultdict & Counter (Counting Elements Efficiently)

```
from collections import defaultdict, Counter

# Using defaultdict for counting
word_counts = defaultdict(int)
document = ["data", "science", "data", "python"]
for word in document:
    word_counts[word] += 1

print(word_counts)  # {'data': 2, 'science': 1, 'python': 1}

# Using Counter for counting
word_counts2 = Counter(document)
print(word_counts2.most_common(2))  # Top 2 most common words

```

# Sorting (Sorting Data in Different Ways)

```
# Sorting a list
numbers = [5, 2, 9, 1, 5, 6]
sorted_numbers = sorted(numbers)  # Returns a new sorted list
numbers.sort()  # Sorts in place

# Sorting with a custom key
names = ["Alice", "Bob", "Charlie"]
sorted_names = sorted(names, key=lambda x: x[-1])  # Sort by last letter
print(sorted_names)

```




