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





