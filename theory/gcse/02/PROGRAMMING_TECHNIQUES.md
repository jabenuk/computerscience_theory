# 2.2 Programming techniques

## 2.2.1 Use of variables

A variable is **a named memory address that stores a value.** The name of a variable is known as the **identifier.** Variables must be declared first before being defined. This can normally be done on the same line, if preferred.

**Constants** are variables that cannot be changed.

A **global** variable can be accessed throughout the program. In Python, the `global` keyword is used, whilst in good languages, the `public` and `static` keywords are the equivalent. **Local** variables are confined to a scope.

## 2.2.2 Operators

There are three types of operators:
 - **arithmetic operators:** `+`, `-`, `*`, `/`, `%`
 - **boolean operators:** `==`, `>=`, `<=`, `!=`, etc
 - **logical operators:** `&&` (and), `||` (or), `!` (not)

## 2.2.3 Basic file handling operations

Files have two modes of operation, read and write. Each item of data written to or read from a file is called a **record.**  Records in a file can be read line by line and stored in an array or the contents of the file can be read into a string. The file should be 'closed' when operations are complete.

Some sort of validation should be done to ensure the end of the file has not yet been encountered when operating on files. For example,
```js
while (!file.endOfFile()):
  // file operations here
endwhile
file.close();
```

## 2.2.4 Storing and accessing data

### The use of records to store data
A **database** is a persistent store of data, stored as **records** - these records are often represented as rows in tables.

An **attribute** is one component of data, such as *title*, *email*, *mobile*, etc. Records normally have more than one attribute.

### The use of SQL to query data

Consider this table with 4 records, each containing 5 fields:
| ID | Title | Forename | Surname | Email address |
| - | - | - | - | - |
| 1001 | Mr | Alan | Turing | aturing@adomain.com |
| 1002 | Mrs | Ada | Lovelace | alovelace@adomain.co.uk |
| 1003 | Miss | Grace | Hopper | ghopper@adomain.xyz |
| 1004 | Mr | George | Boole | gboole@adomain.net |

The table is called "Personnel".

 - `SELECT * FROM "Personnel" WHERE "Title" = "Mr"` would retrieve the records with IDs 1001 and 1004 (title field is 'Mr')
 - `SELECT * FROM "Personnel" WHERE "Email address" LIKE "%com"` would retrieve the record with ID 1001 (address field ends in 'com')
 - `SELECT * FROM "Personnel" WHERE "Surname" = "Turing" OR "Hopper"` would retrieve the records with IDs 1001 and 1003 (surname field is either 'Turing' or 'Hopper')

## 2.2.5 The use of subprograms

The GCSE 'subprogram' topic is awfully outdated. But OCR has forced my hand.

There are two types of subprogram:
 - **procedures** - subprograms that do not return values or manipulate data. (void methods)
 - **functions** - subprograms that return values and may manipulate data. (non-void methods)

## 2.2.6 Basic programming constructs

### Sequence
Sequence is the order in which instructions are executed.

### Selection
Selection is the process of making a decision. An example of selection is with the `if` keyword.

### Iteration
Iteration is often referred to looping, so sections of code that are iterated are often called loops. **Count-controlled iteration** is where the amount of iterations is controlled, such as in for loops. **Condition-controlled iteration** is where the amount of loops depends on a condition, such as in while loops. Condition-controlled loops can be written to continue forever (`while (true)`), but this is a very bad idea in every possible scenario.

## References

### Sections
 - [2.2.1 Use of variables](https://www.bbc.co.uk/bitesize/guides/zb3yb82/revision/1)
 - [2.2.2 Operators](https://www.bbc.co.uk/bitesize/guides/zb3yb82/revision/5)
 - [2.2.3 Basic file handling operations](https://www.bbc.co.uk/bitesize/guides/zb3yb82/revision/6)
 - [2.2.4 Storing and accessing data](https://www.bbc.co.uk/bitesize/guides/zb3yb82/revision/7)
 - [2.2.5 The use of subprograms](https://www.bbc.co.uk/bitesize/guides/zb3yb82/revision/8)
 - [2.2.6 Basic programming constructs](https://www.bbc.co.uk/bitesize/guides/znh6pbk/revision/1)
