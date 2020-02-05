## FiM++ Operators
### Arithmetic
Arithmetic operators take one number (unary operator) or two numbers (binary
operators) as operands.

#### Unary operators
**Identity:** Returns the value of the operand.

_Not implemented! As FiM++ enforces arithmetic operands to be numbers, the
identity operator serves no purpose._

**Negation:** Returns the negation of the operand (1 becomes -1 and vice versa)

* Use one of the keywords "negated", "negative", or "inverted" followed by the
operand  
`Did you know that Spike's favorite number is negative 3?`

    ```typescript
    Spike_s_favorite_number = -3;
    ```

**Increment:** Increases the operand by 1 then returns the value (prefix) or
returns the value then increases the operand by 1 (postfix). The operand must be
a variable or field.

* Use the variable or field followed by one of the keyword phrases "got one
more" or "increased by one". (Postfix)  
`I said Spike's favorite number increased by one.`

    ```typescript
    console.log(Spike_s_favorite_number++);
    ```
* Use the keyword phrase "one more than" followed by the variable or field.
(Prefix)  
`I said one more than Spike's favorite number.`

    ```typescript
    console.log(++Spike_s_favorite_number);
    ```

**Decrement:** Decreases the operand by 1 then returns the value (prefix) or
returns the value then decreases the operand by 1 (postifx). The operand must be
a variable or field.

* The the variable or field followed by one of the keyword phrases "got one
less" or "decreased by one". (Postfix)  
`I said Spike's favorite number decreased by one.`

    ```typescript
    console.log(Spike_s_favorite_number--);
    ```
* Use the keyword phrase "one less than" followed by the variable or field.
(Prefix)  
`I said one less than Spike's favorite number.`

    ```typescript
    console.log(--Spike_s_favorite_number);
    ```

#### Binary operators
**Addition:** Adds the two operands together and returns the result.

* Use the first operand followed by one of the keywords "plus", "and", or "added
to" followed by the second operand  
`Did you know that twelve always is 2 plus 10?`

    ```typescript
    const twelve = 2 + 10;
    ```
* Use the keyword "add" followed by the first operand, the keyword "and", and
the second operand.  
`I said add 2 and 10.`

    ```typescript
    console.log(2 + 10);
    ```

**Subtraction:** Subtracts the second operand from the first and returns the
result.

* Use the first operand followed by one of the keywords "minus" or "without"
followed by the second operand.  
`Did you know that twelve always is 14 minus 2?`

    ```typescript
    const twelve = 14 - 2;
    ```
* Use the keyword "subtract" followed by the **second** operand, the keyword
"from", and the **first** operand. _(Note the operand order is reversed!)_  
`I said subtract 2 from 14.`

    ```typescript
    console.log(14 - 2);
    ```
* Use the keyword phrase "the difference between" followed by the first operand,
the keyword "and", and the second operand.  
`Did you know that twelve always is the difference between 14 and 2?`

    ```typescript
    const twelve = 14 - 2;
    ```

**Multiplication:** Multiplies the two operands together and returns the result.

* Use the first operand followed by one of the keywords "times" or "multiplied
by" followed by the second operand.  
`Did you know that twelve always is 6 times 2?`

    ```typescript
    const twelve = 6 * 2;
    ```
* Use the keyword "multiply" followed by the first operand, the keyword "and",
and the second operand.  
`I said multiply 6 and 2.`

    ```typescript
    console.log(6 * 2);
    ```

**Division:** Divides the first operand by the second operand and returns the
result.

* Use the first operand followed by the keyword phrase "divided by" and the
second operand.  
`Did you know twelve always is 24 divided by 2?`

    ```typescript
    const twelve = 24 / 2;
    ```
* Use the keyword "divide" followed by the first operand, one of the keywords
"and" or "by", and the second operand.  
`I said divide 24 by 2.`

    ```typescript
    console.log(24 / 2);
    ```

**Modulus division:** Divides the first operand by the second and returns the
remainder of the division operation.

* Prefix a normal division operation with the keyword phrase "the remainder
of"  
`Did you know twelve always is the remainder of 30 divided by 18?`

    ```typescript
    const twelve = 30 % 18;
    ```
    `I said the remainder of divide 30 by 18.`
    
    ```typescript
    console.log(30 % 18);
    ```

**Exponentiation:** Raises the first operand to the power of the second operand
and returns the result.

* Use the first operand followed by the keyword phrase "to the power of" and the
second operand.  
`Did you know sixteen always is 2 to the power of 4?`

    ```typescript
    const sixteen = 2 ** 4;
    ```
