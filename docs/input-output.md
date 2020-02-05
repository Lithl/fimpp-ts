## FiM++ Input and Output
### Output
There are four types of output available:

* Log
* Info
* Warn
* Error

These categories correspond to the following keyword phrases, collectively
referred to as output keywords:

* `I said` or `I sang`
* `I thought` or `I thought about`
* `I wrote` or `I wrote about`
* `I shouted` or `I cried`

To produce output, simply use an output keyword followed by an expression which
evaluates to the output you wish to produce.

`I said 'Hello, world'!`
```typescript
console.log('Hello, world');
```

`I thought about the baking competition results.`
```typescript
console.info(the_baking_competition_results);
```

`I wrote 'Nightmare Moon will be released soon'!`
```typescript
console.warn('Nightmare Moon will be released soon');
```

`I cried about my insurmountable friendship problem.`
```typescript
console.error(my_insurmountable_friendship_problem);
```

Of course, if you wish to produce some other kind of output, such as writing to
a file or throwing up text in a browser, you'll simply have to call the
appropriate methods.

### Input
To obtain user input from a prompt, use one of the keyword phrases "I heard",
"I read", or "I asked" followed by a string vairable or field reference.
Optionally, you may follow the variable or field reference with a string which
will be used for the prompt.

`I asked the pony 'What is your name? '.`

The result of this FiM++ code depends on whether the compiler was run using the
`--browser` flag. With the flag, this code produces:
```typescript
the_pony = window.prompt('What is your name? ');
```
Without the flag, however, it becomes:
```typescript
import readline from 'readline-promise';
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
// editor's note: the above code would be near the top of the file, not
// repeated each time the user code needs to ask for a prompt.

let the_pony: string;
rl.questionAsync('What is your name? ').then((answer: string) => {
  the_pony = answer;
});
```

Of course, if you wish to consume some other kind of input, such as reading from
a file or grabbing an input box value from a browser, you'll simply have to call
the appropriate methods.
