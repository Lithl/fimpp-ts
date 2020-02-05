## FiM++ Operators
### Arithmetic
Arithmetic operators take one number (unary operator) or two numbers (binary
operators) as operands.

#### Unary operators
**Identity:** _Not implemented! As FiM++ enforces arithmetic operands to be
numbers, the identity operator serves no purpose._

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

### Bitwise
Bitwise operators take one number (unary operator) or two numbers (binary
operators) as operands.

Bitwise operators convert the 64-bit number operands to 32-bit integers using
two's compliment, except for the zero-fill right shift which uses an unsigned
32-bit integer.

#### Unary operators
**NOT:** Computes the ones' compliment for the operand. (Equivalent to
`-(x + 1)`.)

* TODO

#### Binary operators
**AND:** Computes AND for each corresponding bit in each operand and returns the
result. (The corresponding result bit will be 1 if _both_ operand bits are 1, 0
otherwise.)  

* TODO

**OR:** Computes OR for each corresponding bit in each operand and returns the
result. (The corresponding result bit will be 1 if _either_ operand bits are 1,
0 otherwise.)

* TODO

**XOR:** Computes XOR for each corresponding bit in each operand and returns the
result. (The corresponding result bit will be 1 if the operand bits are
different, 0 otherwise.)

* TODO

**Left shift:** Shifts the bits of the first operand left by a number of
positions equal to the second operand, shifting in `0`s from the right.

* TODO

**Sign-propagating right shift:** Shifts the bits of the first oeprand right by
a number of positions equal to the second operand, shifting in copies of the
leftmost bit from the left.

* TODO

**Zero-fill right shift:** Shifts the bits of the first operand right by a
number of positions equal tot he second operand, shifting in `0`s from the left.

* TODO

### Comparison
Comparison operators produce boolean values from two input operands.

All comparison operators use one of the keywords "is", "was", "has", or "had".
In this section, these keywords will be referred to as a "comparison keyword".
The contraction of these keywords with the word 'not' ("isn't", "wasn't",
"hasn't", and "hadn't") are collectively referred to as "negative comparison
keywords".

#### Equality
Equality operators can function on any two operands, regardless of their
respective types.

**Equality:** _Not implemented! Use of the equality operator is almost always a
mistake, and is often the source of confusion, so has been left out of this
implementation of FiM++._

**Inequality:** _Not implemented! Use of the inequality operator is almost
always a mistake, and is often the source of confusion, so has been left out of
this implementation of FiM++._

**Strict equality:** Returns true if the two operands are exactly equal.

* Use the first operand followed by a comparison keyword and the second
operand.  
`I said Junebug's profit was Rose's profit.`

    ```typescript
    console.log(Junebug_s_profit === Rose_s_profit);
    ```

**Strict inequality:** Returns true if the two operands are not exactly equal.

* Use the first operand followed by either a negative comparison keyword, or
else a comparison keyword followed by the keyword "not", and the second
operand.  
`I said Junebug's profit wasn't Rose's profit.`

    ```typescript
    console.log(Junebug_s_profit !== Rose_s_profit);
    ```

#### Relational
Relational operators will only operate on operands which are number types.

**Greater than:** Returns true if the first operand is greater than the second
operand.  

* Use the first operand followed by a comparison keyword and one of the keyword
phrases "more than" or "greater than" and the second operand.  
`Did you know that truth always is the argument anything Trixie can do is greater than anything you can do?`

    ```typescript
    const truth: boolean = anything_Trixie_can_do > anything_you_can_do;
    ```

**Greater than or equal:** Returns true if the first operand is greater than the
second operand or is equal to the second operand.

* Use the first operand followed by either a negative comparison keyword, or
else a comparison keyword followed by one of the keywords "no" or "not",
followed by the keyword phrase "less than" and the second operand.  
`I said Chrysalis's greatness isn't less than Twilight's greatness.`

    ```typescript
    console.log(Chrysalis_s_greatness >= Twilight_s_greatness);
    ```

**Less than:** Returns true if the first operand is less than the second
operand.

* Use the first operand followed by a comparison keyword and the keyword phrase
"less than" and the second operand.  
`I said the coolness of Rainbow Dash's dress was less than 0.8.`

    ```typescript
    console.log(the_coolness_of_Rainbow_Dash_s_dress < 0.8);
    ```

**Less than or equal to:** Returns true if the first operand is less than the
second perand or is equal to the second operand.

* Use the first operand followed by either a negative comparison keyword, or
else a comparison keyword followed by one of the keywords "no" or "not",
followed by one of the keyword phrases "more than" or "greater than" and the
second operand.  
`I said the number of flowers in Junebug's gardne isn't more than 50.`

    ```typescript
    console.log(the_number_of_flowers_in_Junebug_s_garden <= 50);
    ```
