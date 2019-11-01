## FiM++ Language Specification
This directory contains specification for the FiM++ language, based on [the
original specification document](https://docs.google.com/document/d/1gU-ZROmZu0Xitw_pfC1ktCDvJH5rM85TxxQf5pg_xmg/edit?pli=1#).

* [Comments](comments.md#fim-comments)
* [Classes and Interfaces](classes-interfaces.md#fim-classes)
* [Methods](methods.md)
* [Variables](variables.md)
* [Literals](lierals.md)
* [Operators](operators.md)
* [Input/Output](input-output.md)
* [Logic](logic.md)
* [Control flow](control-flow.md)

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
