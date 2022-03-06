# Text Files and Binary Files

There are two types of files that can be handled in Python, normal text files and binary files.

- Text Files : Each lines of text file ends in a special character called EOL(End of Line), which is the new line character '\n' in Python by default.
- Binary Files : In this type of file there is no terminator between lines, and the data is stored after converted into binary language(written in 0s and 1s).

# How to open, read, write, close the data

## open()

Opening the file can be done with the code below, no extra module required.

        File_object = open(**r**"File_Name","Access_Mode")
        
> The r perfix in front of "File_Name" means that tere will be no special character in the file name behind. For example, putting r perfix in front of a file name **"D:\temp\text.txt"** will prevent the part **\t** treated as the tab character.

## read()

        f = open("filename.txt","r")
        
        data = f.read()
        
        f.close()
        
Reading from a file uses access mode 'r', which is default mode in opening files. The handle is positioned in at the begenning of the file, and raises error if the file does not exist. The data read is temporary, so it must be stored in extra variable for use.
