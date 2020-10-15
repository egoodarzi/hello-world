# PEP 8 -- Style Guide for Python Code 
[source](https://www.python.org/dev/peps/pep-0008/)

"Readability counts"
## Indentation
Use 4 spaces per indentation level.

### Tabs or Spaces?
Spaces are the preferred indentation method.

Python 3 disallows mixing the use of tabs and spaces for indentation.

## Maximum Line Length
Limit all lines to a maximum of 79 characters.

1234567890123456789012345678901234567890123456789012345678901234567890123456789

For flowing long blocks of text with fewer structural restrictions (docstrings or comments), the line length should be limited to 72 characters.

Limiting the required editor window width makes it possible to have several files open side-by-side, and works well when using code review tools that present the two versions in adjacent columns.

 it is okay to increase the line length limit up to 99 characters, provided that comments and docstrings are still wrapped at 72 characters.

The preferred way of wrapping long lines is by using Python's implied line continuation inside parentheses, brackets and braces. These should be used in preference to using a backslash for line continuation.


## Should a Line Break Before or After a Binary Operator?
 displayed formulas always break before binary operations
```python
# Correct:
# easy to match operators with operands
income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)
```

## Blank Lines
Surround top-level function and class definitions with two blank lines.

Method definitions inside a class are surrounded by a single blank line.

Extra blank lines may be used (sparingly) to separate groups of related functions. 
Blank lines may be omitted between a bunch of related one-liners (e.g. a set of dummy implementations).

Use blank lines in functions, sparingly, to indicate logical sections.

Python accepts the control-L (i.e. ^L) form feed character as whitespace; 
Many tools treat these characters as page separators, 
so you may use them to separate pages of related sections of your file. 
Note, some editors and web-based code viewers may not recognize control-L 
as a form feed and will show another glyph in its place.

## Source File Encoding

Code in the core Python distribution should always use UTF-8 (or ASCII in Python 2).

## Imports
- Imports should usually be on separate lines:
```pyhton
# Correct:
import os
import sys
```
- Imports are always put at the top of the file, just after any module comments and docstrings, and before module globals and constants.
- Imports should be grouped in the following order:

  - Standard library imports.
  - Related third party imports.
  - Local application/library specific imports.
You should put a blank line between each group of imports.

## Module Level Dunder Names
Module level "dunders" (i.e. names with two leading and two trailing underscores) such as __all__, __author__, __version__, etc. 
should be placed after the module docstring but before any import statements except from __future__ imports. 

```python
"""This is the example module.

This module does stuff.
"""

from __future__ import barry_as_FLUFL

__all__ = ['a', 'b', 'c']
__version__ = '0.1'
__author__ = 'Cardinal Biggles'

import os
import sys
```
