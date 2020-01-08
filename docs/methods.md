## FiM++ Methods
A method is a procedure associated with an object. Methods may be either
instance (tied to a particular instance of the class) or static (shared by all
instances of the class), and they may be public (accessible by any consumer that
can access the class), protected (only accessible by the class and its
descendants), or private (only accessible by the class itself).

### Method declaration
A method is declared with a particular keyword phrase which determines its
properties, followed by the name of the method. You may follow the name with the
keyword phrase "with" or "to get" and a type in order to specify the method's
return type. You may follow the return type (if present) or name (if no return
type is specified) with the string "using" and one or more instances of a type
and a parameter name (separated by "and" if there are multiple parameters). If
multiple parameters in a row share a type, only the first parameter in the
sequence of parameters sharing a type ned to have the type specified (eg,
`number A and number B` can be written as `numbers A and B`).

To define the method as being public, use the keyword phrase `I learned`.

To define the method as being protected, use the keyword phrase `We learned`.

To define the method as being private, use the keyword phrase
`I secretly learned`.

Methods are by default instance methods. To make a method static, prefix the
declaration with `Finally,`.

Up to one method within a class may be marked as a program entry point. Use
`Today I learned` for such a method, which will make it public and static. The
only valid return type for a program entry point method is `nothing` (or you can
leave the return type unspecified). The program entry point will be passed an
array of strings as its only parameter, so if you wish to make use of it, you
should specify the type as `many words` (or any of the string keyword aliases,
see [Variables and Literals](variables-literals.md#fim-variables) for
specifics).

**Example:** `I learned the importance of oral hygeine!`

Declares a public instance method named "the importance of oral hygeine" with no
parameters or specified return type.

**Example:** `Today I learned how to say Hello World.`

Declares a program entry point function named "how to say Hello World". (While
an array of strings will be passed to the method when called, this function has
no intention of making use of the parameter and so omits it from the
declaration.)

**Example:** `We learned how to do math with a number.`

Declares a protected instance method named "how to do math" which will return a
number.

**Example:**
```
Finally, I secretly learned how to take the sum of a set of numbers
  with a number
  using the numbers A and B.
```

Declares a static private mthod named "how to take the sum of a set of numbers"
which will return a number and has two number parameters, "A" and "B".

#### Typescript equivalent
```typescript
the_importance_of_oral_hygeine() {
```
```typescript
static how_to_say_Hello_World() {
```
(Elsewhere in this typescript output would be code to let this method be run as
a standalone program.)
```typescript
protected how_to_do_math(): number {
```
```typescript
private static
    how_to_take_the_sum_of_a_set_of_numbers(A: number, B: number): number {
```

### Returning a value
Any method with a return type other than `nothing` must explicitly return a
value. Thanks to Typescript's type inferencing, you can also return a value
without specifying the type, so long as all code paths return a value of the
same type.

To return a value, simply write "Then you get" followed by the return value.

**Example:** `Then you get 99!`

Returns the number 99.

**Example:** `Then you get the answer!`

Returns the value stored in the variable `the answer`.

#### Typescript equivalent
```typescript
return 99;
```
```typescript
return the_answer;
```

### Ending a method
Methods must be ended with "That's all about" followed by the method name. Note
that method declarations in interfaces do not have a body, and therefore do not
need to be ended.

**Example:**
```
I learned about friendship:
P.S. method body goes here
That's all about friendship.
```

#### Typescript equivalent
```typescript
friendship() {
  // method body goes here
}
```

### Calling a method
To call a method, you must reference the object instance it's a member of (or
the name of the class, if it's a static method) followed by "remembered" or
"would", and then the method name. If you are supplying parameters to the method
call, follow the mthod name with "using" and each parameter (separating multiple
parameters with "and").

When calling a method that is a member of the current object (or one of its
ancestors) from within an instance method, you can use "I" as the object
reference, or else omit the reference (and the "remembered"/"would" keyword)
entirely. This works for both static and instance methods.

When referencing a static method that's a member of the current class (or one of
its ancestors) from within a static method, you can omit the object reference
(and the "remembered"/"would" keyword) entirely.

**Example:** `Did you know that Spike was Spike's age?`

This calls the function "Spike's age" on the current object, and assigns the
return value to the variable `Spike`.

**Example:** `I said how to write Hello World!`

This calls the function "how to write Hello World" and prints the return value
to the output stream.

**Example:** `I remembered how to write Hello World using Quills.`

Calls the same function in the previous example, but passes the parameter
`Quills`, and doesn't print the return value.

**Example:** `Applejack remembered a countryism!`

Calls the function "a countryism" on the object `Applejack`.

#### Typescript equivalent
```typescript
let Spike = this.Spike_s_age();
```
```typescript
console.log(this.how_to_write_Hello_World());
```
```typescript
this.how_to_write_Hello_World(Quills);
```
```typescript
Applejack.a_countryism();
```

## Future Work
* This specification does not currently include abstract methods.
