## FiM++ Language Specification
This directory contains specification for the FiM++ language, based on [the
original specification document](https://docs.google.com/document/d/1gU-ZROmZu0Xitw_pfC1ktCDvJH5rM85TxxQf5pg_xmg/edit?pli=1#).

* [Comments](comments.md#fim-comments)
* [Classes and Interfaces](classes-interfaces.md#fim-classes)
* [Methods](methods.md#fim-medthos)
* [Variables and Literals](variables-literals.md#fim-variables)
* [Operators](operators.md#fim-operators)
* [Logic](logic.md#fim-logic)
* [Input/Output](input-output.md#fim-input-and-output)
* [Control flow](control-flow.md#fim-control-flow)

### General notes
* Labels (keywords, variable names, class names, method names) can be multiple
  words with whitespace in-between. They may even include punctuation that isn't
  reserved for ending a line of code.
* All labels are case-sensitive, but keywords (or keyword phrases) are not.
* A line of code must be terminated with one of the reserved punctuation marks:
  * `.` (period)
  * `!` (exclamation mark)
  * `?` (question mark)
  * `‽` (interrobang)
  * `…` (ellipsis)
  * `:` (colon)
