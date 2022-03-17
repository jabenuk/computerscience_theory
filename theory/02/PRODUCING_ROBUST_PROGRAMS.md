# 2.3 Producing robust programs

## 2.3.1 Defensive design considerations

### Input validation

To **validate input** is simply to ensure that given input is going to work with the program. For example, checking the input is not too long or too short, or making sure that any input was given in the first place.

### Data sanitisation

The purpose of **data sanitisation** is to hide or protect data. 

One example of this is known as **masking**: hiding visible data by replacing it with something else, like replacing the letters in a password field with asterisks or bullets.

Another method of data sanitisation is **input sanitisation** - to check data that is entered and remove anything that could be dangerous. Input sanitisation is essential in web development to protect from **SQL injection** (entering SQL queries into an input form), or **XSS** (cross site scripting - executing JavaScript via an input form).

### Planning for contingencies

**Contingencies** are possible but uncertain events - edge cases. When dealing with user input, all contingencies should be considered.

### Anticipating misuse

Avoid errors when recieving invalid or malicious input.

### Basic authentication

There are three factors of authentication, as explained by Tom Scott[^1]:
 - **something you know** (password, PIN, signature, etc.)
 - **something you are** (username, ID, biometrics, etc.)
 - **something you have** (bank card, phone, key, etc.)

## 2.3.2 Testing code

The purpose of **testing** is to find and eliminate any bugs or logic errors.

### Types of testing

#### Iterative testing

Iterative testing is carried out while a program is being developed. The developer writes a module (section of code) and then tests it - the module might work fine, but the developer will probably amend the code later on and test it again. This process repeats until the module works as intended.

#### Final/terminal testing

Final, or terminal, testing is carried out when all modules are complete. The program is tested as a whole to ensure that it functions as it should.

### Selecting and using suitable test data

**Test data** is data that is used to test a program. Three types of data are:
 - **valid data** - sensible, possible data that the program should be able to accept
 - **extreme data** - valid data that falls at the boundary of possible ranges (edge cases)
 - **invalid (erroneous) data** - data that the program cannot process and should not accept

Developers should use a **test plan**, a list of all the tests that will be used. This plan should involve several examples of valid, extreme, and invalid data.

#### Testing tables

Here is an example of a **testing table.** This one is for a program that asks a user to input a value between (inclusive) 1 and 10.

| # | Description | Test data | Test type | Expected | Actual | Passed |
| - | -  | - | - | - | - | - |
| 1 | Test that a possible number is accepted | 5 | Valid | Data is accepted | Data was accepted | 🟢 |
| 2 | Test the lower boundary | 1 | Extreme | Data is accepted | Data was accepted | 🟢 |
| 3 | Test the upper boundary | 10 | Extreme | Data is accepted | Data was accepted | 🟢 |
| 4 | Test that the program does not accept a number less than 1 | -50 | Invalid | Data is not accepted | Data was accepted | 🔴 |
| 5 | Test that the program does not accept a number greater than 10 | 100 | Invalid | Data is not accepted | Data was not accepted | 🟢 |

### Errors

**Syntax errors** are errors related to the syntax of the source code. **Logic errors** are errors in the way a program works - i.e., there are no exceptions or build errors, but the program does not work as intended.

## References

### Sections
 - [2.3.1 Defensive design considerations](https://www.bbc.co.uk/bitesize/guides/z4cg4qt/revision/1)
 - [2.3.2 Testing code](https://www.bbc.co.uk/bitesize/guides/z4cg4qt/revision/7)

[^1]: [YouTube link](https://www.youtube.com/watch?v=hGRii5f_uSc)
