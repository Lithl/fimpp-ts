## FiM++ Control flow
### Conditional block
Start a conditional block with one of the keywords "if" or "when" followed by a
boolean value or expression, and optionally the keyword "then".

* `If Spike was 10 then:`

The block can be continued with an else block using one of the keywords
"otherwise" or "or else". This can become an if-else by immediately beginning
anothr conditional block.

* `Otherwise:`
* `Or else if Twilight was 30:`

End the block or chain of blocks with the keyword phrase "That's what I would
do".

* `That's what I would do.`

#### Typescript equivalent
```typescript
if (Spike === 10) {
// ...

else {
// ...

else if (Twilight === 30) {
// ...

}
```

### Switch block
Start a switch block with one of the keyword phrases "in regards to" or "with
regard to" followed by a value.

* `With regard to Pinkie's Tail:`

Each case in the switch is defined with the keyword phrase "in the case of"
followed by a literal value. If the value being switched on is a number, you can
also use the keyword phrase "On the" followed by a literal number and one of "st
hoof", "nd hoof", "rd hoof", or "th hoof".

* `On the 1st hoof:`
* `In the case of 'Celestia':`

All statements following a case and before the next case will be executed if the
literal is exactly equal to the switch value. Do note that this implies two
things:

1. Fallthrough cases are _not supported_ in this implementation of FiM++.
Effectively, all cases break.
2. Because each case requires a literal value, there is little point in
providing an object value to the switch.

You can provide a default case with the keyword phrase "if all else fails".

* `If all else fails:`

Close the switch block with the keyword phrase "that's what I did".

* `That's what I did.`

#### Typescript equivalent
```typescript
switch (Pinkie_s_Tail) {
  case 1:
    break;
  case 'Celestia':
    break;
  default:
    break;
}
```

### Loops
#### While
To start a while loop, use one of the keyword phrases "here's what I did while"
or "as long as" followed by a boolean value or expression.

* `As long as Spike was less than 18:`

End the while loop with the keyword phrase "that's what I did".

* `That's what I did.`

```typescript
while (Spike < 18) {
  // ...
}
```

#### Do-while
To start a do-while loop, use the keyword phrase "here's what I did".

* `Here's what I did:`

End the do-while loop with one of the keyword phrases "I did this while" or "I
did this as long as" followed by a boolean value or expression.

* `I did this as long as Spike was less than 18.`

```typescript
do {
  // ...
} while (Spike < 18);
```

#### For
To create a standard for loop, use the keyword phrase "for every" followed by a
number variable or a variable label, the keyword "from", an initial number
value, the keyword phrase "up to" or "down to", and a final number value.
Optionally, you can follow the final value with the keyword "by" and an
increment value which will be added to (or subtracted from) the loop variable
each iteration.

* `For every x from 1 up to 10:`
* `For every pegasus from 10 down to 1:`
* `For every i from 1 up to 10 by 0.5:`

If the label is not an existing variable, a new local variable will be created.
The number variable will be assigned the initial value, and each iteration of
the loop it will be incremented (if the "up to" keyword phrase is used) or
decremented (if the "down to" keyword phrase is used) by 1, unless an increment
value is provided in which case that will be used instead.

End the loop with the keyword phrase "that's what I did".

* `That's what I did.`

```typescript
for (let x = 1; x <= 10; x++) {
  // ...

for (pegasus = 10; pegasus >= 1; pegasus--) {
  // ...

for (let i = 1; i <= 10; i += 0.5) {
  // ...

}
```

To create an iterable for loop, use the keyword phrase "for every" followed by a
variable or a variable label, the keyword "in", and an iterable object (such as
an array). The type of the loop variable must match the type of the elements in
the iterable object.

* `For every name in 'Rarity' and 'Applejack' and 'Pinkie Pie' and 'Fluttershy' and 'Rainbow Dash' and 'Twilight Sparkle':`

End the iterable for loop he same as a standard for loop.

```typescript
for (const name of [
      'Rarity',
      'Applejack',
      'Pinkie Pie',
      'Fluttershy',
      'Rainbow Dash',
      'Twilight Sparkle',
    ]) {
  // ...
```
