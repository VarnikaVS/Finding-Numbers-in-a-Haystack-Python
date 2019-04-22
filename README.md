# Finding-Numbers-in-a-Haystack-Python
Parse a file with text and numbers and then extracting all the numbers in the file and computing the sum of the numbers.

Also make sure to save the file into the same folder as you will be writing your Python program.


import re

text = open ('regex_sum_193782.txt')
numberslist = list()
for sentences in text:
    txt = sentences.rstrip()
    results = re.findall('[0-9]+', txt)
    for answer in results:
        y = int(answer)
        numberslist.append(y)

print ( 'There are ' +  str(len(numberslist)) + ' numbers in this file that have a total sum of ' + str(sum(numberslist)))
