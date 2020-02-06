## FiM++ Specification
This file provides a specification for this FiM++ implementation using
[Backus–Naur form](https://en.wikipedia.org/wiki/Backus%E2%80%93Naur_form).

This document serves as the source of truth for this FiM++ implementation's
syntax. If there is a conflict with the rest of the documentation, this document
supercedes the content of the others.

### Programs
```ebnf
<compilation unit> ::= [<import declarations>] [<type declarations>]
```

### Declarations
```ebnf
         <import declarations> ::= <import declaration> | <import declarations> <import declaration>
          <import declaration> ::= <file import> | <type import>
                 <file import> ::= Remember when I wrote in <string literal> <terminator>
                 <type import> ::= Remember what I said about <type declaration> when I wrote in <filename> <terminator>
           <type declarations> ::= <type declaration> | <type declarations> <type declaration>
            <type declaration> ::= <class declaration> | <interface declaration>
           <class declaration> ::= Dear <class type> [and <interface type list>]: <class type> <terminator> <class body> <type declaration footer>
         <interface type list> ::= <interface type> | <interface type list> and <interface type>
                  <class body> ::= [<class body declarations>]
     <class body declarations> ::= <class body declaration> | <class body declarations> <class body declaration>
      <class body declaration> ::= <field declaration> | <method declaration> | <constructor declaration>
     <constructor declaration> ::= TO BE DETERMINED
           <field declaration> ::= [<static modifier>] <field modifier> <variable declarator> <terminator>
         <variable declarator> ::= <identifier> [<constant modifier>] <identifier linker> <value or type> <terminator>
               <value or type> ::= <literal> | <expression> | <type>
          <method declaration> ::= <method header> <method body> <method footer>
               <method header> ::= <method modifier> <identifier> [<return type linker> <type>] [using <parameter list>] <terminator>
             <method modifier> ::= <entry point modifier> | <member method modifier>
      <member method modifier> ::= [<static modifier>] <method access modifier>
              <parameter list> ::= <parameter typed list> | <typed parameter list>
        <parameter typed list> ::= <type> <identifier list> | <parameter list> and <type> <identifier list>
        <typed parameter list> ::= <type> <identifier> | <parameter list> and <type> <identifier>
             <identifier list> ::= <identifier> | <identifier list> and <identifier>
                 <method body> ::= <statement list>
              <statement list> ::= <statement> | <statement list> <statement> |
               <method footer> ::= That's all about <identifier> <terminator>
     <type declaration footer> ::= Your faithful student, <string characters>
       <interface declaration> ::= <interface type> [and <interface type list>] <terminator> <interface body> <type declaration footer>
              <interface body> ::= [<interface body declarations>]
 <interface body declarations> ::= <interface body declaration> | <interface body declarations> <interface body declaration>
  <interface body declaration> ::= <interface field declaration> | <interface method declaration>
 <interface field declaration> ::= I know that <variable declarator> <terminator>
<interface method declaration> ::= I learned <identifier> [<return type linker> <type>] [using <parameter list>] <terminator>
```

### Types
```ebnf
                   <type> ::= <primitive type> | <object tpye>
         <primitive type> ::= <numeric type> | <string type> | <boolean type>
           <boolean type> ::= logic | argument
            <string type> ::= letter | character | word | phrase | sentence | quote | name
           <numeric type> ::= number
            <object type> ::= <class or interface type> | <array type>
             <array type> ::= many <type><plural suffix>
<class or interface type> ::= <class type> | <interface type>
             <class type> ::= <type name>
         <interface type> ::= <type name>
```

### Statements
```ebnf
                 <statement> ::= <local variable declaration> | <if statement> | <while statement> | <do while statement> | <for statement> | <switch statement> | <try statement>
          <simple statement> ::= <expression statement> | <return statement>
              <if statement> ::= <if then statement> | <if then else statement> | <if then elseif statement>
         <if then statement> ::= <if linker> <expression> [then] <terminator> <statement list> <if statement footer>
    <if then else statement> ::= <if linker> <expression> [then] <terminator> <statement list> <else linker> <terminator> <statement list> <if statement footer>
  <if then elseif statement> ::= <if linker> <expression> [then] <terminator> <statement list> <else linker> <if statement>
       <if statement footer> ::= That's what I would do <terminator>
           <while statement> ::= <while linker> <expression statement> <statement list> <statement footer>
          <statement footer> ::= That's what I did <terminator>
        <do while statement> ::= Here's what I did <terminator> <statement list> <do while footer>
           <do while footer> ::= <do while linker> <expression statement>
             <for statement> ::= <counting for statement> | <iterable for statement>
    <counting for statement> ::= For every <identifier> from <expression> <counting direction> <expression> [by <expression>] <terminator> <statement list> <statement footer>
    <iterable for statement> ::= For every <identifier> in <expression statement> <statement list> <statement footer>
          <switch statement> ::= <switch header> <case list> <statement footer>
             <switch header> ::= <switch linker> <expression statement>
                 <case list> ::= <case statement> | <case list> <case statement>
            <case statement> ::= <case discriminator> <terminator> <statement list>
        <case discriminator> ::= On the <number literal><ordinal suffix> hoof | In the case of <constant expression>
             <try statement> ::= TO BE DETERMINED
      <expression statement> ::= <expression> <terminator>
          <return statement> ::= Then you get <expression statement>
<local variable declaration> ::= Did you know that <identifier> <identifier linker> <type or expression> <terminator>
        <type or expression> ::= <type> | <expression>
```

### Expressions
```ebnf

```

<string literal>
<string characters>
<literal>
<expression>
<identifier>
<terminator>
<type name>
<number literal>
<constant expression>

### Tokens
```ebnf
<field modifier> ::= I know that | We know that | I secretly know that
<static modifier> ::= Finally,
<constant modifier> ::= always
<entry point modifier> ::= Today I learned
<identifier linker> ::= is | was | has | had | likes | liked
<method access modifier> ::= I learned | We learned | I secretly learned
<return type linker> ::= with | to get
<plural suffix> ::= s | es
<ordinal suffix> ::= st | nd | rd | th
<if linker> ::= if | when
<else linker> ::= Otherwise | Or else
<while linker> ::= Here's what I did while | As long as
<do while linker> ::= I did this while | I did this as long as
<counting direction> ::= up to | down to
<switch linker> ::= In regards to | With regard to
```
