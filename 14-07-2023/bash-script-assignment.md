**Bash operators** are symbols used in scripting to perform operations on values and variables, often combined with commands for various tasks, comparisons, and conditions.

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
   <br>
   <br>
**Logical Operators:** <br>
   They are commonly referred to as boolean operators and serve for executing logical operations. <br> 
   They are classified into three types:
   
   1. **Logical AND (&&):** This is a binary operator, which returns true if both the operands are true otherwise returns false. <br>
   2. **Logical OR (||):** This is a binary operator, which returns true if either of the operands is true or both the operands are true and returns false if none of them is false.       <br>
   3. **Not Equal to (!):** This is a unary operator which returns true if the operand is false and returns false if the operand is true.
     

   

   
   
