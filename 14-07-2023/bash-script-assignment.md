## File Operators in Bash script
1. **-e operator:**
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

2. **-f operator:**
   The -f file operator in Bash is used to check if a file exists and is a regular file (not a directory or a special file like a device file). Here's an example of how it's used in a Bash script:






Some bash operators include: <br>
**1. Arithmetic Operators** <br>
**2. Logical Operators** <br>
**3. Relational Operators** <br>
**4. File Operators**

**Arithmetic Operators:** <br>
   Bash scripts support 11 arithmetic operators, which include addition, subtraction, multiplication, division, modulo, increment by a constant, decrement by a constant, multiply by a constant, divide by a constant, remainder by dividing with a constant, and exponentiation. <br>
   The 11 arithmetic operators are explained with examples below: <br>
   - **Addition:** It adds two operands. <br>
      ```
      Sum=$((10+4))  
      echo "Sum = $Sum"
      ```
      **Output:**
      Sum = 14
      <br>
      <br>
   - **Subtraction:** It subtracts the second operand from the first one.
      ```
      Difference=$((10-3))  
      echo "Difference = $Difference"
      ```
      **Output:**
      Difference = 7 
      <br>
      <br>
   - **Multiplication:** Multiply two operands.
      ```
      Product=$((10*3))  
      echo "Product = $Product" 
      ```
      **Output**
      Product = 30
      <br>
      <br>
   - **Division:** Return the quotient after diving the first operand from the second operand.
      ```
      Division=$((10/3))
      echo "Division = $Division"
      ```
      **Outout**
      Division = 3
      <br>
      <br>
   - **Modulo:** Return remainder after dividing the first operand from the second operand.
      ```
      Modulo=$((10%3))  
      echo "Modulo = $Modulo"
      ```
      **Output**
      Modulo = 1
     <br>
     <br>
- **Increment by a constant:** Increment value of the first operand with given constant value.
     ```
     echo "Incrementing x by 10, then x=10"  
     (( x += 10 ))    
     echo $x
     ```
     **Output:** 20  
     <br>
     <br>
- **Decrement by a constant:** Decrement value of the first operand with a given constant value.
     ```
     echo "Decrementing x by 15, then x=10"  
     (( x -= 15 ))  
     echo $x  
     ```
     **Output:** 5
     <br>
     <br>
- **Multiply by constant:** Multiply the given operand with the constant value.
     ```
     echo "Multiply of x by 2, then x= 10"  
     (( x *= 2 ))
     ```
     **Output:** 200
     <br>
     <br>
- **Divide by a constant:** Divide the operand with the given constant value and return the quotient.
     ```
     echo "Dividing x by 5, x=10"  
     (( x /= 5 ))  
     echo $x 
     ```
     **Output:** 2
     <br>
     <br>
- **Remainder by dividing with a constant:** Divide the operand with the given constant value and return the remainder
     ```
     echo "Remainder of Dividing x by 5, x=10"  
     (( x %= 5 ))  
     echo $x  
     ```
     **Output:** 2
  
      <br>
      <br>
- **Exponentiation:** The result is the second operand raised to the power of the first operand.
     ```
     Exponent=$((10**2))  
     echo "Exponent = $Exponent"
     ```
     **Output**
     Exponential = 100

**Relational Operators:**
   Relational operators are those operators which define the relation between two operands. They give either true or false depending upon the relation. They are of 6 types:

   1. **‘==’ Operator:** Double equal to operator compares the two operands. It returns true if they are equal otherwise returns false.
      ```
      if(( $a==$b )) 
      then 
         echo a is equal to b. 
      else  
         echo a is not equal to b. 
      fi
      ```
   2. **‘!=’ Operator:** Not Equal to operator return true if the two operands are not equal otherwise it returns false.
       if(( $a!=$b )) 
       then 
          echo a is not equal to b. 
       else
          echo a is equal to b. 
   fi 
   3. **‘<‘ Operator:** Less than operator returns true if the first operand is less than the second operand otherwise returns false.
      if(( $a<$b )) 
      then 
         echo a is less than b. 
      else
         echo a is not less than b. 
      fi 
   4. **‘<=’ Operator:** Less than or equal to the operator returns true if the first operand is less than or equal to the second operand otherwise returns false.
      if(( $a<=$b )) 
      then 
         echo a is less than or equal to b. 
      else
         echo a is not less than or equal to b. 
   fi 
   5 **‘>’ Operator:** Greater than operator returns true if the first operand is greater than the second operand otherwise returns false.
      if(( $a>$b )) 
      then 
         echo a is greater than b. 
      else
         echo a is not greater than b. 
   fi 
   6. **‘>=’ Operator:** Greater than or equal to operator returns true if the first operand is greater than or equal to the second operand otherwise returns false.
        if(( $a>=$b )) 
        then 
            echo a is greater than or equal to b. 
        else
            echo a is not greater than or equal to b. 
        fi 
   
**Logical Operators:** <br>
   They are commonly referred to as boolean operators and serve for executing logical operations. <br> 
   They are classified into three types:
   
   1. **Logical AND (&&):** This is a binary operator, which returns true if both the operands are true otherwise returns false. <br>
      ```
      if(($a == "true" & $b == "true" )) 
      then 
      echo Both are true. 
      else
      echo Both are not true. 
      fi
      ```
      **Output:** Both are true.
   2. **Logical OR (||):** This is a binary operator, which returns true if either of the operands is true or both the operands are true and returns false if all of them is false.
      ```
      if(($a == "true" || $b == "true" )) 
      then 
      echo At least one of them is true. 
      else
      echo None of them is true.
      fi 
      ```
      **Output:** At least one of them is true.
   3. **Not Equal to (!):** This is a unary operator which returns true if the operand is false and returns false if the operand is true.
      ```
      if(( ! $a == "true"  )) 
      then 
      echo "a" was initially false. 
      else
      echo "a" was initially true. 
      fi 
      ```
      **Output:** a was initially true.

**File Test Operator:** These operators are used to test a particular property of a file.

   - **-b operator:** This operator checks whether a file is a block special file or not. It returns true if the file is a block special file otherwise false. <br>
      ```
      if [ -b "$block_device" ]; then
         echo "The file $block_device is a block special file."
      else
         echo "The file $block_device is not a block special file."
      fi
      ```
   - **-c operator:** This operator checks whether a file is a character special file or not. It returns true if it is a character special file otherwise false. <br>
      ```
      if [ -c "$device_file" ]; then
         echo "The file $device_file is a character special file."
      else
         echo "The file $device_file is not a character special file."
      fi
      ```
   - **-d operator:** This operator checks if the given directory exists or not. If it exists then the operator returns true otherwise false. <br>
      ```
      if [ -d "$directory" ]; then
         echo "The directory $directory exists."
      else
         echo "The directory $directory does not exist."
      fi
     ```  
   - **-e operator:** This operator checks whether the given file exists or not. If it exits this operator returns true otherwise false. <br>
     ```
      if [ -e $FileName ] 
       then 
          echo File Exist 
       else
          echo File does not exist    
       fi 
     ```
   - **-r operator:** This operator checks whether the given file has read access or not. If it has read access then it returns true otherwise false. <br>
      ```
      if [ -r $FileName ] 
      then 
         echo The given file has read access. 
      else
         echo The given file does not have read access. 
      fi 
      ```
   - **-w operator:** This operator checks whether the given file has write access or not. If it has been written then it returns true otherwise false. <br>
      ```
      if [ -w $FileName ] 
      then 
         echo The given file has write access. 
      else
         echo The given file does not have write access. 
      fi 
      ```
   - **-x operator:** This operator checks whether the given file has executed access or not. If it has execute access then it returns true otherwise false. <br>
      ```
      if [ -x $FileName ] 
      then 
         echo The given file has to execute access. 
      else
         echo The given file does not have execute access. 
      fi 
      ```
   - **-s operator:** This operator checks the size of the given file. If the size of the given file is greater than 0 then it returns true otherwise it is false.
      ```
      if [ -s $FileName ] 
      then 
         echo The given file is not empty. 
      else
         echo The given file is empty. 
      fi 
      ```

  

  

  

  

   
   
