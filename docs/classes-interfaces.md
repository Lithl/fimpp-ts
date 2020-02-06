## FiM++ Classes
Classes are extensible pieces of program code, providing state and behavior.
Each class in FiM++ is like a letter.

### Class declaration
A class declaration begins with the string "Dear", followed by the name of the
superclass being inherited from. Zero or more instances of "and" followed by an
interface name come next, a colon (`:`, and yes this means the colon has a use
other than as a line-terminator), and finally the name of the class being
defined.

All classes must explicitly specify the class they inherit from. If no other
class is appropriate or available, use `Princess Celestia`, which is the
superclass for all other classes, equivalent to Typescript's `Object`.

**Example:**  
`Dear Princess Celestia: Letter One.`

This creates a class named "Letter One", which extends "Princess Celestia".

**Example:**  
`Dear Princess Luna and Shining Armor and Princess Cadance: An Update:`

This creates a class named "An Update", which extends "Princess Luna" and
implements both "Shining Armor" and "Princess Cadance".

#### Typescript equivalent
```typescript
export class Letter_One extends Object {
```
```typescript
export class An_Update extends Princess_Luna
    implements Shining_Armor, Princess_Cadance {
```
Note that all classes will be exported.

### Ending a class
Classes must be ended with the text "Your faithful student," followed by some
text. By convention, that text should be the name of the class's author, but it
is functionally an inline comment with special syntax and could therefore be
anything.

**Example:**  
`Your faithful student, Lithl.`

#### Typescript equivalent
```typescript
} // Lithl
```

## FiM++ Interfaces
An interface is an abstract type that defines behaviors via method signatures,
but does not define implementations for them. Interface syntax is very similar
to class syntax in FiM++.

### Interface declaration
An interface declaration begins with the name of the interface being defined,
followed by zero or more instances of "and" followed by another interface name
to extend the other interface.

An interface is not required to explicitly extend anything, unlike classes.

**Example:**  
`Princess Cadance:`

This creates an interface named "Princess Cadance".

**Example:**  
`Shining Armor and Guard Captain and BBBFF:`

This creates an interface named "Shining Armor", which extends both the "Guard
Captain" interface and the "BBBFF" interface.

#### Typescript equivalent
```typescript
export interface Princess_Cadance {
```
```typescript
export interface Shining_Armor extends Guard_Captain, BBBFF {
```
Note that all interfaces will be exported.

### Interface restrictions
* Method signatures in an interface may not be marked private (using the
  `I secretly learned` keyword phrase).
* Method signatures in an interface may not be marked protected (using the
  `We learned` keyword phrase).
* No method signature in an interface may be marked as a program entry point
  (using the `Today` keyword).

### Ending an interface
Interfaces are ended in exactly the same way as classes, above.

## Future Work
* This specification does not currently include abstract classes
* This specification does not currently include explicit calls to the
superclass's constructor or methods.
* This specification does not currently have any means to inspect the
inheritance tree (`instanceof`).
