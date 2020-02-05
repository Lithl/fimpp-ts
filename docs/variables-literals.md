## FiM++ Variables
### Variable declaration
A variable is declared with the keyword phrase `Did you know that` followed by
the variable label, one of the keywords `is`, `was`, `has`, `had`, `likes`, or
`liked` and the variable type.

To declare the variable as being a constant, add the keword `always` after the
variable label.

A variable declaration can include an initial value by giving the value instead
of the variable type. A constant variable _must_ include an initializer.

**Example:**  
`Did you know that Applejack has a number?`

Declares a variable named "Applejack" that is a number.

**Example:**  
`Did you know that the number of pies is 5?`

Declares a variable named "the number of pies" with an initial value of 5.

**Example:**  
`Did you know that the book's title always was "The Elements of Harmony: A Reference Guide"?`

Declares a constant variable named "the book's title" with a value of "The
Elements of Harmony: A Reference Guide".

If the variable's type is an object, you can construct a new object using the
keyword phrase `brand new` followed by the object type name. If the constructor
has parameters, set them with the `using` keyword just like
[calling a method](methods.md#calling-a-method).

**Example:**  
`Did you know that the book was a brand new Encyclopedia using 'Ferns and Fillies'?`

#### Typescript equivalent
```typescript
let Applejack: number;
```
```typescript
let the_number_of_pies = 5;
```
```typescript
const the_book_s_title = 'The Elements of Harmony: A Reference Guide';
```
```typescript
let the_book = new Encyclopedia('Ferns and Fillies');
```

### Field declaration
Fields are variables declared at the class level, rather than at the function
level (or lower).

A public field is declared with `I know that`.

A protected field is declared with `We know that`.

A private field is declared with `I secretly know that`.

A static field declaration is prefixed with `Finally,`.

Field declarations are otherwise identical to variable declarations.

### Variable and field referencing
To reference a variable in the current scope, sinply use its label.

To reference a field, reference the object instance it's a member of (or the
name of the class, if it's a static field) followed by "remembered" or "would",
and then the field name.

When referencing a field that's a member of the current object (or one of its
ancestors) from within an instance method, you can use "I" as the object
reference, or else omit the reference (and the "remembered"/"would" keyword)
entirely. This works for both static and instance fields.

When referencing a static field that's a member of the current class (or one of
its ancestors) from within a static method, you can omit the object reference
(and the "remembered"/"would" keyword) entirely.

### Variable and field assignment
To change the value of a non-constant variable or field, use the label followed
by one of these keyword phrases:

* is now
* are now
* is now like
* are now like
* now likes
* now become
* now becomes
* becomes

Then, follow with the new value for the variable or field.

**Example:**  
`Applejack now likes 0.`

Assigns the value 0 to the variable "Applejack".

**Example:**  
`the number of pies becomes 25.`

Assigns the value 25 to the variable "the number of pies".

**Example:**  
`Twilight remembered her checklist is now correct.`

Assigns the value true to the field "her checklist" in the "Twilight" object.

#### Typescript equivalent
```typescript
Applejack = 0;
```
```typescript
the_number_of_pies = 25;
```
```typescript
Twilight.her_checklist = true;
```

### List of variable types
A type keyword may optionally be prefixed with "the", "a", or "an".

* 64-bit floating-point number
    * `number`
* String
    * One of: `letter`, `character`, `word`, `phrase`, `sentence`, `quote`,
      `name`<br>
      _Note: The FiM++ specification distinguishes a single-character type from
      a multi-character type. However, that specification is based on Java,
      while this compiler targets Typescript, which makes no such distinction._
* Boolean
    * One of: `logic`, `argument`
* Array
    * `many` followed by another type name, optionally suffixed with "s" or "es"
* Object
    * The object label

### Literals
* 64-bit floating point number
    * `/[1-9]\d*(?:\.\d+)?/` for a base-10 number
    * `/0b[01]+/` for a base-2 integer
    * `/0[0-7]+/` for a base-8 integer
    * `/0x[0-9a-fA-F]+/` for a base-16 integer
* String
    * A sequence of unicode characters prefixed and suffixed with a single quote
      (`'`), excluding newline characters. Escape sequences can be included.
    * A sequence of unicode characters prefixed and suffixed with a double quote
      (`"`), excluding newline characters. Escape sequences can be included.
    * A sequence of unicode characters prefixed and suffixed with a single
      backtick (`` ` ``), including newline characters. In addition to the
      escape sequences usable in other strings, you can wrap an expression with
      `${` and `}` in order to insert the result of the expression into the
      string.
* Boolean
    * `yes`, `true`, `right`, `correct`
    * `no`, `false`, `wrong`, `incorrect`
* Null
    * `empty`
    * `none`
* Undefined
    * `nothing`

## Future work
* This specification does not currently have any means to inspect variable or
field types (`typesof`).
