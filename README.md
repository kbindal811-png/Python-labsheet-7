# Python-labsheet-7
Python labsheet 7

Python Programming Lab – File Handling – Read 
and Write Operations using Python Programming

1. Write a Python program to create and write text into a file.

with open("sample1.txt", "w") as f:
    f.write("Hello, this is a sample text file.\n")
    f.write("This file is created using Python.\n")
    f.write("File handling is easy and fun!")

print("Data written successfully into 'sample1.txt'")

output -
Hello, this is a sample text file.
This file is created using Python.
File handling is easy and fun!


2. Write a program to read the entire content of a text file.

with open("sample1.txt", "r") as f:
    content = f.read()

print("File Content:\n")
print(content)

output -
File Content:

Hello, this is a sample text file.
This file is created using Python.
File handling is easy and fun!


3. Write a program to read a file line by line.

with open("sample1.txt", "r") as f:
    for line in f:
        print(line.strip())
output -
Hello, this is a sample text file.
This file is created using Python.
File handling is easy and fun!


4. Write a program to count the number of words in a text file.

with open("sample1.txt", "r") as f:
    content = f.read()
    words = content.split()
    print("Number of words:", len(words))
output -
Number of words: 14


5. Write a program to count the number of lines and characters in a file.

with open("sample1.txt", "r") as f:
    lines = f.readlines()
    num_lines = len(lines)
    num_chars = sum(len(line) for line in lines)

print("Number of lines:", num_lines)
print("Number of characters:", num_chars)
output -
Number of lines: 3
Number of characters: 92



6. Write a program to display only even-numbered lines from a file.

with open("sample1.txt", "r") as f:
    lines = f.readlines()
    print("Even-numbered lines:\n")
    for i in range(1, len(lines), 2):
        print(lines[i].strip())
output -
Even-numbered lines:

This file is created using Python.



7. Write a program to write multiple lines of input from the user into a file.

with open("user_input.txt", "w") as f:
    print("Enter multiple lines (type 'end' to finish):")
    while True:
        line = input()
        if line.lower() == "end":
            break
        f.write(line + "\n")

print("Data successfully written into 'user_input.txt'")
output -
Enter multiple lines (type 'end' to finish):
Python is fun
We are learning file handling
end
Data successfully written into 'user_input.txt'



8. Write a program to append new content to an existing file.

with open("sample1.txt", "a") as f:
    f.write("\nAppended line: Python makes file handling simple.")

print("New content appended successfully.")
output -
New content appended successfully.



9. Write a program to copy the contents of one file into another.

with open("sample1.txt", "r") as f1, open("copy.txt", "w") as f2:
    for line in f1:
        f2.write(line)

print("Contents copied successfully to 'copy.txt'")
output -
Contents copied successfully to 'copy.txt'



10. Write a program to read a file and convert its content to uppercase.

with open("sample1.txt", "r") as f:
    content = f.read()

print("Uppercase Content:\n")
print(content.upper())
output -
Uppercase Content:

HELLO, THIS IS A SAMPLE TEXT FILE.
THIS FILE IS CREATED USING PYTHON.
FILE HANDLING IS EASY AND FUN!
APPENDED LINE: PYTHON MAKES FILE HANDLING SIMPLE.



11. Write a program to search for a particular word in a file.

word = input("Enter word to search: ")

with open("sample1.txt", "r") as f:
    content = f.read()

if word in content:
    print(f"The word '{word}' is found in the file.")
else:
    print(f"The word '{word}' is NOT found in the file.")
output -
Enter word to search: Python
The word 'Python' is found in the file.



12. Write a program to count the occurrence of a specific word in a file.

word = input("Enter word to count: ").lower()

with open("sample1.txt", "r") as f:
    content = f.read().lower()
    count = content.split().count(word)

print(f"The word '{word}' occurs {count} times in the file.")
output -
Enter word to count: python
The word 'python' occurs 2 times in the file.



13. Write a program to read numbers from a file and display their sum and average.

# Create a file with numbers
with open("numbers.txt", "w") as f:
    f.write("10 20 30 40 50")

# Read and calculate
with open("numbers.txt", "r") as f:
    numbers = list(map(int, f.read().split()))
    total = sum(numbers)
    avg = total / len(numbers)

print("Numbers:", numbers)
print("Sum =", total)
print("Average =", avg)
output -
Numbers: [10, 20, 30, 40, 50]
Sum = 150
Average = 30.0



14. Write a program to display the longest line in a file.

with open("sample1.txt", "r") as f:
    lines = f.readlines()
    longest_line = max(lines, key=len)

print("Longest line:\n", longest_line.strip())
output -
Longest line:
Appended line: Python makes file handling simple.



15. Write a program to replace a word in a file with another word.

old_word = "Python"
new_word = "Java"

with open("sample1.txt", "r") as f:
    content = f.read()

content = content.replace(old_word, new_word)

with open("sample1.txt", "w") as f:
    f.write(content)

print(f"'{old_word}' has been replaced with '{new_word}'.")
output -
'Python' has been replaced with 'Java'.



16. Write a program to display the first and last lines of a file.

with open("sample1.txt", "r") as f:
    lines = f.readlines()
    print("First line:", lines[0].strip())
    print("Last line:", lines[-1].strip())
output -
First line: Hello, this is a sample text file.
Last line: Appended line: Python makes file handling simple.



17. Write a program to remove blank lines from a file.

with open("sample1.txt", "r") as f:
    lines = f.readlines()

with open("sample1.txt", "w") as f:
    for line in lines:
        if line.strip():
            f.write(line)

print("Blank lines removed successfully.")
output -
Blank lines removed successfully.



18. Write a program to read a file and store only unique words into another file.

with open("sample1.txt", "r") as f:
    words = f.read().split()

unique_words = sorted(set(words))

with open("unique_words.txt", "w") as f:
    f.write(" ".join(unique_words))

print("Unique words saved to 'unique_words.txt'.")
output -
Unique words saved to 'unique_words.txt'.



19. Write a program to sort all words in a file alphabetically and save to a new file.

with open("sample1.txt", "r") as f:
    words = f.read().split()

words.sort()

with open("sorted_words.txt", "w") as f:
    f.write(" ".join(words))

print("Words sorted alphabetically and saved to 'sorted_words.txt'.")
output -
Words sorted alphabetically and saved to 'sorted_words.txt'.



20. Write a program to merge two text files into a third file.

with open("sample1.txt", "r") as f1, open("user_input.txt", "r") as f2, open("merged.txt", "w") as f3:
    f3.write(f1.read() + "\n" + f2.read())

print("Files merged successfully into 'merged.txt'.")
output -
Files merged successfully into 'merged.txt'.



21. Write a Python program to create and write data into a CSV file.
import csv

data = [
    ["Name", "RollNo", "Marks"],
    ["Amit", 1, 85],
    ["Neha", 2, 90],
    ["Ravi", 3, 78]
]

with open("students.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerows(data)

print("Data written successfully into 'students.csv'")
output -
Data written successfully into 'students.csv'




22. Write a program to read data from a CSV file and display it.

import csv

with open("students.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
output -
['Name', 'RollNo', 'Marks']
['Amit', '1', '85']
['Neha', '2', '90']
['Ravi', '3', '78']



23. Write a program to read a CSV file and calculate the average of numeric columns.

import csv

with open("students.csv", "r") as f:
    reader = csv.reader(f)
    next(reader)
    marks = [int(row[2]) for row in reader]

avg_marks = sum(marks) / len(marks)
print("Average Marks =", avg_marks)
output -
Average Marks = 84.33333333333333



24. Write a program to count the number of rows and columns in a CSV file.

import csv

with open("students.csv", "r") as f:
    reader = list(csv.reader(f))
    rows = len(reader)
    cols = len(reader[0])

print("Number of rows:", rows)
print("Number of columns:", cols)
output -
Number of rows: 4
Number of columns: 3



25. Write a program to append a new record to an existing CSV file.

import csv

with open("students.csv", "a", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["Priya", 4, 88])

print("New record appended successfully.")
output -
New record appended successfully.



26. Write a program to copy data from one CSV file to another.

import csv

with open("students.csv", "r") as f1, open("copy_students.csv", "w", newline="") as f2:
    writer = csv.writer(f2)
    for row in csv.reader(f1):
        writer.writerow(row)

print("Data copied successfully to 'copy_students.csv'.")
output -
Data copied successfully to 'copy_students.csv'.



27. Write a program to display specific columns (like Name and Marks) from a CSV file.

import csv

with open("students.csv", "r") as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(f"Name: {row['Name']}, Marks: {row['Marks']}")
output -
Name: Amit, Marks: 85
Name: Neha, Marks: 90
Name: Ravi, Marks: 78
Name: Priya, Marks: 88



28. Write a program to find and display the highest marks from a CSV file.

import csv

with open("students.csv", "r") as f:
    reader = csv.DictReader(f)
    highest = max(reader, key=lambda x: int(x["Marks"]))

print(f"Topper: {highest['Name']} with {highest['Marks']} marks")
output -
Topper: Neha with 90 marks



29. Write a program to search a record in a CSV file based on student name.

import csv

name = input("Enter name to search: ")

found = False
with open("students.csv", "r") as f:
    reader = csv.DictReader(f)
    for row in reader:
        if row["Name"].lower() == name.lower():
            print("Record found:", row)
            found = True
            break

if not found:
    print("Record not found.")
output -
Enter name to search: Ravi
Record found: {'Name': 'Ravi', 'RollNo': '3', 'Marks': '78'}



30. Write a program to combine multiple CSV files into one single file.

import csv
import glob

csv_files = glob.glob("*.csv")

with open("combined.csv", "w", newline="") as out:
    writer = None
    for file in csv_files:
        with open(file, "r") as f:
            reader = csv.reader(f)
            if writer is None:
                writer = csv.writer(out)
                writer.writerows(reader)
            else:
                next(reader, None)  # Skip header
                writer.writerows(reader)

print("All CSV files merged into 'combined.csv'.")
output -
All CSV files merged into 'combined.csv'.



















