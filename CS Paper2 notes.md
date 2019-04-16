## 2.1 ALGORITHM DESIGN & PROBLEM-SOLVING

### 2.1.1 Algorithms

------

**Algorithm:** a solution to a problem expressed as a sequence of steps



### 2.1.1.1 Identifier Table

- **Identifier:** name given to a variable in order to call it 
- An identifier table depicts information about the variable, e.g.
- Rules for naming identifiers:
  ~ Must be unique
  ~ Spaces must not be used
  ~ Must begin with a letter of the alphabet
  ~ Consist only of a mixture of letters and digits and the underscore character _
  ~ Must not be a 'reserved' word – e.g. Print, If, etc.

### 2.1.1.2 Basic Program Operations

- **Assignment:** an instruction in a program that places a value into a specified variable
- **Sequence:** programming statements are executed consequently, as they appear in the program
- **Selection:** control structure in which there is a test to decide if certain instructions are executed
  - <u>IF selection:</u> testing 2 possible outcomes
  - <u>CASE selection</u>: testing more than 2 outcomes
- **Repetition/Iteration:** control structure in which a group of statements is executed repeatedly
  - **FOR loop:** <unconditional> executed a set no. of times 
  - **WHILE loop:** <conditional> executed based on condition at start of statements
  - **REPEAT loop:** <conditional> executed based on condition at end of statements



### 2.1.1.3 Structured English

<INCOMPLETE>

### 2.1.1.4 Flowchart

<IMCOMPLETE>



### 2.1.1.5 Stepwise Refinement

- Process of developing a <span style="color:red">modular design </span>
- by **splitting** a problem into smaller **sub-tasks** [which themselves are repeatedly split into even smaller sub-tasks until each is just one element of the final program]

**<WAITING FOR EXAMPLE>**

### 2.1.1.6 Program Modules

- This refers to a <span style="color:red">modular design </span>
- **Subroutines**: 
  - self-contained section of code
  - performing a specific task
  - part of the main program
- **Procedures**: 
  - performs a specific task
  - no value returned to part of code where called
- **Functions**: 
  - performs a specific task
  - returns a value







### 2.1.2 Structure Charts

------

- **Features**:
  - **Parameter** that are passed between modules
  - **Hierarchy** of modules
  - **Sequence** of module execution
- **Purpose: **
  - used in <structured programming> to arrange program modules
  - -> each module represented by a box
- **Tree structure** visualizes relationships between modules, showing data transfer between modules using arrows.
- Rules:

| Symbols     | Description                                                  |
| ----------- | ------------------------------------------------------------ |
| Process     | Represents a programming module e.g. a calculation           |
| Data Couple | Data being passed from module to module that needs to be processed |
| Flag        | Check data sent to start or stop a process. E.g. check if data sent in the correct format |
| Selection   | Condition will be checked and depending on the result, different modules will be executed. |
| Iteration   | Implies that module is executed multiple times               |



### 2.1.3 Corrective Maintenance

------

**Corrective maintenance**: 

- a maintenance task or operation done in order to identify, isolate or separate and rectify a particular fault. 
- This is performed in order to restore the failed machine, equipment or system to an operational condition. 
- Corrective maintenance is necessary when a fault or bug is found in the operation of the new system. 
- These are software bugs which were not picked up at the formal testing stage. 
- A technician or the original programmers will be needed to correct the error.

### 2.1.3.1 White-Box testing

- testing every path through the program code
- Tester validates the internal structure of the item under consideration along with the output. 
- In IDE setting breakpoints, stepping and subroutine parameter checking are the features that provides to carry out white box testing. 



### Black box testing

- Tester is mainly concerned with validation of output rather than how the output is produced. 
- In short, black-box testing is comparing expected value with actual results when program runs.

**Trace table:** technique used to test algorithms; make sure that no logical errors occur e.g.



### Stub Testing

- When you develop a user interface, you may wish to test it before you have implemented all the facilities. 
- You can write a ‘stub’ for each procedure. 
- The procedure body only contains an output statement to acknowledge that the call was made.

| Black box testing                                            | White box testing                                     |
| :----------------------------------------------------------- | :---------------------------------------------------- |
| Tester don't know the internal structure, design and implementation of the data | Tester know them                                      |
| Programming Implementation and knowledge is not required.    | Programming Implementation and knowledge is required. |
| It means functional test or external test.                   | It means structural test or interior test.            |



### 2.1.3 Adaptive Maintenance

------

- The action of making amendments to a program to enhance functionality or in response to specification changes. 
- Adaptive maintenance is necessary when conditions change from those that existed when the original system was created. 
- This may be because of a **change** in the law (tax rates may change, for example) or the hardware may be changed, so that changes need to be made to the software for it to remain functional. 
- Making amendments to:
  - Parameters: due to changes in specification
  - Logic: to enhance functionality or more faster or both
  - Design: to make it more user friendly



### Rogue value

- A specific value
- outside the generally **expected range**
- which is used to **terminate** a list of data items.



### 2.1 Data Types

#### Integer:

- Positive or negative number; no fractional part
- Held in pure binary for processing and storage
- Some languages differentiate short/long integers (more bytes used to store long integers)

#### Real:

- Number that contains a decimal point
- Referred to as singles and doubles depending upon number of bytes used to store

#### Boolean:

- Can store one of only two values; “True” or “False”
- Stored in 1 byte: True = 11111111, False = 00000000 String:
- Combination of alphanumeric characters enclosed in “ ” 
- Each character stored in one byte using ASCII code
- Each character stored in two bytes using Unicode
- Max length of a string limited by available memory.
- Phone no. must be stored as string else initial 0 lost Character:
- A character is any letter, number, punctuation or space 
- Takes up a single unit of storage (usually a byte). 

#### Dates:

- Dates are stored as a ‘serial’ number
- Equates to the number of seconds since January 1st, 1904 (thus they also contain the time)
- Usually take 8 bytes of storage
- Displayed as dd/mm/yyyy or mm/dd/yyyy

### 2.2 ASCII Code

- Uses 1 byte to store a character
- 7 bits available to store data and 8th bit is a check digit 
- 27 = 128, therefore 128 different values
- ASCII values can take many forms: numbers, letters (capitals and lower case are separate), punctuation, non- printing commands (enter, escape, F1)

### 2.3 Unicode

- ASCII allows few number of characters; good for English 
- Unicode allows others too: Chinese, Greek, Arabic etc. 
- 4 bytes per character
- Different types of Unicode:
  ~ UTF-8: compatible with ASCII, variable-width encoding can expand to 16, 24, 32, 40, 42
  ~ UTF-16: 16-bit, variable-width encoding can expand to 32 bits
  ~ UTF-32: 32 bit, fixed-width encoding, each character exactly 32 bits

### 2.4 Arrays

- Pseudocode:
  ~ 1-D Array: A[1:n]
  ~ 2-D Array: A[1:m, 1:n]
- Python:
  ~ Declaring an array: a = []
  ~ Adding to an array: a.append(anything)
  ~ Length of array i.e. number of elements: len(a) ~ Printing an element in a 1D array: print(a[x]) 
  ~ Printing element in a 2D array:
  print(a[row][column])
  ~ Printing row in a 2D array: print(a[row])
  ~ Printing column: use for loop and keep adding 1 to the row and keep column same

### 2.5 Bubble Sort

- A FOR loop is set to stop the sort
- Setting a variable ‘sorted’ to be ‘true’ at the beginning 
- Another FOR loop is set up next in order to search
  through the array
- An IF is used to see if the first number of the array is
  greater than the second. If true:
  ~ First number stored to variable
  ~ Second number assigned as first number
  ~ Stored variable assigned to second number
  ~ Set ‘sorted’ to ‘false’ causing loop to start again
- Files are needed to import contents (from a file) saved in secondary memory into the program, or to save the output of a program (in a file) into secondary memory, so that it is available for future use
  Pseudocode:
- Opening a file:
  ```OPENFILE <filename> FOR READ/WRITE/APPEND```
- Reading a file:
  ```READFILE <filename>```
- Writing a line of text to the file:
  ```WRITEFILE <filename>, <string>```
  Python:
- Opening a file
  ```variable = open(“filename”, “mode”)```
  Where the mode can be:
- Reading a file:
  ~ Read all characters variable.read()
  ~ Read each line and store as list variable.readlines()
- Writing to a file:
  ~ Write a fixed a sequence of characters to file variable.write(“Text”)
  ~ Write a list of string to file variable.write[“line1”, “line2”, “line3”]
- Programming is a transferable skill
- Transferable skill: skills developed in one situation which can be transferred to another situation.

### 2.5 File Handling

- Closing a file:
- Testing for end of the file:
- The second FOR loop is count based thus will stop after a specific number of times
- Goes through bigger FOR loop ∴ ‘sorted’ remains ‘true’ 
- This exits the loop ∴ ending the program

### 2.6 Linear Search

- A FOR loop goes through the array
- It compares item in question to those in list using an IF:
  ~ If item matches with another then search is stopped ~ Also the location where it was found is returned
  ~ If not found it exits the FOR loop

| Mode | Description                                                  |
| ---- | ------------------------------------------------------------ |
| r    | Opens file for reading only. Pointer placed at the beginning of the file. |
| w    | Opens a file for writing only. Overwrites file if file exists or creates new file if it doesn’t |
| a    | Opens a file for appending. Pointer at end of file if it exists or creates a new file if not |

- Then returns fact that item in question is not in the list



## 2.3 Variables

### 2.3.2 Transferable skills

- Ability to define a specific problem in a particular situation
- understand and expand the learns of broad generality that can be applied in other in other situation or field
- develop the use cases that solve the specific problem in such a way as the tool developed can be applied to the broader case.
- **Similar syntax**
  - Assignment, variable, data types 
  - Common operators, Symbols for functions 
- **Control structures**
  - Iteration
  - Selection
  - Sequence
  - Layout, format (e.g. indentation ) 
- **Modular features**
  - Objects
  - Procedures
  - Functions



### 2.3.6 Structured programming

#### Function

- **returns** a value
- Functions are normally used for **computations** 
- has **return** type. 
- function only accepts **input** **parameters**.



#### Procedure

- procedure may or may **not** return a value or may return more than one value using the output parameters. 
- procedures are normally used for **executing business logic.** 
- Procedure is a **bundle** of code, it does not have return type
- Procedure accepts **input or output parameters**



## 2.4 SOFTWARE DEVELOPMENT

### 2.4.1 Programming

#### Program development cycle

1. Design
2. Coding
3. Testing

### 4.2 Integrated Development Environment

- A software application that allows the creation of a program e.g. Python
- Consists of a source code editor, build automation tools, a debugger
- **Coding:**
  - **Context-sensitive prompts:** reserved words are used by it as command prompts 
  - Listed in the end-user documentation of IDE
  - A series of files consisting of preprogrammed-
    subroutines may also be provided by the IDE
- **Initial Error Detection:**
  - **Syntax/Logic Error:** 
    - before program is run, an error message warns the user about this
    - errors are highlighted
  - **Runtime Error:** run of the program ends in an error
  - **Type checking**
  - **Parameter checking**
  - **Identification of unused variables**
- **Debugging:**
  - **Single stepping:** traces through each line of code and steps into procedures. Allows you to view the effect of each statement on variables
  - **Breakpoints:** set within code; program stops temporarily to check that it is operating correctly up to that point
  - **Variable dumps** (report window): at specific parts of program, variable values shown for comparison
- **Presentation**
  - Pretty print
    - Indentation 
    - Colour-coding of keywords 
    - Expand and collapse code blocks

### 4.3 Types of Errors

#### Syntax errors:

- When source code does not obey rules of the language 
- Compiler generates error messages
- Examples:
  - Misspell identifier when calling it
  - Missing punctuation – colon after if
  - Incorrectly using a built-in function
  - Argument being made does not match data type

#### Run-time errors:

- Source code compiles to machine code but fails upon execution (red lines show up in Python)
- When the program keeps running and you have to kill it manually
- Examples:
  - Divisionby 0
  - Infinite loop – will not produce error message, program will just not stop until forced to

#### Logic errors:

- Program works but gives incorrect output 
- Examples:
  - Out By One – when ‘>’ is used instead of ‘>=’
  - Misuse of logic operators

### 4.4 Testing Strategies

#### Black box testing:

- Use test data for which results already calculated & compare result from program with expected results
- Testing only considers input and output and the code is viewed as being in a ‘black box’

#### White box testing:

- Examine each line of code for correct logic and accuracy. 
- May record value of variables after each line of code
- Every possible condition must be tested

#### Stub testing:

- Stubs are computer programs that act as temporary replacement for a called module and give the same output as the actual product or software.
- Important when code is not completed however must be tested so modules are replaced by stubs



#### Features that improve the code

- **Comment**
  - Explain the functionality of the code
- **Indentation**
  - Easier to identify structure





#### Why information is saved on a file rather than an array

- Information is saved after the program ends



#### Features that make the code easier to read and understand <fppmj22182a>

- Keywords in capitals 
- White Space / blank lines / grouping 
- Comments 
- Sensible function names 
- Indentation 
- Meaningful identifier names 



#### Local variables

- **variables that are declared**, (not parameters)



#### Benefits of using array rather than multiple variables

- Same data type using a single identifier / more efficient coding / less declaration statements needed 
- Access of individual elements (using subscript / index) 
- Ability to iterate through the data // easier to search / sort the data 
- Code easier to understand / maintain / modify 