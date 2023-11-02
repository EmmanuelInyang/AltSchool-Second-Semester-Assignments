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
     echo "Incrementing x by 10, then x= "  
     (( x += 10 ))    
     echo $x
     ```
     **Output:** 20  
     <br>
     <br>
- **Decrement by a constant:** Decrement value of the first operand with a given constant value.
     <br>
     <br>
- **Multiply by constant:**
     <br>
     <br>
- **Divide by a constant:** Multiply the given operand with the constant value.
     <br>
     <br>
- **Remainder by dividing with a constant:**
      <br>
      <br>
- **Exponentiation:** The result is the second operand raised to the power of the first operand.
     ```
     Exponent=$((10**2))  
     echo "Exponent = $Exponent"
     ```
     **Output**
     Exponential = 100
     
     
     
     

   

   
   
