# Text Files and Binary Files

There are two types of files that can be handled in Python, normal text files and binary files.

Text Files : Each line of text file ends in a special character called EOL(End of Line), which is the new line character '\n' in Python by default.
Binary Files : In this type of file there is no terminator between lines, and the data is stored after being converted into a binary language(written in 0s and 1s).

# How to open, read, write, close the data

## open()

Opening the file can be done with the code below, no extra module required.

    File_object = open(r"filename.ext","Access_Mode")
        
> The r prefix in front of "File_Name" means that there will be no special character in the file name behind. For example, putting r prefix in front of a file name **"D:\temp\text.txt"** will prevent the part **\t** treated as the tab character. It could be ignored if the target file is located in the same directory as the Python file and the address is not being placed.
<br/><br/>

## read()

~~~Python
f = open('filename.ext','r')

data = f.read()

f.close()
~~~

Reading from a file uses access mode 'r', which is the default mode in opening files. The handle is positioned at the beginning of the file and raises an error if the file does not exist. The data read is temporary, so it must be stored in an extra variable for use.

~~~Python
f = open('filename.ext','r')

data = f.readline()

f.close()
~~~

Also the file can read by the code above, but only the first line with it. ```f.readlines()``` can read all lines and return them merged in a list.
<br/><br/>

## write()

~~~Python
f = open('filename.ext','w')

f.write(content in string)

f.close()
~~~

Access mode 'w' is used in writing to a file.

~~~Python
f = open('filename.ext','w')

f.writelines(lst) for lst = [string1,srting2,string3]

f.close()
~~~

Using ```f.writelines()``` will add each element in the list to the text file at a single time.
<br/><br/>

## close()

The file should be closed to save it. If the file is not closed, the added data may not be shown, or a buffering issue can come up.
