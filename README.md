# Automated File Filter
There are many files in our system which are of various types, for e.g., jpg, png, csv, xls, etc. In some cases, there is a requirement to filter and place the files in specific folders which are related to the type of files. Hence, I created a program that copy or move the files in the folders having their extension in the folder name specified.




# Libraries used
1. os : It is used for performing operating system dependent functionalities like opening the file, making directory, showing the files and folders in a specific path entered, checking if the path of file exists or not, etc.
   
2. shutil : This module offers high-level operations on files and collections of files. Particularly, they provide the functions for supporting the operations like copy, move, delete on a file. In windows, there's a limitation, while using any of these shutil operations, the meta-data like file owners, ACLs and alternate data streams are not copied. shutil also provides the support to copy a file like an object, example, shutil.copyfileobj(file_src, file_dest [, length])

Reference : https://docs.python.org/3/library/shutil.html
Reference : https://docs.python.org/3/library/os.html



# User-defined functions
1. folder_exists_for_file : It takes the extension of file as input and checks whether that extension name exists in the folder names entered by user. If so, then it return True, else False. This function is created in order to automatically go for the files with existing folders having their extension and start the next operation of copying it or moving it accordingly.
   
2. folder_name_for_file_extension : It returns the folder name having matched the file extension exists in its name.



# Input
1. Enter the path of the folder in which the files are present (e.g., C:\Documents\Files)

2. Enter the number of folders you want to create

3. Start entering the folder name for the folders

4. Enter the operation you want to perform (currently 'copy' or 'move')




# Output
- If the files already exists in the folders you named, then repeat operations are avoided and not performed.

- If the folders didn't exist, they are created. Then, the copying and moving of the files are performed according to the operation entered.


