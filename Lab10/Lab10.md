# EE160 Lab 10: More Loops 

(Repo of lab notes: <https://github.com/duck8880/EE160>)

(Lab 8 spec: <http://www-ee.eng.hawaii.edu/~tep/EE160/Labs/Lab10/lab10.html>)

​     

## Notes

- Common mistakes

  - Properly use ""**&&**"" or "**||**" in the condition in **while()** or **if()** statement: 

    ```c
    while(a >= 0 && a <= 10) { ... }
    if (b == 0 || b == 1) { ... }
    ```

  - We don't have to write the `if (a <= 0)` in the following code : 

     ```c
     if (a > 0) {
         // do something
     } else if (a <= 0) {
         // do another thing
     }
     ```
     Just write like this:

     ```c
     if (a > 0) {
         // do something
     } else {
         // do another thing
     }
     ```
     
  - \#include only .h files in your .c files. Don't \#include .c files.

  - Makefile

    ```makefile
    # target to make all programs for Lab 9
    all: mygrader mygrader2 countgrades
    
    # Problem 1 - grader programs
    #       complete the dependency and action lines for your filenames
    mygrader: driver.o grader.o
            cc  -o mygrader driver.o grader.o
    
    mygrader2: driver2.o grader2.o
            cc  -o mygrader2 driver2.o grader2.o
    
    # Problem 2 - grade counter
    countgrades: countgrades.o
            cc -o countgrades countgrades.o
    
    # source file dependencies
    #       add target lines showing dependencies for your .o files
    driver.o:
    
    grader.o:
    
    driver2.o:
    
    grader2.o:
    
    countgrades.o:
    
    # utility targets
    
    clean:
            rm -f *.o
    
    real_clean: clean
            rm -f mygrader mygrader1 countgrades

    ```



​     

## Tasks

- Create a new directory **`EE160/Labs/Lab10`** as your working directory.

- (6 Points). **Exploring the "for" and "while" statements. **
  
  



     ​




## Submission

- Turn in the all of the source files (.c and .h files) you created using:

  `grade -lab10s2,ee160  *.c *.h`  

  Verify your submission using:

  `grade -lab10s2,ee160`  


   ​

## Useful VI commands to copy, cut, paste, etc.

  `v`: enter visual mode;    `h`, `j`, `k`, `l`: move cursor  
  `0`: to the beginning of a line;    `$`: to the end of a line  
  `c`: cut;    `y`: copy;    `p`: paste;    `cc` or `dd`: cut the current line;    `yy`: copy the current line  
  `u`: undo;    `Ctrl`+`r`: redo

## Tutorial offering from the CoE

<http://web.eng.hawaii.edu/Tutor/intro.html>

## Unix/Linux Command Cheat Sheet

<https://files.fosswire.com/2007/08/fwunixref.pdf>