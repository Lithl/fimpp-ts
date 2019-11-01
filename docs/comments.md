## FiM++ Comments
Comments come in two varieties: inline and block, just as in so many languages.

### Inline comments
An inline comment is preceded by the string "S.", which is itself preceded by
one or more instances of the string "P.". Everything from the first "P." to the
end of the line is ignored.

**Example:** `Did you know that Applejack likes numbers? P.S. I don't know how
high she can count, though.`

In this case, `Did you know that Applejack likes numbers?` declares a variable,
while the rest of the line does nothing.

**Example:**
```
Did you know that Applejack likes numbers? P.S. I don't know how high she can count, though.
P.P.S. That's mean, I shouldn't says that. Ignore that!
```

This example is functionally identical to the previous one, simply with multiple
comments. Do note that the number of "P."s is arbitrary, and it is not
_required_ that you follow a sequence of increasing-number of "P."s as is proper
for writing an actual letter with actual postscripts. You can also write more
code after a P.S., it doesn't have to be the last line of your letter.

#### Typescript equivalent
```typescript
let Applejack: number; // I don't know how high she can count, though.
// That's mean, I shouldn't say that. Ignore that!
```

### Block comments
A block comment is preceded by the character "(" and followed by the character
")". The two parentheses and everything between them is ignored.

**Example:**
```
Dear Princess Luna (and by extension, Princess Celestia): Hey, Luna!
Your faithful student, Lithl.
```

In this case, `Dear Princess Luna: Hey, Luna!` defines a class named `Hey, Luna`
which extends `Princess Luna`. The parenthetical between `Luna` and `:` is
ignored.

**Example:**
```
(This letter functions as a simple example of a FiM++ program.
When running this program, it will simply print "Hello, World!" and exit)
Dear Princess Celestia: Hello World!
Today I learned how to say hello world.
I said "Hello,World!"
That's all about hot to say hello world.
Your faithful student, Lithl.
```

This example demonstrates that the block comment can span multiple lines.

#### Typescript equivalent
```typescript
class Hey_Luna extends Princess_Luna /*and by extension, Princess Celestia*/ {
} // Lithl
```
```typescript
/*This letter functions as a simple example of a FiM++ program.
When running this program, it will simply print "Hello, World!" and exit*/
class Hello_World extends Object {
  static how_to_say_hello_world(): void {
    console.log('Hello, World!');
  }
} // Lithl
```

#### A note on math
Yes, the fact that parentheses are used for block comments does cause a problem
for writing math which needs parentheses to control order of operations. One
option is simply to rewrite whatever equation you need in a way that the
parentheses are not required. For example, instead of `a * (b + c)`, you could
write `a * b + a * c`. Alternatively, you could write several operations in
sequence, such as `b + c` stored in a temporary variable followed by `a * tmp`.

An amendment could also be made to the language syntax, but when that happens
this documentation ought to be updated!
