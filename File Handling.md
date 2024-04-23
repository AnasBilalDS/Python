```python
#Files - Text, CSV, Excel
    #Very less data storage in  File systems 
    #Data Bases are for high data volume
```


```python
#Types of files 

    #Text files - Jupyter notebook, log files, program file, normal text files - Human can read it 
    #Binary files - Image or videos 
    
#To perform any action on the files 
    #Open a file, need to mention the purpose of the opening of the file as well
    
#open(filename,mode)

#The allowable modes in python 

    #1. Read (r) - Opens up the file for read operation and its a default mode 
    #2. Write (w) - opens up the file for write something in the file, if data is present in the then it overwrite 
        #If the file is not present it will create one
    #3. Append (a) - It will append the data in the file. If the file is not present it will create one
    #4. Read and write (r+) - Read will take the priority and it will not overwrite the data 
    #5. Write and read (w+) - Write will take the priority and it will overwrite the data 
    #6. Append and read (a+) - Append will take the priority and it will not overwrite 
    #7. Exclusive creation mode for writing operation (x) - Fileexists error, the file should not be there
```


```python
#For binary file
    #1. rb
    #2. wb
    #3. ab
    #4. r+b
    #5. w+b
    #6. a+b
    #7. xb
```


```python
# for import inbuild module os#
import os
```


```python
# for getting current working directory #
os.getcwd()
```




    'C:\\Users\\dell'




```python
os.chdir('C:\\Users\\dell\\Desktop')
```


```python
f = open('Caravan011.txt','w')
print('File Name: ', f.name)
print('File Mode: ', f.mode)
print('File Readable: ', f.readable())
print('File Writeable: ', f.writable())
print('File Closed: ', f.closed)
f.close()
print('File Closed: ', f.closed)
```

    File Name:  Caravan011.txt
    File Mode:  w
    File Readable:  False
    File Writeable:  True
    File Closed:  False
    File Closed:  True
    


```python
f=open('Caravan011.txt','w')
f.write('Python is an easy language to learn\n')
f.write('Earlier I was very much scared of python\n')
f.close()
```


```python
f= open ('Caravan011.txt','w')
f.write ('Python is an easy language to learn\n')
f.write('Python iseasy tricky to understand\n')
f.close()
```


```python
f= open ('Caravan011.txt','a')
f.write ('Python is an easy language to learn\n')
f.write('Python iseasy tricky to understand\n')
f.close()
```


```python
# f.witelines(), this is for writing lines from a list #
list1=['Hi my name is Anas Bilal\n','I did my MBA from Chennai\n','I am a foodie\n']
f=open ('Caravan011.txt','w')
f.writelines(list1)
f.close()
```


```python
f= open ('Caravan011.txt','a')
f.write ('Python is an easy language to learn\n')
f.write('Python iseasy tricky to understand\n')
f.close()
```


```python
# How can I read the data #
f=open ('Caravan011.txt','r')
data = f.read()
print(data)
f.close()
```

    Hi my name is Anas Bilal
    I did my MBA from Chennai
    I am a foodie
    Python is an easy language to learn
    Python iseasy tricky to understand
    
    


```python
# Write a python code to to count length of words, character and lines
fname = input('Enter the file name: ')
f = open(fname,'r')
lcount = wcount = ccount = 0

for line in f:
    lcount = lcount+1
    ccount = ccount + len(line)
    words = line.split()
    wcount = wcount + len(words)
print('The number of lines: ', lcount)
print('The number of characters: ', ccount)
print('The number of words: ', wcount)
f.close()
```

    Enter the file name:  Caravan011.txt
    

    The number of lines:  5
    The number of characters:  136
    The number of words:  28
    


```python

```


```python

```
