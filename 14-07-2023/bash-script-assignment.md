## File Operators in Bash script
1. **-e operator:** <br>
   The -e file operator is used to check if a file exists. It returns true if the file exists and false if it doesn't.
   Here's an example of how it's used in a Bash script:
     ```
      #!/bin/bash

      file_path="/altschool/exam/semester-two.txt"
  
      if [ -e "$file_path" ]; then
         echo "The file exists."
      else
         echo "The file does not exist."
      fi
     ```
     In this script, the -e operator is used to check if the file located at the specified path exists. If it does, it prints "The file exists," and if it doesn't, it prints "The file does not exist."

2. **-f operator:** <br>
   The -f file operator is used to check if a file exists and is a regular file (not a directory or a special file like a device file).
   Here's an example of how it's used in a Bash script:
      ```
      #!/bin/bash

      file_path="/altschool/exam/semester-two.txt"

      if [ -f "$file_path" ]; then
          echo "The file exists and is a regular file."
      else
          echo "The file does not exist or is not a regular file."
      fi
      ```
      In this script, the -f operator checks if the file at the specified path exists and is a regular file. If it is, it prints "The file exists and is a regular file." If the file does not exist or is not a regular file, it prints "The file does not exist or is not a regular file.

3. **-d operator** <br>
   The -d file operator is used to check if a directory exists.
   Here's an example of how it's used in a Bash script:
      ```
      #!/bin/bash

      directory_path="/altschool/exam"

      if [ -d "$directory_path" ]; then
          echo "The directory exists."
      else
          echo "The directory does not exist."
      fi
      ```
      In this script, the -d operator checks if the directory at the specified path exists. If it does, it prints "The directory exists." If the directory does not exist, it prints "The directory does not exist."

4. **-s operator** <br>
   The -s file operator is used to check if a file exists and has a size greater than zero (i.e., it's not empty).
   Here's an example of how it's used in a Bash script:
      ```
      #!/bin/bash

      file_path="/altschool/exam/semester-two.txt"

      if [ -s "$file_path" ]; then
          echo "The file exists and is not empty."
      else
          echo "The file does not exist or is empty."
      fi
      ```
   In this script, the -s operator checks if the file at the specified path exists and has a size greater than zero. If the file exists and is not empty, it prints "The file exists and is not empty." If the file does not exist or is empty, it prints "The file does not exist or is empty."

5. **-r operator** <br>
   The -r file operator is used to check if a file is readable.
   Here's an example of how it's used in a Bash script:
      ```
      #!/bin/bash

      file_path="/altschool/exam/semester-two.txt"
      
      if [ -r "$file_path" ]; then
          echo "The file is readable."
      else
          echo "The file is not readable."
      fi
      ```
      In this script, the -r operator checks if the file at the specified path is readable. If the file is readable, it prints "The file is readable." If the file is not readable, it prints "The file is not readable."

6. **-w operator** <br>
   The -w file operator is used to check if a file is writable.
   Here's an example of how it's used in a Bash script:
      ```
      #!/bin/bash

      file_path="/altschool/exam/semester-two.txt"

      if [ -w "$file_path" ]; then
          echo "The file is writable."
      else
          echo "The file is not writable."
      fi
      ```
      In this script, the -w operator checks if the file at the specified path is writable. If the file is writable, it prints "The file is writable." If the file is not writable, it prints "The file is not writable."

7. **-x operator** <br>
   The -x file operator is used to check if a file is executable.
   Here's an example of how it's used in a Bash script:
      ```
      #!/bin/bash

      file_path="/path/to/your/script.sh"

      if [ -x "$file_path" ]; then
         echo "The file is executable."
      else
         echo "The file is not executable."
      fi
      ```
   In this script, the -x operator checks if the file at the specified path is executable. If the file is executable, it prints "The file is executable." If the file is not executable, it prints "The file is not executable."

8. **-L operator** <br>
    In Bash, the -L file operator checks if a file is a symbolic link.
    Here's an example:
      ```
      #!/bin/bash

      # Define a file path (a symbolic link to a file)
      file_path="/path/to/symbolic_link"

      # Check if the file is a symbolic link
      if [ -L "$file_path" ]; then
         echo "The file is a symbolic link."
      else
         echo "The file is not a symbolic link."
      fi
      ```
   The script will determine whether the specified file is a symbolic link and print the corresponding message.

9. **-c operator** <br>
    the -c file operator is used to check whether a file is a special character file. Special character files are typically associated with devices in Unix-like systems. These files provide access to various devices such as terminals, serial ports, or sound cards. The -c operator checks if a file is a special character file, and it returns true if the file is of this type. If the file is not a special character file or if it doesn't exist, the operator returns false.
    Here's how you can use the -c file operator in a Bash script:
      ```
      #!/bin/bash

      # Define the file path to check
      file_path="/dev/tty"

      # Check if the file is a special character file
      if [ -c "$file_path" ]; then
          echo "The file is a special character file."
      else
          echo "The file is not a special character file or doesn't exist."
      fi
      ```
      
10. **-p operator** <br>
    The -p file operator is used to check whether a file is a named pipe (also known as a FIFO or First-In-First-Out). Named pipes are a type of special file used for inter-process communication (IPC) on Unix-like systems. They allow data to be passed between processes. The -p operator checks if a file is a named pipe and returns true if the file is indeed a named pipe. If the file is not a named pipe or if it doesn't exist, the operator returns false.
Here's how you can use the -p file operator in a Bash script:
      ```
      #!/bin/bash

      # Define the file path to check
      file_path="/tmp/my_named_pipe"

      # Check if the file is a named pipe
      if [ -p "$file_path" ]; then
         echo "The file is a named pipe (FIFO)."
      else
         echo "The file is not a named pipe or doesn't exist."   
      fi
      ```

11. **-u operator** <br>
    In Bash scripting, the -u file operator is used to check if a file has the setuid (SUID) permission bit set. The setuid permission bit is a special permission that can be assigned to executable files. When a file has the SUID bit set, it means that when the file is executed, it runs with the permissions of the file's owner, not the permissions of the user who runs it. The -u operator checks whether the SUID bit is set on a file. If the SUID bit is set, the operator returns true. If the SUID bit is not set or the file does not exist, it returns false.
Here's how you can use the -u file operator in a Bash script:
      ```
      #!/bin/bash

      # Define the file path to check
      file_path="/path/to/my_executable_file"

      # Check if the file has the SUID bit set
      if [ -u "$file_path" ]; then
          echo "The file has the SUID (setuid) permission bit set."
      else
          echo "The file does not have the SUID (setuid) permission bit set or doesn't exist."
      fi
      ```
      
12. **-ef operator** <br>
  -ef (Equivalent Files): This operator checks if two files are equivalent, meaning they have the same device and inode numbers. It’s often used to check if two files are hard links to the same data.
Example:
      ```
      if [ "file1.txt" -ef "file2.txt" ]; then
         echo "file1.txt and file2.txt are hard links to the same data."
      fi
      ```
 
13. **-G operator** <br>
    The -G file operator in Bash script is used to check whether a file exists and whether it has the set-group-ID (SGID) permission set. The SGID permission on a file means that when the file is executed, it runs with the privileges of the group that owns the file rather than with the privileges of the user who executes it. This operator is useful for determining whether a file is set to execute with group permissions.
Here's the basic syntax for using the -G file operator:
      ```
      [ -G file ]
       ```
      `[` and `]` are used to enclose the file test expression.
      `-G` is the file operator itself.
      `file` should be replaced with the path to the file you want to test.
For example, you can use the -G operator to check if a file named "example.sh" has the SGID permission set:
      ```
      if [ -G "example.sh" ]; then
         echo "The file 'example.sh' has the SGID permission set."
      else
         echo "The file 'example.sh' does not have the SGID permission set."
      fi
      ```

14. **-nt operator** <br>
    The -nt file operator in Bash script is used to compare the modification timestamp of two files and determine if one file is newer than another. Specifically, it checks if the file on the left side of the operator is newer (modified more recently) than the file on the right side of the operator. This operator is useful for conditional statements in scripts where you need to perform actions based on file modification times.
Here's the basic syntax for using the -nt file operator:
      ```
      [ file1 -nt file2 ]
      ```
      `[` and `]` are used to enclose the file test expression.
      `file1` and `file2` are the two files you want to compare. You should replace them with the actual file paths.
For example, you can use the -nt operator to compare two files, "file1.txt" and "file2.txt," to check if "file1.txt" is newer:
      ```
      if [ "file1.txt" -nt "file2.txt" ]; then
         echo "file1.txt is newer than file2.txt."
      else
         echo "file2.txt is newer than file1.txt or they have the same modification time."
      fi
      ```

15. **-ot operator** <br>
   The -ot file operator in Bash script is used to compare the modification timestamps of two files and determine if one file is older than another. Specifically, it checks if the file on the left side of the operator is older (modified earlier) than the file on the right side of the operator. This operator is useful for conditional statements in scripts where you need to perform actions based on file modification times.
Here's the basic syntax for using the -ot file operator:
      ```
      [ file1 -ot file2 ]
      ```
      `[` and `]` are used to enclose the file test expression.
      `file1` and `file2` are the two files you want to compare. You should replace them with the actual file paths.
For example, you can use the -ot operator to compare two files, "file1.txt" and "file2.txt," to check if "file1.txt" is older:
      ```   
      if [ "file1.txt" -ot "file2.txt" ]; then
         echo "file1.txt is older than file2.txt."
      else
         echo "file2.txt is older than file1.txt or they have the same modification time."
      fi
      ```

   
